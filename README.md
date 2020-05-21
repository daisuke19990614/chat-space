# README

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## userテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, foreign_key: true|
|mail|string|null: false,|
|password|string|null: false|

### Association
- has_many :group,through:members
- has_many :messeage
- has_many :members

## groupsテーブル

|Column|Type|Options|
|user_id|integer|null: false, foreign_key: true|
|groupsname|integer|null: false,|

### Association
- belongs_to :user
- has_many :messeage

## messeageテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|text|text|null: false|

### Association
- belongs_to :group
- belongs_to :user


