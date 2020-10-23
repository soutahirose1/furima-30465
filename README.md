

# REAADM

## users table

| Column                  | Type                | Options                 |
|--------------------     |---------------------|-------------------------|
| nickname                | string              | null: false             |
| sex (Chinese characters)| string              | null: false             |
| name(Chinese characters)| string              | null: false             |
| sex (furigana)          | string              | null: false             |
| name (furigana)         | string              | null: false             |
| email                   | string              | null: false ,unique: true|
| password                | string              | null: false             |
| birthday 　　            | data                | null: false             |

### Association

- has_many:items
- has_many:purchse records


## items table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| product            | string              | null: false             |
| product description| text                | null: false             |
| category_id        | integer             | null: false             |
| product status_id  | integer             | null: false             |
| price_id 　　　     | integer             | null: false             |
| delivery charge_id | integer             | null: false             |
| area_id            | integer             | null: false             |
| days_id            | integer             | null: false             |

### Association

- belongs_to:users
- has_one:purchase records

##　purchase records table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| user_id            | string              | null: false             |
| item_id            | string              | null: false             |


### Association

- belongs_to:users
- belongs_to:items
- has_one:street adress


##　street adress table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| postal code        | string              | null: false             |
| prefectures        | string              | null: false             |
| municipality       | string              | null: false             |
| address            | string              | null: false             |
| builing name       | string              | null: false             |
| phone number       | string              | null: false             |


### Association

- belongs_to:purchase records