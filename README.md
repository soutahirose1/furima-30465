# REAADM

## users table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| nickname           | string              | null: false             |
| email              | string              | null: false ,unique: true|
| password           | string              | null: false             |
| identification     | string              | null: false             |
| birthday 　　       | string              | null: false             |

### Association

- has_many :items
- has_many :purchases


## items table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| product image      | string               | null: false             |
| product            | string              | null: false             |
| product description| text                | null: false             |
| category           | string              | null: false             |
| product status     | string              | null: false             |
| price 　　　　      | integer             | null: false             |

### Association

- belongs_to :users
- has_hmany :purchases

##　purchases table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| delivery charge    | nteger              | null: false             |
| area               | string              | null: false             |
| days               | date                | null: false             |


### Association

- belongs_to :users
- belongs_to :purchases