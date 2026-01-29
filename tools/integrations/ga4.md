# Google Analytics 4 (GA4) （日本語訳：Google アナリティクス 4 (GA4)）

Web analytics platform for tracking user behavior, conversions, and marketing performance. （日本語訳：ユーザーの行動、コンバージョン、マーケティング パフォーマンスを追跡するための Web 分析プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Data API for reports, Admin API for configuration（日本語訳：レポート用のデータ API、構成用の管理 API） |
| MCP（日本語訳：MCP） | ✓ | Available via Google Analytics MCP server（日本語訳：Google Analytics MCPサーバー経由で利用可能） |
| CLI（日本語訳：CLI） | - | Use gcloud for some operations（日本語訳：一部の操作には gcloud を使用します） |
| SDK（日本語訳：SDK） | ✓ | gtag.js, Google Analytics SDK for mobile（日本語訳：gtag.js、モバイル用 Google アナリティクス SDK） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 or Service Account （日本語訳：**タイプ**: OAuth 2.0 またはサービス アカウント）
- **Scopes**: `https://www.googleapis.com/auth/analytics.readonly` (read), `https://www.googleapis.com/auth/analytics.edit` (write) （日本語訳：**スコープ**: `https://www.googleapis.com/auth/analytics.readonly` (読み取り)、`https://www.googleapis.com/auth/analytics.edit` (書き込み)）
- **Setup**: Create credentials in Google Cloud Console （日本語訳：**セットアップ**: Google Cloud Console で認証情報を作成する）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Run a report (Data API) （日本語訳：レポートの実行 (データ API)）

```bash
POST https://analyticsdata.googleapis.com/v1beta/properties/{property_id}:runReport

{
  "dateRanges": [{"startDate": "30daysAgo", "endDate": "today"}],
  "dimensions": [{"name": "sessionSource"}],
  "metrics": [{"name": "sessions"}, {"name": "conversions"}]
}
```

### Get real-time data （日本語訳：リアルタイムデータを取得する）

```bash
POST https://analyticsdata.googleapis.com/v1beta/properties/{property_id}:runRealtimeReport

{
  "dimensions": [{"name": "country"}],
  "metrics": [{"name": "activeUsers"}]
}
```

### List conversion events （日本語訳：変換イベントのリストを表示する）

```bash
GET https://analyticsadmin.googleapis.com/v1beta/properties/{property_id}/conversionEvents
```

### Create a conversion event （日本語訳：コンバージョンイベントを作成する）

```bash
POST https://analyticsadmin.googleapis.com/v1beta/properties/{property_id}/conversionEvents

{
  "eventName": "purchase"
}
```

## Client-Side Tracking （日本語訳：クライアント側の追跡）

### Send custom event (gtag.js) （日本語訳：カスタム イベントの送信 (gtag.js)）

```javascript
gtag('event', 'signup_completed', {
  'method': 'email',
  'plan': 'free'
});
```

### Send event via Measurement Protocol （日本語訳：測定プロトコル経由でイベントを送信）

```bash
POST https://www.google-analytics.com/mp/collect?measurement_id={measurement_id}&api_secret={api_secret}

{
  "client_id": "client_123",
  "events": [{
    "name": "purchase",
    "params": {
      "value": 99.99,
      "currency": "USD"
    }
  }]
}
```

## Key Dimensions & Metrics （日本語訳：主要なディメンションと指標）

### Common Dimensions （日本語訳：共通寸法）
- `sessionSource` - Traffic source （日本語訳：`sessionSource` - トラフィックソース）
- `sessionMedium` - Traffic medium （日本語訳：`sessionMedium` - トラフィック媒体）
- `sessionCampaignName` - Campaign name （日本語訳：`sessionCampaignName` - キャンペーン名）
- `landingPage` - Entry page （日本語訳：`landingPage` - エントリーページ）
- `deviceCategory` - Device type （日本語訳：`deviceCategory` - デバイスのタイプ）
- `country` - User country （日本語訳：`country` - ユーザーの国）

### Common Metrics （日本語訳：一般的な指標）
- `sessions` - Total sessions （日本語訳：`sessions` - 合計セッション数）
- `activeUsers` - Active users （日本語訳：`activeUsers` - アクティブなユーザー）
- `newUsers` - New users （日本語訳：`newUsers` - 新規ユーザー）
- `conversions` - Conversion events （日本語訳：`conversions` - 変換イベント）
- `engagementRate` - Engaged sessions rate （日本語訳：`engagementRate` - エンゲージメントセッション率）
- `averageSessionDuration` - Session duration （日本語訳：`averageSessionDuration` - セッション期間）

## When to Use （日本語訳：いつ使用するか）

- Tracking website traffic and user behavior （日本語訳：Web サイトのトラフィックとユーザーの行動を追跡する）
- Measuring marketing campaign performance （日本語訳：マーケティング キャンペーンのパフォーマンスの測定）
- Setting up conversion tracking （日本語訳：コンバージョン トラッキングの設定）
- Analyzing user journeys and funnels （日本語訳：ユーザージャーニーとファネルの分析）
- Attribution modeling （日本語訳：アトリビューションモデリング）

## Rate Limits （日本語訳：レート制限）

- Data API: 10 requests per second per property （日本語訳：データ API: プロパティごとに 1 秒あたり 10 リクエスト）
- Admin API: Varies by endpoint （日本語訳：管理 API: エンドポイントによって異なります）
- Measurement Protocol: 1M hits/day for free tier （日本語訳：測定プロトコル: 無料枠で 100 万ヒット/日）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- ab-test-setup （日本語訳：ab-テストのセットアップ）
- seo-audit （日本語訳：SEO監査）
- page-cro （日本語訳：ページクロ）
