# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001409/2021sys-design/blob/main/%E3%82%AA%E3%83%AA%E3%82%B8%E3%83%8A%E3%83%AB/%E7%94%BB%E9%9D%A2%E9%81%B7%E7%A7%BB%E5%9B%B3/db/ER.md "ER図はこちら")

# DBテーブルカラム一覧詳細

#### 購入テーブル
|和名   |属性名(カラム名)|型     |PK   |NN     |FK      |
|:------|:--------------|:------|:----|:-----:|:------:|
|注文ID |order_id       |varchar(50)|〇|〇     |-       |
|顧客ID |customer_id|varchar(50)|-    |〇      |-       |
|注文日 |purchase_date|date     |-    |〇      |-       |
|総額   |total_price|int(10)    |-    |〇      |-       |



#### 購入詳細テーブル
|和名   |属性名(カラム名)|型     |PK   |NN     |FK      |
|:------|:--------------|:------|:----|:-----:|:------:|
|注文ID |order_id       |varchar(50)|〇|〇    |〇       |
|詳細ID |detail_id      |varchar(50)|〇|〇    |-        |
|商品ID |items_id       |varchar(50)|- |〇    |〇       |
|値段   |price          |int(10) |-    |〇    |         |
|個数   |num            |int(10) |-    |〇    |-        |

#### 顧客マスタ
|和名   |属性名(カラム名)|型     |PK   |NN     |FK      |
|:------|:--------------|:------|:----|:-----:|:------:|
|顧客ID|customer_code|varchar(20)|〇   |〇     |-      |
|パスワード|pass     |varchar(20)|-    |〇     |-      |
|名前   |name   |varchar(50)    |-    |〇     |-       |
|住所   |address　　|varchar(100)   |〇  |-    |-     |
|電話   |tel         |varchar(20)|-   |〇      |-      |
|メール |mail       |varchar(100)|-   |〇      |-      |
|削除フラグ|del_flag|int(1)     |-    |-       |-      |
|更新日 |reg_date   |date       |-    |〇      |-      |



#### カテゴリマスタ
|和名   |属性名(カラム名)|型     |PK   |NN     |FK      |
|:------|:--------------|:------|:----|:-----:|:------:|
|カテゴリーID|category_id|varchar(50)|〇 |〇   |-       |
|カテゴリ名|category_name|varchar(50)|-   |〇 |-        |
|更新日 |reg_date       |date    |-    |〇      |-       |



#### 商品マスタ
|和名   |属性名(カラム名)|型     |PK   |NN     |FK      |
|:------|:--------------|:------|:----|:-----:|:------:|
|商品コード|items_id|varchar(50)|〇   |〇     |-        |
|商品名 |item_name  |varchar(50)|-    |〇     |-        |
|値段   |price      |int(10)    |-    |〇     |-        |
|カテゴリーID|category_id|varchar(50)|-|〇    |〇　　　　|
|画像   |image　　　|varchar(200)|-   |-      |-         |
|商品詳細|deteil    |varchar(500)|-   |-      |-         |
|削除フラグ|del_flag|int(1)      |-     |-    |-         |
|更新日 |reg_date   |date        |-   |〇     |-          |
   

