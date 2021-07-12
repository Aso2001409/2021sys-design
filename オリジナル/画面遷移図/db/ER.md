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
        + 顧客ID [PK]
        --
        パスワード
        名前
        住所
        電話
        メール
    }
    
    entity "商品マスタ" as items <<M,MASTER_MARK_COLOR>>{
        + 商品ID　[PK]
        --
        カテゴリーID 
        商品名
        値段
        画像
    }
}
    
    
    
    
    
