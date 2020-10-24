

# REAADM

## users_table

| Column                  | Type                | Options                 |
|--------------------     |---------------------|-------------------------|
| nickname                | string              | null: false             |
| sex_Chinese characters  | string              | null: false             |
| name_Chinese characters | string              | null: false             |
| sex_furigana            | string              | null: false             |
| name_furigana           | string              | null: false             |
| email                   | string              | null: false ,unique: true|
| password                | string              | null: false             |
| birthday 　　            | date                | null: false             |

### Association

- has_many:items
- has_many:purchse records


## items_table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| product            | string              | null: false             |
| product_description| text                | null: false             |
| category_id        | integer             | null: false             |
| product status_id  | integer             | null: false             |
| price    　　　     | integer             | null: false             |
| delivery charge_id | integer             | null: false             |
| area_id            | integer             | null: false             |
| days_id            | integer             | null: false             |

### Association

- belongs_to:users
- has_one:purchase records

##　purchase_records_table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| user_id            | string              | foreign_key: true       |
| item_id            | string              | foreign_key: true       |


### Association

- belongs_to:users
- belongs_to:items
- has_one:street adress


##　street_adress_table

| Column             | Type                | Options                 |
|--------------------|---------------------|-------------------------|
| postal_code        | string              | null: false             |
| prefectures        | string              | null: false             |
| municipality       | string              | null: false             |
| address            | string              | null: false             |
| builing_name       | string              |                         |
| phone_number       | string              | null: false             |


### Association

- belongs_to:purchase_records