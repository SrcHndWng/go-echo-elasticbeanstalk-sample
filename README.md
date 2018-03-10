# About This

Golang Echo で作成したWebアプリケーションをElastic Beanstalkで実行するサンプル。

ソースは[CRUD Recipe](https://echo.labstack.com/cookbook/crud)を元に変更。

# Elastic Beanstalkへのデプロイ手順

## 事前準備

Elastic Beanstalkで

* Web Server環境
* プラットフォームはGoを選択

して環境を作成しておくこと。

## ソースバンドル作成

1. build

```
GOARCH=amd64 GOOS=linux go build -o build/bin/application
```

2. zip

```
$ cd build
$ zip -r ../app.zip *
$ cd ..
```

## デプロイ

app.zipをElastic Beanstalkへデプロイする。

# 参考サイト
* https://dev.classmethod.jp/cloud/aws/elastic-beanstalk-supported-go/
* https://docs.aws.amazon.com/ja_jp/elasticbeanstalk/latest/dg/go-environment.html
* https://stackoverflow.com/questions/42209109/deploying-golang-app-in-cmd-folder-to-aws-beanstalk
* https://binhbv.wordpress.com/2017/03/20/deploying-a-simple-golang-application-to-aws-elastic-beanstalk-echo-framework/
* https://echo.labstack.com/cookbook/crud
