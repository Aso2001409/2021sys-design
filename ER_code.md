```uml
@startuml


!define MASTER_MARK_COLOR AAFFAA
!define TRANSACTION_MARK_COLOR FFAA00

entity "顧客マスタ" as customer <m_customers>
<<M,MASTER_MARK_COLOR>>{
+ custoner_code[PK]
--
item_code
pass
name
address
tel
mail
del_flag
reg_date
}




@enduml
```
