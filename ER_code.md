'''puml
@startuml


entity "employee" {    
    + id [PK]   
    ==
    # company_id [FK(company,id)]    
    name:varchar(128)
}


@enduml
'''
