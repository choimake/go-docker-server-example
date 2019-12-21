# go-docker-server-example
書籍「Docker/Kubernetes 実践コンテナ開発入門」のDockerサンプルの写経です。

## 使い方
dockerイメージをビルドします。
```
docker image build -t example/echo:latest .
```
dockerコンテナを実行します。
```
docker container run -d -p 8080:8080 example/echo:latest
```
終了する場合は以下のコマンドを実行してください
```
docker container stop $(docker container ls --filter "ancestor=example/echo" -q)
```

## 参考
- [Docker/Kubernetes 実践コンテナ開発入門](https://www.amazon.co.jp/Docker-Kubernetes-%E5%AE%9F%E8%B7%B5%E3%82%B3%E3%83%B3%E3%83%86%E3%83%8A%E9%96%8B%E7%99%BA%E5%85%A5%E9%96%80-%E5%B1%B1%E7%94%B0-%E6%98%8E%E6%86%B2-ebook/dp/B07GP1Q3VT)
