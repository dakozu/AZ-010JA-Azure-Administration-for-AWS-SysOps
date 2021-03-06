﻿# ラボ 01 解答キー

## 指示

1. 以下の CLI スクリプトをメモ帳などのエディタにコピーする
   1. `# ----EDIT THESE VALUES Before Running----` と名付けられたロケーション セクション
   1. サブスクリプション ID を編集すると、エラーが発生します
   1. ファイルをローカルに保存する
1. Azure ポータルにログインし、bash Cloud Shell を開きます。
1. ローカル ファイルから CLI スクリプトをコピーし、Bash Cloud Shell にスクリプトを貼り付けます。
1. 一部のタスクは 1 分以上かかる場合があります。スクリプトが完了するのを待ち、出力を確認します。
1. エラーが発生した場合は講師と話しましょう

> 注: 受講生は、ラボ 01 で説明されているように、既定のサブスクリプションを設定する必要があります。

```sh
# AZ-010 LAB1 Solution
# 以下の値を指定します。
#   subscriptionID
# Azure CLI Bashで以下のコマンドを実行する前に
# 次を使用してサブスクリプションを表示: az account list -o table

# ----------START----------

# ----実行する前にこれらの値を編集する----
subscriptionID=[**subscription ID to use for labs**]

# ----主なスクリプト----
# ----デフォルトのサブスクリプションを設定する----
az account set --subscription $subscriptionID
# ---デフォルトのサブスクリプションに注意する---
az account list --output table

# ----WestRGの作成----
az group create --location westus --name WestRG --output table

# ----EastRGの作成----
az group create --location eastus --name EastRG --output table

# ----リソースグループの一覧表示----
az group list -o table
```
