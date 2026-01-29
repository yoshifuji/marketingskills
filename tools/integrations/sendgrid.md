# SendGrid （送信グリッド）

Email delivery platform for transactional and marketing emails. （トランザクションおよびマーケティング電子メールのための電子メール配信プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Mail Send API, Marketing API（メール送信API、マーケティングAPI） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | Official libraries for most languages（ほとんどの言語の公式ライブラリ） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API Keys in SendGrid dashboard （**キーの取得**: SendGrid ダッシュボードの [設定] > [API キー]）

## Common Agent Operations （エージェントの共通操作）

### Send email （電子メールを送信する）

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

### Send with template （テンプレートで送信）

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

### Add contact to list （連絡先をリストに追加）

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

### Search contacts （連絡先の検索）

```bash
POST https://api.sendgrid.com/v3/marketing/contacts/search

{
  "query": "email LIKE 'user@%'"
}
```

### Get email statistics （電子メールの統計を取得する）

```bash
GET https://api.sendgrid.com/v3/stats?start_date=2024-01-01&end_date=2024-01-31

Authorization: Bearer {api_key}
```

### Get bounces （バウンスを取得する）

```bash
GET https://api.sendgrid.com/v3/suppression/bounces

Authorization: Bearer {api_key}
```

### Get spam reports （スパムレポートを取得する）

```bash
GET https://api.sendgrid.com/v3/suppression/spam_reports

Authorization: Bearer {api_key}
```

### Validate email （電子メールを検証する）

```bash
POST https://api.sendgrid.com/v3/validations/email

{
  "email": "user@example.com"
}
```

## Webhook Events （Webhook イベント）

| Event（イベント） | Description（説明） |
|-------|-------------|
| `processed`（__コード0__） | Email accepted（電子メールを受け付けました） |
| `delivered`（__コード0__） | Email delivered（メール配信） |
| `open`（__コード0__） | Email opened（メールを開封しました） |
| `click`（__コード0__） | Link clicked（リンクがクリックされました） |
| `bounce`（__コード0__） | Hard/soft bounce（ハード/ソフトバウンス） |
| `dropped`（__コード0__） | Email dropped（メールがドロップされました） |
| `spamreport`（__コード0__） | Marked as spam（スパムとしてマークされる） |
| `unsubscribe`（__コード0__） | Unsubscribed（購読解除済み） |

## Node.js SDK （Node.js SDK）

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

## When to Use （いつ使用するか）

- Transactional email at scale （大規模なトランザクションメール）
- Marketing email campaigns （マーケティング電子メール キャンペーン）
- Email validation （電子メールの検証）
- Deliverability management （納期管理）

## Rate Limits （レート制限）

- Free: 100 emails/day （無料: 100 メール/日）
- Paid: Varies by plan (up to millions/month) （有料: プランによって異なります (最大数百万/月)）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- analytics-tracking （分析追跡）
