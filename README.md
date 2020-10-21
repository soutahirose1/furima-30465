# DB設計

## ユーザーテーブル

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| nickname           | string              | null: false             |
| email              | string              | null: false             |
| password           | string              | null: false             |
| password(確認)      | string              | null: false             |
| 本人確認（漢字）      | string              | null: false             |
| 本人確認（カナ）      | string              | null: false             |
| 生年月日　　　　      | string              | null: false             |

### Association

- has_many :商品
- has_many :購入・配送


## 商品テーブル

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| 出品画像            | string               | null: false             |
| 商品名              | string              | null: false             |
| 商品の説明           | text                | null: false             |
| 商品の詳細（カテゴリ） | string              | null: false             |
| 商品の詳細（商品の状態)| string              | null: false             |
| 販売価格　　　　      | integer             | null: false             |

### Association

- belongs_to :ユーザー
- has_hmany :購入・配送

## 購入・配送テーブル

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| 配送料の負担         | nteger              | null: false             |
| 配送元の地域         | string              | null: false             |
| 配送までの日数       | date                | null: false             |


### Association

- belongs_to :ユーザー
- belongs_to :商品