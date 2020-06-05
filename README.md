## userテーブル

|Colum|Type|Options|
|-----|----|-------|
|id|intenger|null: false, foreign_key: true|
|name|intenger|null: false, foreign_key: true|

### Association
- belongs_to :users_group
- belongs_to :


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user