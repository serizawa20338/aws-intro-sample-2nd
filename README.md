# Ruby on Rails チュートリアルのサンプルアプリケーション

https://github.com/nakaken0629/aws-intro-sample-2nd を勉強会用に編集したもの。

```
$ rbenv install 2.6.6
$ gem install bundler -v 1.17.3
$ sudo apt-get install libmysqlclient-dev libxml2-dev libcurl4-openssl-dev
$ bundle install --with production
$ docker compose up -d
$ export RACK_ENV=development
$ bundle exec rails db:migrate
$ bundle exec rails server
```

http://localhost:3000/

## 書籍との変更点

- `rails` コマンドを実行する際は `bundle exec rails ~` にする（`bundle exec rails server` など）
- DBのURLは環境変数 `AWS_INTRO_SAMPLE_DATABASE_HOST` で設定する
- メールは使用しないので、メール関連の環境変数 `AWS_INTRO_SAMPLE_SMTP_*` は設定しない

---

これは、次の教材で作られたサンプルアプリケーションです。   
[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
[Michael Hartl](http://www.michaelhartl.com/) 著

## ライセンス

[Ruby on Rails チュートリアル](https://railstutorial.jp/)内にある
ソースコードはMITライセンスとBeerwareライセンスのもとで公開されています。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

## 使い方

このアプリケーションを動かす場合は、まずはリポジトリを手元にクローンしてください。
その後、次のコマンドで必要になる RubyGems をインストールします。

```
$ bundle install --without production
```

その後、データベースへのマイグレーションを実行します。

```
$ rails db:migrate
```

最後に、テストを実行してうまく動いているかどうか確認してください。

```
$ rails test
```

テストが無事に通ったら、Railsサーバーを立ち上げる準備が整っているはずです。

```
$ rails server
```

詳しくは、[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
を参考にしてください。
