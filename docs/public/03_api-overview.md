# API概要

[English](./03_api-overview.en.md)

Base path:

```text
/api/v1
```

## 認証

- `GET /auth/google/authorize-url`
- `POST /auth/google/exchange`
- `GET /auth/session`
- `POST /auth/logout`

## Chat

- `POST /chat/messages`
- `GET /chat/model-options`
- `GET /chat/sessions`
- `GET /chat/sessions/{session_id}/messages`
- `DELETE /chat/sessions/{session_id}`

## ドキュメント

- `POST /me/documents`
- `GET /me/documents`
- `DELETE /me/documents/{document_id}`

## Response原則

- ユーザーデータには認証を必須にする。
- ドキュメントAPIはログインユーザー本人の文書だけを扱う。
- Chat回答は、根拠がある場合だけ文書名、URL、抜粋を含む出典カードを返す。
- 登録文書に根拠がない場合は、誤解を招く出典カードを返さない。
- 公開環境ではuser/dayの利用制限を適用できる。

詳細schema、内部model選択、実装codeは非公開です。
