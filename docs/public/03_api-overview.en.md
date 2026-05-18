# API Overview

[日本語版はこちら](./03_api-overview.md)

Base path:

```text
/api/v1
```

## Auth

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

## Documents

- `POST /me/documents`
- `GET /me/documents`
- `DELETE /me/documents/{document_id}`

## Response Principles

- Auth is required for user data.
- Document APIs are owner-scoped.
- Chat answers include source cards with document name, URL, and excerpt only when evidence supports the answer.
- When registered documents do not provide evidence, the response does not include misleading source cards.
- Public deployment can enforce user/day rate limits.

Detailed schemas, internal model choices, and implementation code are private.
