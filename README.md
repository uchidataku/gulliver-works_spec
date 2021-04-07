# モックサーバー
NameSpaceごとにモックサーバーを立ててあります。
下記のオリジンをbaseURLにして、各エンドポイントにリクエストを送れば、レスポンスが返ってきます。

## NameSpace
### Application
Origin: 'https://910f8d82-868e-4ac2-981d-af7621255ff8.mock.pstmn.io'
### Enterprise
Origin: 'https://149863f0-f745-4984-aed5-fba036d550d1.mock.pstmn.io'
### Auth
Origin: 'https://1134932e-a443-49eb-8dd6-764a9db8d7bc.mock.pstmn.io'
### EnterpriseAuth
Origin: 'https://78375609-8394-40e4-87c6-770a646d6a2f.mock.pstmn.io'

## Exp
Applicationのエンドポイントで「都道府県一覧一覧を取得する」の場合、
`GET https://910f8d82-868e-4ac2-981d-af7621255ff8.mock.pstmn.io/prefectures`
で以下のレスポンスが返ってくる。

{
    "prefectures": [
        {
            "id": "velit ad id",
            "name": "東京"
        }
    ]
}

## 注意点
実際のエンドポイントの実装では、バージョニングとNameSpaceがあるので、
 - Applicationであれば、`/v1/prefectures` 
 - Enterpriseであれば、`/enterprise/v1/prefectures`
というURIになります。
