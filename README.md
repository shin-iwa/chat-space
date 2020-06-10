## usersテーブル

|Colum|Type|Options|
|-----|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :messages
- has_many :groups through: :user_groups
- has_many :user_groups

## messagesテーブル

|Colum|Type|Options|
|-----|----|-------|
|body|text|null:false|
|image|string|
|user_id|intenger|null: false, foreign_key: true|
|group_id|intenger|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false|

### Association
- has_many :messages
- has_many :users through: :user_groups
- has_many :user_groups

## users_groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
