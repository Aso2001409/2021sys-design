```uml
###詳細表示
@startuml
ユーザー -> Webサーバー :詳細表示
Webサーバー -> DBサーバー :詳細検索
DBサーバー -> Webサーバー :検索結果
Webサーバー -> ユーザー :結果表示
@enduml
```
