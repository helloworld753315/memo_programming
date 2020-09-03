
# 用語

- ルーティング→コントローラー→View
- **マイグレーションファイル**　Rubyで書かれた テーブルの設計図


# コマンド

## アプリケーション作成

`rails new アプリケーション名`

## コントローラー生成

`rails generate controller <コントローラー名> <アクション名>`

## マイグレーションファイル作成

`rails g model モデル名（単数形） カラム名:データ型`

## データベースに反映

`rails db:migrate` 

# Rails Console

## 起動と終了

- 起動  rails console

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

```

# その他

```Ruby

# aタグの代わり

link_to("テキスト","パス")

#フォームの値を受け取る(nameはname属性の名前)

params[:name]

#ルーティングで設定したURLのid取得

params[:id]



```





