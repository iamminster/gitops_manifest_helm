# helm_nginx
create-react-appをGKE上にデプロイするサンプルリポジトリです。

# 備忘録: HELMテンプレート新規作成手順

## コマンドを使用するために自分のマシンへHELMをインストール

インストール手順  
https://helm.sh/docs/intro/install/

## HELMテンプレートを新規作成する

このリポジトリのトップディレクトリで以下のコマンドを実行
```
helm create .
```

## Chart.yamlのnameを変更

`helm create .`した時の名前がセットされるため、「.」となっている
ここの名前がデプロイされるk8sリソースに使用されるため、わかりわかりやすい名前に変えておく

変更前
```
name: .
````

変更後
```
name: nginx
```