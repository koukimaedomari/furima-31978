## usersテーブル

| Column          | Type   | Options     |
| --------------- | ------ | ----------- |
| name            | string | null: false |
| email           | string | null: false |
| password        | string | null: false |
| last_name       | string | null: false |
| first_name      | string | null: false |
| kana_last_name  | string | null: false |
| kana_first_name | string | null: fasle |

- has_many :items
- has_many :buys

## itemsテーブル

| Column     | Type      | Options     |
| ---------- | ------    | ----------- |
| image      | reference |             |
| item_name  | string    | null: false |
| item_text  | text      | null: false |
| price      | integer   | null: false |
| seller     | reference |             |

- belongs_to :users
- has_one :buy

## buysテーブル

| Column     | Type      | Options     |
| ---------- | ------    | ----------- |
| image      | reference |             |
| item_name  | reference |             |

- belongs_to :item
- belongs_to :residence

## residencesテーブル

| Column           | Type   | Options     |
| ---------------- | ------ | ----------- |
| post_number      | string | null: false |
| city             | string | null: false |
| address          | string | null: false |
| build_name       | string | null: false |
| telephone_number | string | null: false |

has_one :buy