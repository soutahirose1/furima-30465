

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
| category           | string              | null: false             |
| product status     | string              | null: false             |
| price 　　　　      | integer             | null: false             |
| delivery charge    | integer             | null: false             |
| area               | integer             | null: false             |
| days               | integer             | null: false             |

### Association

- belongs_to:users
- has_one:purchase records

##　purchase records table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| who                | string              | null: false             |
| when               | string              | null: false             |
| buys               | string              | null: false             |


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