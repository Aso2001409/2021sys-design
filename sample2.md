ログイン
```uml
@startuml


alt ログイン時
ユーザー -> Webサーバー :詳細表示
Webサーバー -> DBサーバー :詳細検索
DBサーバー -> Webサーバー :検索結果
Webサーバー -> ユーザー :結果表示
else 未ログイン
ユーザー -> Webサーバー :ログイン
Webサーバー -> DBサーバー :ログイン情報検索
DBサーバー -> DBサーバー :会員情報検索

end
@enduml
```
