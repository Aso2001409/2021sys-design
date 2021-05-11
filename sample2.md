カートの中身表示
```uml
@startuml


alt ログイン時
ebサーバー -> ユーザー :カート中身表示

else 未ログイン
Webサーバー -> ユーザー :メッセージを表示

end
@enduml
```
