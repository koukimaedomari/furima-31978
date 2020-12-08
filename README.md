## usersテーブル

| Column          | Type   | Options     |
| --------------- | ------ | ----------- |
| name            | string | null: false |
| email           | string | null: false |
| password        | string | null: false |
| last_name       | string | null: false |
| first_name      | string | null: false |
| kana_last_name  | string | null: false |
| kana_first_name | string | null: false |
| birth_year      | string | null: false |
| birth_month     | string | null: false |
| birth_day       | string | null: false |

- has_many :items
- has_many :buys

## itemsテーブル

| Column     | Type      | Options     |
| ---------- | ------    | ----------- |
| image      | reference |             |
| item_name  | string    | null: false |
| item_text  | text      | null: false |
| seller     | reference |             |
| category   | string    | null: false |
| status     | string    | null: false |
| postage    | string    | null: false |
| area       | string    | null: false |
| day        | string    | null: false |
| price      | integer   | null: false |

- belongs_to :users
- has_one :buy

## buysテーブル

| Column     | Type      | Options     |
| ---------- | --------- | ----------- |
| users      | reference |             | 
| items      | reference |             |

- belongs_to :item
- belongs_to :residence

## residencesテーブル

| Column           | Type   | Options     |
| ---------------- | ------ | ----------- |
| post_number      | string | null: false |
| city             | string | null: false |
| address          | string | null: false |
| build_name       | string |             |
| telephone_number | string | null: false |
| prefectures      | string | null: false |

has_one :buy