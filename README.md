## users table
|column|Type|Option|
|------|----|------|
|name  |string|null: false, unique :true|
|email |string|null: false, unique :true|


### association
-has_one :users_info

## users_info table
|column|Type|Option|
|------|----|------|
|nickname|string|null: false, unique :true|
|profile_photo|bynary|
|address_1|text|null: false|
|address_2|text|null: false|
|address_3|text|null: false|
|post_code|integer|null: false|
|phone_number|integer|null: false|
|users_id|reference|null: false, foreign_key: true|


### association 
-belongs_to :user

## producers table
|column|Type|Option|
|------|----|------|
|producer_name|string|null: false, unique :true|
|farm_name|string|null: false, unique :true|
|farm_profile|text|
|farm_phone_number|integer|null: false|
|farm_address_1|text|null: false|
|farm_address_2|text|null: false|
|farm_address_3|text|null: false|
|items_id|reference|null: false, foreign_key: true|

### association
-has_many :items


## items table
|column|Type|Option|
|------|----|------|
|title |text|null: false|
|price |integer|null: false|
|detail|text|null: false|
|discrption|text|null: false|
|prefecture|string|null: false|
|producers_id|reference|null: false, foreign_key: true|
|item_images_id|reference|null: false, foreign_key: true|
|tags_id|reference|null: false, foreign_key: true|

### association
-has_many :tags
-belongs_to :producer
-has_many :item_images

## item_images table
|column|Type|Option|
|------|----|------|
|item_photo |varchar|
|items_id|reference|null: false, foreign_key: true|


### association
-belongs_to :item


## tags table
|column|Type|Option|
|------|----|------|
|rice  |integer|
|onion |integer|
|tomato|integer|
|carrot|integer|
|radish|integer|
|cabbage|integer|
|lettuce|integer|
|spinach|integer|
|eggplant|integer|
|greenpapper|integer|
|mustard_spinach|integer|
|strawberry|integer|
|orange |integer|
|lemon |integer|
|kewi  |integer|
|mandarin_orange|integer|
|sweet_summer|integer|
|peach |integer|
|apple |integer|
|pineapple|integer|
|pear  |integer|
|mango |integer|
<!-- |items_id|reference|null: false, foreign_key: true| -->

### association
-belongs_to :item

