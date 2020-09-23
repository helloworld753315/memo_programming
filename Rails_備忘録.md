# 用語

- ルーティング → コントローラー →View
- **マイグレーションファイル**　 Ruby で書かれた テーブルの設計図(これを元にテーブルが作られる)

# コマンド

## アプリケーション作成

`rails new アプリケーション名`

## サーバーを建てる

`rails s`

## コントローラー生成

`rails generate controller <コントローラー名> <アクション名>`

## マイグレーションファイル作成

`rails g model モデル名（単数形） カラム名:データ型`

## データベースに反映

`rails db:migrate`

# Rails Console

## 起動と終了

- 起動 rails console

# ファイル置き場所

## ルーティングのファイル

**config** / routes.rb

## コントローラー

app / **controllers** / xx_controller.rb

## View ファイル

app / **view** /コントローラー名 / action.html.erb

## css ファイル

stylesheets 内に入ってる css に書けば全てのビューに css が適用される

app / assets / **stylesheets** / コントローラー名.scss

## 画像

app / **public** / sample.png

```html
<!-- ファイル名の前に/つける  -->

<img src="/sample.png" />
```

# データベース

```Ruby

# モデル名はPost

# インスタンスの作成

post = Post.new(引数)


# 保存

post.save

# 全てのデータ取得

Post.all

#特定のidのデータ取得

post=Post.find_by(id:n)

#データの削除

post.destroy

#バリデーション（不正なデータのチェック）

#検証するカラム:content, 空の投稿を防ぐ

validates :content, {presense: true}

```

# その他

```html
<!-- HTML内にRubyのコードを挿入する時 -->

<!-- ※簡単な繰り返し処理、変数の定義などに使用 -->

<% username=　"佐藤太郎" %>

<!-- 変数の中身を文字列として出力したい場合 -->

<p><%= username %>さん、ようこそ</p>

<!-- こうすると表示されないので注意 -->

<p><% username %>さん、ようこそ</p>
```

```Ruby

#グローバル変数は変数名の前に@をつける

@text="Hello,World"

# aタグの代わり

link_to("テキスト","パス")

#フォームの値を受け取る(nameはname属性の名前)

params[:name]

#ルーティングで設定したURLのid取得

params[:id]

#formのデータ送信(POST)

<%= form_tag("URL", method: :POST) do %>

<% end %>

#他のURLに転送

redirect_to("URL")

```
