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
|name|string|null: false|
|mail|string|null: false,|
|password|string|null: false|

### Association
- has_many :groups,through: :groups_users
- has_many :messeages
- has_many :groups_users


## groupsテーブル

|Column|Type|Options|
|name|string|null: false,|

### Association
- has_many :user,through: :groups_users
- has_many :messeages
- has_many :groups_users

## messeageテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|text|text||
|image|text||

### Association
- belongs_to :group
- belongs_to :user


