# Resend （再送信）

Developer-friendly transactional email service with modern API. （最新の API を使用した開発者向けのトランザクション電子メール サービス。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Simple REST API for sending emails（メール送信用のシンプルなREST API） |
| MCP（MCP） | ✓ | Available via Resend MCP server（再送信 MCP サーバー経由で利用可能） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | Official SDKs for Node.js, Python, Go, etc.（Node.js、Python、Go などの公式 SDK） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: API Keys section in Resend dashboard （**キーの取得**: 再送信ダッシュボードの API キー セクション）

## Common Agent Operations （エージェントの共通操作）

### Send email （電子メールを送信する）

```bash
POST https://api.resend.com/emails

{
  "from": "hello@example.com",
  "to": ["user@example.com"],
  "subject": "Welcome!",
  "html": "<h1>Welcome to our app!</h1>"
}
```

### Send with React template （React テンプレートで送信）

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

### Get email status （電子メールのステータスを取得する）

```bash
GET https://api.resend.com/emails/{email_id}
```

### List emails （メールの一覧表示）

```bash
GET https://api.resend.com/emails
```

### Send batch emails （バッチメールを送信する）

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

### List domains （ドメインのリスト）

```bash
GET https://api.resend.com/domains
```

### Verify domain （ドメインの検証）

```bash
POST https://api.resend.com/domains/{domain_id}/verify
```

## Node.js SDK （Node.js SDK）

### Install （インストール）

```bash
npm install resend
```

### Usage （使用法）

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

### With React Email （反応メールの場合）

```typescript
import { WelcomeEmail } from './emails/welcome';

await resend.emails.send({
  from: 'hello@example.com',
  to: 'user@example.com',
  subject: 'Welcome!',
  react: WelcomeEmail({ name: 'John' })
});
```

## Email Statuses （電子メールのステータス）

- `queued` - Email queued for delivery （`queued` - 電子メールが配信待ちにされました）
- `sent` - Email sent to recipient server （`sent` - 受信者サーバーに送信された電子メール）
- `delivered` - Email delivered （`delivered` - 電子メールが配信されました）
- `opened` - Email opened (if tracking enabled) （`opened` - 電子メールが開かれました (追跡が有効な場合)）
- `clicked` - Link clicked (if tracking enabled) （`clicked` - リンクがクリックされました (追跡が有効な場合)）
- `bounced` - Email bounced （`bounced` - 電子メールが返送されました）
- `complained` - Marked as spam （`complained` - スパムとしてマークされています）

## Webhook Events （Webhook イベント）

| Event（イベント） | When（いつ） |
|-------|------|
| `email.sent`（__コード0__） | Email sent（メールを送信しました） |
| `email.delivered`（__コード0__） | Email delivered（メール配信） |
| `email.opened`（__コード0__） | Email opened（メールを開封しました） |
| `email.clicked`（__コード0__） | Link clicked（リンクがクリックされました） |
| `email.bounced`（__コード0__） | Email bounced（電子メールが返送されました） |
| `email.complained`（__コード0__） | Spam complaint（スパムに関する苦情） |

## When to Use （いつ使用するか）

- Sending transactional emails （トランザクションメールの送信）
- Welcome emails, password resets （ウェルカムメール、パスワードのリセット）
- Receipt and notification emails （受信および通知メール）
- Developer-friendly email integration （開発者向けの電子メール統合）
- React-based email templates （Reactベースのメールテンプレート）

## Rate Limits （レート制限）

- Free: 100 emails/day, 3,000/month （無料: 100 メール/日、3,000 メール/月）
- Pro: 100 emails/second （プロ: 100 メール/秒）
- Higher limits on scale plans （スケール プランの上限の引き上げ）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- onboarding-cro （オンボーディングクロ）
