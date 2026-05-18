# UI Overview

[日本語版はこちら](./04_ui-overview.md)

## Public Demo Screens

- `/login`
- `/chat`
- `/documents`
- `/403`

## Login

The login screen uses Google OAuth as the main path. Valid sessions route users to the chat experience.

## Chat

The chat screen includes:

- conversation list
- message thread
- answer model selector
- input form
- source cards with document name, URL, and excerpt
- unsupported-answer message
- retry/error state

Source cards are intended to represent document information actually used by the answer, not a post-hoc guess. When evidence is insufficient, the Chat screen shows an unsupported-answer message without source cards.

## Documents

The documents screen lets a logged-in user manage their own documents.

Expected actions:

- register document
- list document status
- delete document with confirmation

Documents are tied to the user who registered them.

Registered documents are used only as answer candidates for that user's own Chat flow. They do not affect other users' Chat results.

## Admin

Admin and operations paths are not part of the public portfolio demo.
