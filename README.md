## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :groups
- has_many :messages


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|user_id|integer|null: false|
### Association
- belongs_to :groups
- has_many :messages


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|text|text||
|user_id|integer|null: false|
|group_id|integer|null: false|
### Association
- belongs_to :users
- belongs_to :groups


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user