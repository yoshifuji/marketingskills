# Resend （日本語訳：再送信）

Developer-friendly transactional email service with modern API. （日本語訳：最新の API を使用した開発者向けのトランザクション電子メール サービス。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Simple REST API for sending emails（日本語訳：メール送信用のシンプルなREST API） |
| MCP（日本語訳：MCP） | ✓ | Available via Resend MCP server（日本語訳：再送信 MCP サーバー経由で利用可能） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | Official SDKs for Node.js, Python, Go, etc.（日本語訳：Node.js、Python、Go などの公式 SDK） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: API Keys section in Resend dashboard （日本語訳：**キーの取得**: 再送信ダッシュボードの API キー セクション）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Send email （日本語訳：電子メールを送信する）

```bash
POST https://api.resend.com/emails

{
  "from": "hello@example.com",
  "to": ["user@example.com"],
  "subject": "Welcome!",
  "html": "<h1>Welcome to our app!</h1>"
}
```

### Send with React template （日本語訳：React テンプレートで送信）

```bash
POST https://api.resend.com/emails

{
  "from": "hello@example.com",
  "to": ["user@example.com"],
  "subject": "Welcome!",
  "react": "WelcomeEmail",
  "props": {
    "name": "John"
  }
}
```

### Get email status （日本語訳：電子メールのステータスを取得する）

```bash
GET https://api.resend.com/emails/{email_id}
```

### List emails （日本語訳：メールの一覧表示）

```bash
GET https://api.resend.com/emails
```

### Send batch emails （日本語訳：バッチメールを送信する）

```bash
POST https://api.resend.com/emails/batch

[
  {
    "from": "hello@example.com",
    "to": ["user1@example.com"],
    "subject": "Welcome User 1"
  },
  {
    "from": "hello@example.com",
    "to": ["user2@example.com"],
    "subject": "Welcome User 2"
  }
]
```

### List domains （日本語訳：ドメインのリスト）

```bash
GET https://api.resend.com/domains
```

### Verify domain （日本語訳：ドメインの検証）

```bash
POST https://api.resend.com/domains/{domain_id}/verify
```

## Node.js SDK （日本語訳：Node.js SDK）

### Install （日本語訳：インストール）

```bash
npm install resend
```

### Usage （日本語訳：使用法）

```typescript
import { Resend } from 'resend';

const resend = new Resend('re_xxx');

await resend.emails.send({
  from: 'hello@example.com',
  to: 'user@example.com',
  subject: 'Welcome!',
  html: '<h1>Welcome!</h1>'
});
```

### With React Email （日本語訳：反応メールの場合）

```typescript
import { WelcomeEmail } from './emails/welcome';

await resend.emails.send({
  from: 'hello@example.com',
  to: 'user@example.com',
  subject: 'Welcome!',
  react: WelcomeEmail({ name: 'John' })
});
```

## Email Statuses （日本語訳：電子メールのステータス）

- `queued` - Email queued for delivery （日本語訳：`queued` - 電子メールが配信待ちにされました）
- `sent` - Email sent to recipient server （日本語訳：`sent` - 受信者サーバーに送信された電子メール）
- `delivered` - Email delivered （日本語訳：`delivered` - 電子メールが配信されました）
- `opened` - Email opened (if tracking enabled) （日本語訳：`opened` - 電子メールが開かれました (追跡が有効な場合)）
- `clicked` - Link clicked (if tracking enabled) （日本語訳：`clicked` - リンクがクリックされました (追跡が有効な場合)）
- `bounced` - Email bounced （日本語訳：`bounced` - 電子メールが返送されました）
- `complained` - Marked as spam （日本語訳：`complained` - スパムとしてマークされています）

## Webhook Events （日本語訳：Webhook イベント）

| Event（日本語訳：イベント） | When（日本語訳：いつ） |
|-------|------|
| `email.sent`（日本語訳：__コード0__） | Email sent（日本語訳：メールを送信しました） |
| `email.delivered`（日本語訳：__コード0__） | Email delivered（日本語訳：メール配信） |
| `email.opened`（日本語訳：__コード0__） | Email opened（日本語訳：メールを開封しました） |
| `email.clicked`（日本語訳：__コード0__） | Link clicked（日本語訳：リンクがクリックされました） |
| `email.bounced`（日本語訳：__コード0__） | Email bounced（日本語訳：電子メールが返送されました） |
| `email.complained`（日本語訳：__コード0__） | Spam complaint（日本語訳：スパムに関する苦情） |

## When to Use （日本語訳：いつ使用するか）

- Sending transactional emails （日本語訳：トランザクションメールの送信）
- Welcome emails, password resets （日本語訳：ウェルカムメール、パスワードのリセット）
- Receipt and notification emails （日本語訳：受信および通知メール）
- Developer-friendly email integration （日本語訳：開発者向けの電子メール統合）
- React-based email templates （日本語訳：Reactベースのメールテンプレート）

## Rate Limits （日本語訳：レート制限）

- Free: 100 emails/day, 3,000/month （日本語訳：無料: 100 メール/日、3,000 メール/月）
- Pro: 100 emails/second （日本語訳：プロ: 100 メール/秒）
- Higher limits on scale plans （日本語訳：スケール プランの上限の引き上げ）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- onboarding-cro （日本語訳：オンボーディングクロ）
