カートの中身表示
```uml
@startuml
ユーザー -> Webサーバー :カートの中表示
Webサーバー -> DBサーバー :カートの中身検索
DBサーバー - Webサーバー :検索結果

alt 条件分岐
  hoge -> bar
  bar -> hoge
else elseの処理
  hoge -> fuga
  fuga -> hoge
end
@enduml
```
