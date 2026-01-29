# Mailchimp （日本語訳：メールチンパンジー）

Email marketing platform for campaigns, automation, and audience management. （日本語訳：キャンペーン、自動化、視聴者管理のための電子メール マーケティング プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Marketing API for campaigns, audiences, automation（日本語訳：キャンペーン、オーディエンス、自動化のためのマーケティング API） |
| MCP（日本語訳：MCP） | ✓ | Available via Mailchimp MCP server（日本語訳：Mailchimp MCP サーバー経由で利用可能） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | Official SDKs for multiple languages（日本語訳：複数の言語に対応した公式 SDK） |

## Authentication （日本語訳：認証）

- **Type**: API Key or OAuth 2.0 （日本語訳：**タイプ**: API キーまたは OAuth 2.0）
- **Header**: `Authorization: Bearer {api_key}` or `Authorization: apikey {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}` または `Authorization: apikey {api_key}`）
- **Base URL**: `https://{dc}.api.mailchimp.com/3.0/` (dc = datacenter from API key) （日本語訳：**ベース URL**: `https://{dc}.api.mailchimp.com/3.0/` (dc = API キーからのデータセンター)）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List audiences (lists) （日本語訳：オーディエンスをリストする (リスト)）

```bash
GET https://{dc}.api.mailchimp.com/3.0/lists
```

### Get audience members （日本語訳：視聴者を獲得する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/lists/{list_id}/members?count=100
```

### Add subscriber （日本語訳：購読者の追加）

```bash
POST https://{dc}.api.mailchimp.com/3.0/lists/{list_id}/members

{
  "email_address": "user@example.com",
  "status": "subscribed",
  "merge_fields": {
    "FNAME": "John",
    "LNAME": "Doe"
  }
}
```

### Update subscriber （日本語訳：購読者を更新する）

```bash
PATCH https://{dc}.api.mailchimp.com/3.0/lists/{list_id}/members/{subscriber_hash}

{
  "merge_fields": {
    "FNAME": "Jane"
  },
  "tags": ["customer", "premium"]
}
```

### Get campaigns （日本語訳：キャンペーンを取得する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/campaigns?count=20
```

### Get campaign report （日本語訳：キャンペーンレポートを入手する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/reports/{campaign_id}
```

### Create campaign （日本語訳：キャンペーンの作成）

```bash
POST https://{dc}.api.mailchimp.com/3.0/campaigns

{
  "type": "regular",
  "recipients": {
    "list_id": "{list_id}"
  },
  "settings": {
    "subject_line": "Your Subject",
    "from_name": "Your Name",
    "reply_to": "reply@example.com"
  }
}
```

### Send campaign （日本語訳：キャンペーンを送信する）

```bash
POST https://{dc}.api.mailchimp.com/3.0/campaigns/{campaign_id}/actions/send
```

### List automations （日本語訳：リストオートメーション）

```bash
GET https://{dc}.api.mailchimp.com/3.0/automations
```

## Key Metrics （日本語訳：主要な指標）

### Campaign Report Fields （日本語訳：キャンペーンレポートのフィールド）
- `emails_sent` - Total sent （日本語訳：`emails_sent` - 送信合計数）
- `opens` - Open count （日本語訳：`opens` - オープン数）
- `unique_opens` - Unique opens （日本語訳：`unique_opens` - ユニークなオープン）
- `open_rate` - Open rate （日本語訳：`open_rate` - 開封率）
- `clicks` - Click count （日本語訳：`clicks` - クリック数）
- `click_rate` - Click rate （日本語訳：`click_rate` - クリック率）
- `unsubscribes` - Unsubscribe count （日本語訳：`unsubscribes` - 購読解除数）
- `bounces` - Bounce count （日本語訳：`bounces` - バウンス数）

### Subscriber Hash （日本語訳：加入者ハッシュ）

Calculate subscriber hash for updates: （日本語訳：更新用のサブスクライバ ハッシュを計算します。）
```javascript
const hash = md5(email.toLowerCase());
```

## Subscriber Statuses （日本語訳：加入者のステータス）

- `subscribed` - Active subscriber （日本語訳：`subscribed` - アクティブなサブスクライバ）
- `unsubscribed` - Unsubscribed （日本語訳：`unsubscribed` - 購読解除されました）
- `cleaned` - Hard bounce （日本語訳：`cleaned` - ハード バウンス）
- `pending` - Awaiting confirmation （日本語訳：`pending` - 確認待ち）
- `transactional` - Transactional only （日本語訳：`transactional` - トランザクションのみ）

## When to Use （日本語訳：いつ使用するか）

- Managing email lists and subscribers （日本語訳：メールリストと購読者の管理）
- Creating and sending email campaigns （日本語訳：電子メール キャンペーンの作成と送信）
- Setting up email automation （日本語訳：電子メールの自動化を設定する）
- Analyzing campaign performance （日本語訳：キャンペーンのパフォーマンスを分析する）
- Segmenting audiences （日本語訳：オーディエンスのセグメント化）
- A/B testing emails （日本語訳：A/B テストメール）

## Rate Limits （日本語訳：レート制限）

- 10 concurrent connections （日本語訳：10の同時接続）
- 10 requests per second （日本語訳：1 秒あたり 10 リクエスト）
- Batch endpoints for bulk operations （日本語訳：一括操作用のバッチエンドポイント）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- analytics-tracking （日本語訳：分析追跡）
- referral-program （日本語訳：紹介プログラム）
