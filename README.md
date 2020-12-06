# gitops_manifest_helm
GitOpsのマニフェストリポジトリのサンプルです。

こちらのQiita記事で使用しています。  
`執筆中`

# 備忘録: HELMテンプレート新規作成手順

## コマンドを使用するために自分のマシンへHELMをインストール

公式インストール手順  
https://helm.sh/docs/intro/install/

## HELMテンプレートを新規作成する

この階層で以下のコマンドを実行
```
helm create .
```

## Chart.yamlのnameを変更しておく
`helm create .`した時の名前が自動セットされるため、nameの値が「.」になる。  
ここの名前がデプロイされるk8sリソース名に含まれるため、わかりわかりやすい名前に変えておく。

変更前
```
name: .
````

変更後
```
name: web
```