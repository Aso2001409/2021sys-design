カートの中身表示
```uml
@startuml


alt 条件分岐
ユーザー -> Webサーバー :詳細表示
Webサーバー -> DBサーバー :詳細検索
DBサーバー -> Webサーバー :検索結果
Webサーバー -> ユーザー :結果表示
else elseの処理

end
@enduml
```
