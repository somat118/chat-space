# README

## users テーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|string|null: false|
|email|string|null, false|
|password|integer||

### Association
- has_many:groups,through:member
- has_many:messages
- has_many:members

## groups table
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null:false foreign_key: true|
|group_name|string||
|group_member|string||

Association
- has_many:users

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## message table
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|group_id|integer|foreign_key: true|
|users_id|integer|foreign_key: true|

### Association
- belongs_to: user


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
