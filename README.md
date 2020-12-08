## usersテーブル

| Column          | Type   | Options     |
| --------------- | ------ | ----------- |
| name            | string | null: false |
| email           | string | null: false |
| password        | string | null: false |
| last_name       | text   | null: false |
| first_name      | text   | null: false |
| kana_last_name  | text   | null: false |
| kana_first_name |

- has_many :items
- has_many :buys

## itemsテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| image      | string | null: false |
| item_name  | string | null: false |
| item_text  | string | null: false |
| price      | text   | null: false |
| seller     | text   | null: false |

- belongs_to :users
- has_one :buy

## buysテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| image      | string | null: false |
| item_name  | string | null: false |

- belongs_to :item
- belongs_to :residence

## residencesテーブル

| Column           | Type   | Options     |
| ---------------- | ------ | ----------- |
| post_number      | string | null: false |
| city             | string | null: false |
| address          | string | null: false |
| build_name       | text   | null: false |
| telephone_number | text   | null: false |

has_one :buy