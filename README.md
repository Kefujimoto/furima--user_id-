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
- has_many :items, through: :orders
- has_one :adress

## items テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| name     | string   | null: false |
| explain  | text     | null: false |
| category | integer  | null: false |
| status   | integer  | null: false |
| charge   | integer  | null: false |
| area     | integer  | null: false |
| days     | integer  | null: false |
| price    | integer  | null: false |

### Association

- has_many :orders
- has_many :user, through: :orders

## orders テーブル
| user_id  | integer | null: false |
| items_id | integer | null: false |

### Association

-  belongs_to :user
-  belongs_to :item 

## adresses テーブル
| user_adress | string | null: false |

### Association

- has_one :user
