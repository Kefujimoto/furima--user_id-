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
| nickname        | string | null: false |
| mailadress      | string | null: false |
| password        | string | null: false |
| familyname      | string | null: false |
| name            | string | null: false |
| kana_familyname | string | null: false |
| kana_name       | string | null: false |
| birthday        | string | null: false |

### Association

- has_many :items

## items テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| name     | string  | null: false |
| explain  | text    | null: false |
| category | string  | null: false |
| status   | string  | null: false |
| charge   | integer | null: false |
| area     | string  | null: false |
| days     | string  | null: false |
| price    | integer | null: false |

### Association

- belongs_to :users