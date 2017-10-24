# PhoenixでWebアプリの作成課題(2)

## 参照テキスト

- [Elixir入門「第3回：Phoenix 1.3で高速webアプリ ＆ REST APIアプリをサクッと書いてみる」](
  https://www.slideshare.net/piacere_ex/elixir3phoenix-13web-rest-api-81099953)
  - 2017/10/10 ver1.3 (Phoenix 1.3対応)

## 実行方法

- 下記のコマンドを実行後にブラウザで「http://localhost:4000」を表示
```
$ cd app
$ iex -S mix phx.server
```

## 作成手順

- 下記のコマンドを実行後にブラウザで動作確認
```
# apt-get update
# apt-get install postgresql
# /etc/init.d/postgresql start
# sudo -u postgres psql
postgres=# \q

# git clone https://github.com/creationix/nvm.git ~/.nvm
# source ~/.nvm/nvm.sh
# nvm install v4.2.6
# apt-get install npm

# mix phx.new app --no-brunch
# cd app
# sudo -u postgres psql -c "ALTER USER postgres PASSWORD 'postgres';"
# sudo service postgresql restart

# mix ecto.create
# sudo -u postgres psql -l

# mix phx.gen.html Tool Post posts title:string body:text
※ テキストエディタで「lib/app_web/router.ex)にパスを追加
# mix ecto.migrate

# sudo -u postgres psql
postgres=# \c app_dev
postgres=# \d posts
postgres=# \q

# iex -S mix phx.server
```

## 動作確認

- ブラウザで「http://localhost:4000/posts」を表示して下記を実行
  - New post: 新規登録
  - Show: 詳細表示
  - Edit: 修正
  - Delete: 削除
