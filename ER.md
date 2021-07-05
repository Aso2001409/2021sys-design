
'''startuml
@startuml

package "外部データベース" as ext <<Database>> {
    Class "顧客マスタ" as customer <<M,AAFFAA)>> {
       +顧客ID [PK]
        ---
        顧客名
        郵便番号
        住所
        電話番号
        FAX
    }
}

package "開発対象システム" as target_system {
    /'
      マスターテーブルを M、トランザクションを T などと安直にしていますが、
      チーム内でルールを決めればなんでも良いと思います。交差テーブルは "I" とか。
      角丸四角形が描けない代替です。
      １文字なら "主" とか "従" とか日本語でも OK だったのが受ける。
     '/
    Class "注文テーブル" as order <<主,FFAA00)>> {
       +注文ID [PK]
        ---
       #顧客ID [FK]
        注文日時
        配送希望日
        配送方法
        お届け先名
        お届け先住所
        決済方法
        合計金額
        消費税額
    }

    Class "注文明細テーブル" as order_detail <<T,FFAA00)>> {
       +注文ID   [PK]
       +明細番号 [PK]
        ---
       #SKU [FK]
        注文数
        税抜価格
        税込価格
    }

    Class "SKUマスタ" as sku <<M,AAFFAA)>> {
       +SKU [PK]
        ---
       #商品ID [FK]
        カラー
        サイズ
        重量
        販売単価
        仕入単価
    }

    Class "商品マスタ" as product <<M,AAFFAA)>> {
       +商品ID [PK]
        ---
        商品名
        原産国
       #仕入先ID [FK]
        商品カテゴリ
        配送必要日数
    }

    Class "仕入先マスタ" as vendor <<M,AAFFAA)>> {
       +仕入先ID [PK]
        ---
        仕入れ先名
        郵便番号
        住所
        電話番号
        FAX番号
    }
}

customer      "0,1"--ri--"0..*"     order
order           "1"--ri--"1..*"     order_detail
order_detail    "*" -do- "1"        sku
sku             "*"--le--"1"        product
product      "0..*"--le--"1"        vendor


@enduml
'''
