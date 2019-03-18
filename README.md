## how2use

1. XAMMP/Composer/node.js(npm) をインストール
1. このリポジトリを適当なディレクトリにダウンロード
1. MariaDBで以下を作成
  1. ユーザーを作成 `CREATE USER test IDENTIFIED BY 'test';`
    1. GRANT で権限を追加する `GRANT ALL ON *.* TO test@'localhost' IDENTIFIED BY 'test';`
  1. todo-app データベースを作成 `CREATE DATABASE todo;`
1. この todo-app があるディレクトリに移動
  1. composer install を実行 `$ composer install`
  1. todo データベースにテーブルを作成 `$ php artisan migrate`
  1. 必要なJavaScriptライブラリをインストール `npm install`
  1. npm でフロントをビルド `npm run development`
1. todo-app を起動
  1. アプリケーションを起動 `php artisan serve`
  1. http://localhost:8000 にアクセス