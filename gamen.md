```uml
@startuml
[*]-->トップページ
トップページ->商品詳細:商品をクリック
トップページ->ログイン画面:ログインをクリック
トップページ->登録画面:会員登録をクリック
トップページ->ショッピングカート:カートをクリック
商品詳細->トップページ:戻るをクリック
商品詳細->ショッピングカート:注文をクリック
ログイン画面->トップページ:ログアウトをクリック
@enduml
```