### Tenants Table

| attribute name | type | kind | index | description |
| ------------ | ---------- | ----------- | -------------------- | ---------------------- |
| tenant_id | String | PK | | テナントID |
| kind | String | SK | | テナント情報か各種設定かを表す |
| tenant_name | String | | | テナント名（ブランド名） |
| user_id | String | | | テナント作成者のID |
| contact | Map | | | 連絡先情報 |
| billing_information | Map | | | 請求先情報 |
| shipping_infomation | Map | | | 配送先情報 |

### kind (SK) について

`kind` を `TENANT` としているレコードはテナント名や連絡先情報などテナントの基本情報を持つ。そのテナントに関する詳細な設定は同レコードに記録するのではなく、 `kind` を `SETTINGS#` から始まる文字列とする。

例えば、T-Shirtに関する設定の場合、`kind` を `SETTINGS#TSHIRT#FIT` や `SETTINGS#TSHIRT#FABRIC` のようにして各種設定を記録する。このようにすることで、テナント単位での検索や洋服の種類単位での検索が実現できる。