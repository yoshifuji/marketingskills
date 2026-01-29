# Mailchimp （メールチンパンジー）

Email marketing platform for campaigns, automation, and audience management. （キャンペーン、自動化、視聴者管理のための電子メール マーケティング プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Marketing API for campaigns, audiences, automation（キャンペーン、オーディエンス、自動化のためのマーケティング API） |
| MCP（MCP） | ✓ | Available via Mailchimp MCP server（Mailchimp MCP サーバー経由で利用可能） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | Official SDKs for multiple languages（複数の言語に対応した公式 SDK） |

## Authentication （認証）

- **Type**: API Key or OAuth 2.0 （**タイプ**: API キーまたは OAuth 2.0）
- **Header**: `Authorization: Bearer {api_key}` or `Authorization: apikey {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}` または `Authorization: apikey {api_key}`）
- **Base URL**: `https://{dc}.api.mailchimp.com/3.0/` (dc = datacenter from API key) （**ベース URL**: `https://{dc}.api.mailchimp.com/3.0/` (dc = API キーからのデータセンター)）

## Common Agent Operations （エージェントの共通操作）

### List audiences (lists) （オーディエンスをリストする (リスト)）

```bash
GET https://{dc}.api.mailchimp.com/3.0/lists
```

### Get audience members （視聴者を獲得する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/lists/{list_id}/members?count=100
```

### Add subscriber （購読者の追加）

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

### Update subscriber （購読者を更新する）

```bash
PATCH https://{dc}.api.mailchimp.com/3.0/lists/{list_id}/members/{subscriber_hash}

{
  "merge_fields": {
    "FNAME": "Jane"
  },
  "tags": ["customer", "premium"]
}
```

### Get campaigns （キャンペーンを取得する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/campaigns?count=20
```

### Get campaign report （キャンペーンレポートを入手する）

```bash
GET https://{dc}.api.mailchimp.com/3.0/reports/{campaign_id}
```

### Create campaign （キャンペーンの作成）

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

### Send campaign （キャンペーンを送信する）

```bash
POST https://{dc}.api.mailchimp.com/3.0/campaigns/{campaign_id}/actions/send
```

### List automations （リストオートメーション）

```bash
GET https://{dc}.api.mailchimp.com/3.0/automations
```

## Key Metrics （主要な指標）

### Campaign Report Fields （キャンペーンレポートのフィールド）
- `emails_sent` - Total sent （`emails_sent` - 送信合計数）
- `opens` - Open count （`opens` - オープン数）
- `unique_opens` - Unique opens （`unique_opens` - ユニークなオープン）
- `open_rate` - Open rate （`open_rate` - 開封率）
- `clicks` - Click count （`clicks` - クリック数）
- `click_rate` - Click rate （`click_rate` - クリック率）
- `unsubscribes` - Unsubscribe count （`unsubscribes` - 購読解除数）
- `bounces` - Bounce count （`bounces` - バウンス数）

### Subscriber Hash （加入者ハッシュ）

Calculate subscriber hash for updates: （更新用のサブスクライバ ハッシュを計算します。）
```javascript
const hash = md5(email.toLowerCase());
```

## Subscriber Statuses （加入者のステータス）

- `subscribed` - Active subscriber （`subscribed` - アクティブなサブスクライバ）
- `unsubscribed` - Unsubscribed （`unsubscribed` - 購読解除されました）
- `cleaned` - Hard bounce （`cleaned` - ハード バウンス）
- `pending` - Awaiting confirmation （`pending` - 確認待ち）
- `transactional` - Transactional only （`transactional` - トランザクションのみ）

## When to Use （いつ使用するか）

- Managing email lists and subscribers （メールリストと購読者の管理）
- Creating and sending email campaigns （電子メール キャンペーンの作成と送信）
- Setting up email automation （電子メールの自動化を設定する）
- Analyzing campaign performance （キャンペーンのパフォーマンスを分析する）
- Segmenting audiences （オーディエンスのセグメント化）
- A/B testing emails （A/B テストメール）

## Rate Limits （レート制限）

- 10 concurrent connections （10の同時接続）
- 10 requests per second （1 秒あたり 10 リクエスト）
- Batch endpoints for bulk operations （一括操作用のバッチエンドポイント）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- analytics-tracking （分析追跡）
- referral-program （紹介プログラム）
