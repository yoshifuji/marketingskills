# SendGrid （日本語訳：送信グリッド）

Email delivery platform for transactional and marketing emails. （日本語訳：トランザクションおよびマーケティング電子メールのための電子メール配信プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Mail Send API, Marketing API（日本語訳：メール送信API、マーケティングAPI） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | Official libraries for most languages（日本語訳：ほとんどの言語の公式ライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API Keys in SendGrid dashboard （日本語訳：**キーの取得**: SendGrid ダッシュボードの [設定] > [API キー]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Send email （日本語訳：電子メールを送信する）

```bash
POST https://api.sendgrid.com/v3/mail/send

Authorization: Bearer {api_key}

{
  "personalizations": [{
    "to": [{"email": "user@example.com"}]
  }],
  "from": {"email": "hello@example.com"},
  "subject": "Welcome!",
  "content": [{
    "type": "text/html",
    "value": "<h1>Welcome!</h1>"
  }]
}
```

### Send with template （日本語訳：テンプレートで送信）

```bash
POST https://api.sendgrid.com/v3/mail/send

{
  "personalizations": [{
    "to": [{"email": "user@example.com"}],
    "dynamic_template_data": {
      "name": "John",
      "order_id": "12345"
    }
  }],
  "from": {"email": "hello@example.com"},
  "template_id": "d-xxx"
}
```

### Add contact to list （日本語訳：連絡先をリストに追加）

```bash
PUT https://api.sendgrid.com/v3/marketing/contacts

{
  "list_ids": ["list-id"],
  "contacts": [{
    "email": "user@example.com",
    "first_name": "John",
    "last_name": "Doe"
  }]
}
```

### Search contacts （日本語訳：連絡先の検索）

```bash
POST https://api.sendgrid.com/v3/marketing/contacts/search

{
  "query": "email LIKE 'user@%'"
}
```

### Get email statistics （日本語訳：電子メールの統計を取得する）

```bash
GET https://api.sendgrid.com/v3/stats?start_date=2024-01-01&end_date=2024-01-31

Authorization: Bearer {api_key}
```

### Get bounces （日本語訳：バウンスを取得する）

```bash
GET https://api.sendgrid.com/v3/suppression/bounces

Authorization: Bearer {api_key}
```

### Get spam reports （日本語訳：スパムレポートを取得する）

```bash
GET https://api.sendgrid.com/v3/suppression/spam_reports

Authorization: Bearer {api_key}
```

### Validate email （日本語訳：電子メールを検証する）

```bash
POST https://api.sendgrid.com/v3/validations/email

{
  "email": "user@example.com"
}
```

## Webhook Events （日本語訳：Webhook イベント）

| Event（日本語訳：イベント） | Description（日本語訳：説明） |
|-------|-------------|
| `processed`（日本語訳：__コード0__） | Email accepted（日本語訳：電子メールを受け付けました） |
| `delivered`（日本語訳：__コード0__） | Email delivered（日本語訳：メール配信） |
| `open`（日本語訳：__コード0__） | Email opened（日本語訳：メールを開封しました） |
| `click`（日本語訳：__コード0__） | Link clicked（日本語訳：リンクがクリックされました） |
| `bounce`（日本語訳：__コード0__） | Hard/soft bounce（日本語訳：ハード/ソフトバウンス） |
| `dropped`（日本語訳：__コード0__） | Email dropped（日本語訳：メールがドロップされました） |
| `spamreport`（日本語訳：__コード0__） | Marked as spam（日本語訳：スパムとしてマークされる） |
| `unsubscribe`（日本語訳：__コード0__） | Unsubscribed（日本語訳：購読解除済み） |

## Node.js SDK （日本語訳：Node.js SDK）

```javascript
const sgMail = require('@sendgrid/mail');
sgMail.setApiKey('SG.xxx');

await sgMail.send({
  to: 'user@example.com',
  from: 'hello@example.com',
  subject: 'Welcome!',
  html: '<h1>Welcome!</h1>'
});
```

## When to Use （日本語訳：いつ使用するか）

- Transactional email at scale （日本語訳：大規模なトランザクションメール）
- Marketing email campaigns （日本語訳：マーケティング電子メール キャンペーン）
- Email validation （日本語訳：電子メールの検証）
- Deliverability management （日本語訳：納期管理）

## Rate Limits （日本語訳：レート制限）

- Free: 100 emails/day （日本語訳：無料: 100 メール/日）
- Paid: Varies by plan (up to millions/month) （日本語訳：有料: プランによって異なります (最大数百万/月)）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- analytics-tracking （日本語訳：分析追跡）
