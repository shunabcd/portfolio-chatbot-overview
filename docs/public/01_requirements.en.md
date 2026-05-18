# Requirements Overview

[日本語版はこちら](./01_requirements.md)

## Purpose

Portfolio Chatbot demonstrates a production-minded AI chatbot / virtual assistant that can answer questions from user-provided documents with visible supporting sources.

The project emphasizes:

- source-grounded answers
- suppression when evidence is insufficient
- owner-scoped document access
- secure login and session handling
- public deployment readiness

## MVP Scope

- Google OAuth login
- `/chat` for authenticated users
- `/documents` for owner-scoped document registration and management
- Source cards that show the document name, URL, and excerpt used for the answer
- Guardrail behavior when registered documents do not provide enough evidence
- LLM provider switching through an internal adapter boundary
- Public HTTPS deployment

## Public Demo Usage Notes

The document registration feature is intended for public URLs or test URLs that the user has the right to register and use. It is not intended for third-party copyrighted material, personal information, confidential information, access-restricted information, or URLs that violate the source site's terms.

In the public demo, URL fetching targets, file size, fetch time, and usage may be limited to reduce security risk and impact on external sites.

## Future Improvements

The current public demo is an MVP that exposes the minimum practical experience first. The project will continue to improve the following areas based on usage and verification.

- UI/UX and mobile display quality
- Supported document handling and registration flow
- Answer quality and source presentation
- Public deployment monitoring, limits, and operational quality

## Non-Scope

- Full application source code publication
- Detailed administration or operations flows
- Implementation internals

## Quality Goals

- Do not answer beyond available evidence.
- Do not show sources that were not used.
- Do not let one user's documents affect another user's chat.
- Do not guess when a question is outside the registered documents.
- Keep personal or sensitive information out of public documentation and screenshots.
