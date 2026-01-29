# Segment （日本語訳：セグメント）

Customer data platform for collecting, routing, and activating user data. （日本語訳：ユーザー データを収集、ルーティング、アクティブ化するための顧客データ プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Tracking API, Profile API, Config API（日本語訳：トラッキング API、プロファイル API、構成 API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | analytics.js, iOS, Android, server libraries（日本語訳：Analytics.js、iOS、Android、サーバー ライブラリ） |

## Authentication （日本語訳：認証）

- **Tracking**: Write Key (per source) （日本語訳：**トラッキング**: 書き込みキー (ソースごと)）
- **API**: Access Token (OAuth 2.0) （日本語訳：**API**: アクセス トークン (OAuth 2.0)）
- **Header**: `Authorization: Bearer {access_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {access_token}`）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Track event （日本語訳：イベントを追跡する）

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

### Identify user （日本語訳：ユーザーの識別）

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

### Track page view （日本語訳：ページビューを追跡する）

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

### Batch events （日本語訳：バッチイベント）

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

### Get user profile (Profile API) （日本語訳：ユーザープロファイルの取得（プロファイルAPI））

```bash
GET https://profiles.segment.com/v1/spaces/{space_id}/collections/users/profiles/user_id:{user_id}/traits

Authorization: Basic {base64(access_token:)}
```

### Get user events （日本語訳：ユーザーイベントを取得する）

```bash
GET https://profiles.segment.com/v1/spaces/{space_id}/collections/users/profiles/user_id:{user_id}/events

Authorization: Basic {base64(access_token:)}
```

## JavaScript SDK （日本語訳：JavaScript SDK）

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

## Key Concepts （日本語訳：主要な概念）

- **Sources** - Where data comes from (website, app, server) （日本語訳：**ソース** - データの取得元 (Web サイト、アプリ、サーバー)）
- **Destinations** - Where data goes (analytics, CRM, ads) （日本語訳：**宛先** - データの送信先 (分析、CRM、広告)）
- **Tracking Plan** - Schema for events and properties （日本語訳：**追跡計画** - イベントとプロパティのスキーマ）
- **Protocols** - Data governance and validation （日本語訳：**プロトコル** - データ ガバナンスと検証）
- **Personas** - Unified user profiles （日本語訳：**ペルソナ** - 統合されたユーザー プロファイル）
- **Audiences** - Computed user segments （日本語訳：**視聴者** - 計算されたユーザー セグメント）

## Common Destinations （日本語訳：一般的な目的地）

- Analytics: GA4, Mixpanel, Amplitude （日本語訳：分析: GA4、ミックスパネル、振幅）
- CRM: HubSpot, Salesforce （日本語訳：CRM: HubSpot、Salesforce）
- Email: Customer.io, Mailchimp （日本語訳：電子メール: Customer.io、Mailchimp）
- Ads: Google Ads, Meta （日本語訳：広告: Google 広告、メタ）
- Data Warehouse: BigQuery, Snowflake （日本語訳：データ ウェアハウス: BigQuery、Snowflake）

## When to Use （日本語訳：いつ使用するか）

- Centralizing event tracking （日本語訳：イベント追跡の一元化）
- Routing data to multiple tools （日本語訳：データを複数のツールにルーティングする）
- Maintaining consistent tracking （日本語訳：一貫した追跡を維持する）
- Building unified user profiles （日本語訳：統合されたユーザープロファイルの構築）
- Syncing audiences across platforms （日本語訳：プラットフォーム間で視聴者を同期する）

## Rate Limits （日本語訳：レート制限）

- 500 requests/second per source （日本語訳：ソースごとに 500 リクエスト/秒）
- Batch up to 500KB or 32KB per event （日本語訳：イベントあたり最大 500 KB または 32 KB のバッチ）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- email-sequence （日本語訳：電子メールシーケンス）
- paid-ads （日本語訳：有料広告）
