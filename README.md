## userテーブル

|Colum|Type|Options|
|-----|----|-------|
|id|intenger|null: false, foreign_key: true|
|name|intenger|null: false, foreign_key: true|

### Association
- belongs_to :users_group
- belongs_to :


## Messageテーブル

|Colum|Type|Options|
|-----|----|-------|
|id|intenger|null: false, foreign_key: true|
|body|text|null:false, foreign_key: true|
|image|string|
|user_id|intenger|null: false, foreign: true|
|group_id|intenger|


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user