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
    + customer_code [PK]
    --
    pass
    name
    address
    tel
    mail
    }
}
    
    
    
    
    
