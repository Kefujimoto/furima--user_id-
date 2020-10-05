# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
＃テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nickname        | string  | null: false |
| mailadress      | string  | null: false |
| password        | string  | null: false |
| familyname      | string  | null: false |
| name            | string  | null: false |
| kana_familyname | string  | null: false |
| kana_name       | string  | null: false |
| birthday        | date    | null: false |

### Association

- has_many :orders
- has_many :items
- has_one :adress

## items テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
<<<<<<< Updated upstream
| name     | string     | null: false      |
| explain  | text       | null: false      |
| category | integer    | null: false      |
| status   | integer    | null: false      |
| charge   | integer    | null: false      |
| area     | integer    | null: false      |
| days     | integer    | null: false      |
| price    | integer    | null: false      |
| user     | references | foreign_key: true|

### Association

- has_one :orders
=======
| name        | string   | null: false |
| explain     | text     | null: false |
| category_id | integer  | null: false |
| status_id   | integer  | null: false |
| charge_id   | integer  | null: false |
| area_id     | integer  | null: false |
| days_id     | integer  | null: false |
| price       | integer  | null: false |

### Association

- has_one :order
>>>>>>> Stashed changes
- has_one :user

## orders テーブル
| user_id  | integer | null: false |
| items_id | integer | null: false |

### Association

-  belongs_to :user
-  belongs_to :item 

## adresses テーブル
| post_number   | integer | null: false |
| live_area     | string  | null: false |
| live_city     | string  | null: false |
| city_number   | integer | null: false |
| building_name | string  | null: false |
| phone_number  | integer | null: false |

### Association

- has_one :user
