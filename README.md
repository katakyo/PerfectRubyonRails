Dockerで環境構築しました。Apple siliconを搭載したMacで動かすことを想定しています。
前のリポジトリだとwebpack関連で動かなかったので、Rails7系で作り直しました。

### build
```
docker-compose build
```

### コンテナの起動
```
docker-compose up -d
```

### DB作成
```
docker-compose run app rails db:create
```
### appコンテナに入る
```
docker-compose exec app sh
```

### マイグレーションを実行
```
rails db:migrate
```

localhostに接続
http://localhost:3030/
