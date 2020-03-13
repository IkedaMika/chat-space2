# README
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false,unique: true|
### Association
- has_many :group
- has_many :messege
- has_many groups through: :group_users

## messegeテーブル
|Column|Type|Options|
|------|----|-------|
|use_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|
|body|text|
|image|tring|
### Association
- belongs_to user
- belongs_to group

## group_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association
- has_many :users, throught: :group_users
- has_many :masseges
- has_mamy :mambers



