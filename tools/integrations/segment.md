# Segment （セグメント）

Customer data platform for collecting, routing, and activating user data. （ユーザー データを収集、ルーティング、アクティブ化するための顧客データ プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Tracking API, Profile API, Config API（トラッキング API、プロファイル API、構成 API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | analytics.js, iOS, Android, server libraries（Analytics.js、iOS、Android、サーバー ライブラリ） |

## Authentication （認証）

- **Tracking**: Write Key (per source) （**トラッキング**: 書き込みキー (ソースごと)）
- **API**: Access Token (OAuth 2.0) （**API**: アクセス トークン (OAuth 2.0)）
- **Header**: `Authorization: Bearer {access_token}` （**ヘッダー**: `Authorization: Bearer {access_token}`）

## Common Agent Operations （エージェントの共通操作）

### Track event （イベントを追跡する）

```bash
POST https://api.segment.io/v1/track

Authorization: Basic {base64(write_key:)}

{
  "userId": "user_123",
  "event": "signup_completed",
  "properties": {
    "plan": "pro",
    "method": "email"
  }
}
```

### Identify user （ユーザーの識別）

```bash
POST https://api.segment.io/v1/identify

Authorization: Basic {base64(write_key:)}

{
  "userId": "user_123",
  "traits": {
    "email": "user@example.com",
    "name": "John Doe",
    "plan": "pro"
  }
}
```

### Track page view （ページビューを追跡する）

```bash
POST https://api.segment.io/v1/page

Authorization: Basic {base64(write_key:)}

{
  "userId": "user_123",
  "name": "Pricing",
  "properties": {
    "title": "Pricing - Example",
    "url": "https://example.com/pricing"
  }
}
```

### Batch events （バッチイベント）

```bash
POST https://api.segment.io/v1/batch

Authorization: Basic {base64(write_key:)}

{
  "batch": [
    {"type": "identify", "userId": "user_1", "traits": {"plan": "free"}},
    {"type": "track", "userId": "user_1", "event": "signup"}
  ]
}
```

### Get user profile (Profile API) （ユーザープロファイルの取得（プロファイルAPI））

```bash
GET https://profiles.segment.com/v1/spaces/{space_id}/collections/users/profiles/user_id:{user_id}/traits

Authorization: Basic {base64(access_token:)}
```

### Get user events （ユーザーイベントを取得する）

```bash
GET https://profiles.segment.com/v1/spaces/{space_id}/collections/users/profiles/user_id:{user_id}/events

Authorization: Basic {base64(access_token:)}
```

## JavaScript SDK （JavaScript SDK）

```javascript
// Initialize
analytics.load('WRITE_KEY');

// Identify user
analytics.identify('user_123', {
  email: 'user@example.com',
  plan: 'pro'
});

// Track event
analytics.track('Feature Used', {
  feature_name: 'export'
});

// Page view
analytics.page('Pricing');
```

## Key Concepts （主要な概念）

- **Sources** - Where data comes from (website, app, server) （**ソース** - データの取得元 (Web サイト、アプリ、サーバー)）
- **Destinations** - Where data goes (analytics, CRM, ads) （**宛先** - データの送信先 (分析、CRM、広告)）
- **Tracking Plan** - Schema for events and properties （**追跡計画** - イベントとプロパティのスキーマ）
- **Protocols** - Data governance and validation （**プロトコル** - データ ガバナンスと検証）
- **Personas** - Unified user profiles （**ペルソナ** - 統合されたユーザー プロファイル）
- **Audiences** - Computed user segments （**視聴者** - 計算されたユーザー セグメント）

## Common Destinations （一般的な目的地）

- Analytics: GA4, Mixpanel, Amplitude （分析: GA4、ミックスパネル、振幅）
- CRM: HubSpot, Salesforce （CRM: HubSpot、Salesforce）
- Email: Customer.io, Mailchimp （電子メール: Customer.io、Mailchimp）
- Ads: Google Ads, Meta （広告: Google 広告、メタ）
- Data Warehouse: BigQuery, Snowflake （データ ウェアハウス: BigQuery、Snowflake）

## When to Use （いつ使用するか）

- Centralizing event tracking （イベント追跡の一元化）
- Routing data to multiple tools （データを複数のツールにルーティングする）
- Maintaining consistent tracking （一貫した追跡を維持する）
- Building unified user profiles （統合されたユーザープロファイルの構築）
- Syncing audiences across platforms （プラットフォーム間で視聴者を同期する）

## Rate Limits （レート制限）

- 500 requests/second per source （ソースごとに 500 リクエスト/秒）
- Batch up to 500KB or 32KB per event （イベントあたり最大 500 KB または 32 KB のバッチ）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- email-sequence （電子メールシーケンス）
- paid-ads （有料広告）
