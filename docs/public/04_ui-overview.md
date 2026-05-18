# UI概要

[English](./04_ui-overview.en.md)

## 公開デモ画面

- `/login`
- `/chat`
- `/documents`
- `/403`

## Login

Login画面ではGoogle OAuthを主導線にします。有効なsessionがある場合はchat画面へ進みます。

## Chat

Chat画面には次を含めます。

- conversation list
- message thread
- answer model selector
- input form
- 文書名、URL、抜粋を含む出典カード表示
- unsupported answer（根拠不足時の回答）メッセージ
- retry/error state

出典カードは、後付けの推定ではなく、回答の根拠として使った文書情報を表すためのものです。根拠が不足する場合、Chat画面は出典カードを表示せず、根拠不足時の回答を表示します。

## ドキュメント

ドキュメント画面では、ログインユーザーが自分の文書を管理できます。

想定操作:

- 文書登録
- 文書statusの一覧表示
- 確認付きの文書削除

文書は登録したユーザー本人に紐づきます。

登録された文書は、そのユーザー自身のChat回答候補として使われます。他ユーザーのChatには影響しません。

## Admin

Adminと運用系pathは、公開ポートフォリオデモの対象外です。
