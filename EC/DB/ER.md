```uml
@startuml


!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

skinparam class {
    BackgroundColor Snow
    BorderColor Black
    ArrowColor Black
}

package "ショッピングサイト" as terget_system {
    entity "顧客マスタ" as customer <<M,MASTER_MARK_COLOR>>{
        + customer_id [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
    }
    
    entity "商品マスタ" as items <<M,MASTER_MARK_COLOR>>{
        + items_id　[PK]
        --
        # category_id [FK]
        item_name
        price
        image
        detail
        del_flag
        reg_date
    }
    
    entity "カテゴリマスタ" as category <<M,MASTER_MARK_COLOR>>{
        + category_id [PK]
        --
        category_name
        reg_date
    }
    
    entity "購入テーブル" as purchase <<T,TRANSACTION_MARK_COLOR>>{
        + order_id [PK]
        --
       #  customer_id [FK]
        purchase_deta
        total_price
    }
    
    entity "購入詳細テーブル" as purchase_detail <<T,TRANSACTION_MARK_COLOR>>{
        + detail_id [PK]
        + order_id [PK]
        --
        # items_id [FF]
        price
        num
    }
}
    
customer |o-o{  purchase
purchase ||-|{ purchase_detail
purchase_detail }--|| items
category ||-o{ items

@enduml
```
