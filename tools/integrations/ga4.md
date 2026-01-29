# Google Analytics 4 (GA4) （Google アナリティクス 4 (GA4)）

Web analytics platform for tracking user behavior, conversions, and marketing performance. （ユーザーの行動、コンバージョン、マーケティング パフォーマンスを追跡するための Web 分析プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Data API for reports, Admin API for configuration（レポート用のデータ API、構成用の管理 API） |
| MCP（MCP） | ✓ | Available via Google Analytics MCP server（Google Analytics MCPサーバー経由で利用可能） |
| CLI（CLI） | - | Use gcloud for some operations（一部の操作には gcloud を使用します） |
| SDK（SDK） | ✓ | gtag.js, Google Analytics SDK for mobile（gtag.js、モバイル用 Google アナリティクス SDK） |

## Authentication （認証）

- **Type**: OAuth 2.0 or Service Account （**タイプ**: OAuth 2.0 またはサービス アカウント）
- **Scopes**: `https://www.googleapis.com/auth/analytics.readonly` (read), `https://www.googleapis.com/auth/analytics.edit` (write) （**スコープ**: `https://www.googleapis.com/auth/analytics.readonly` (読み取り)、`https://www.googleapis.com/auth/analytics.edit` (書き込み)）
- **Setup**: Create credentials in Google Cloud Console （**セットアップ**: Google Cloud Console で認証情報を作成する）

## Common Agent Operations （エージェントの共通操作）

### Run a report (Data API) （レポートの実行 (データ API)）

```bash
POST https://analyticsdata.googleapis.com/v1beta/properties/{property_id}:runReport

{
  "dateRanges": [{"startDate": "30daysAgo", "endDate": "today"}],
  "dimensions": [{"name": "sessionSource"}],
  "metrics": [{"name": "sessions"}, {"name": "conversions"}]
}
```

### Get real-time data （リアルタイムデータを取得する）

```bash
POST https://analyticsdata.googleapis.com/v1beta/properties/{property_id}:runRealtimeReport

{
  "dimensions": [{"name": "country"}],
  "metrics": [{"name": "activeUsers"}]
}
```

### List conversion events （変換イベントのリストを表示する）

```bash
GET https://analyticsadmin.googleapis.com/v1beta/properties/{property_id}/conversionEvents
```

### Create a conversion event （コンバージョンイベントを作成する）

```bash
POST https://analyticsadmin.googleapis.com/v1beta/properties/{property_id}/conversionEvents

{
  "eventName": "purchase"
}
```

## Client-Side Tracking （クライアント側の追跡）

### Send custom event (gtag.js) （カスタム イベントの送信 (gtag.js)）

```javascript
gtag('event', 'signup_completed', {
  'method': 'email',
  'plan': 'free'
});
```

### Send event via Measurement Protocol （測定プロトコル経由でイベントを送信）

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

## Key Dimensions & Metrics （主要なディメンションと指標）

### Common Dimensions （共通寸法）
- `sessionSource` - Traffic source （`sessionSource` - トラフィックソース）
- `sessionMedium` - Traffic medium （`sessionMedium` - トラフィック媒体）
- `sessionCampaignName` - Campaign name （`sessionCampaignName` - キャンペーン名）
- `landingPage` - Entry page （`landingPage` - エントリーページ）
- `deviceCategory` - Device type （`deviceCategory` - デバイスのタイプ）
- `country` - User country （`country` - ユーザーの国）

### Common Metrics （一般的な指標）
- `sessions` - Total sessions （`sessions` - 合計セッション数）
- `activeUsers` - Active users （`activeUsers` - アクティブなユーザー）
- `newUsers` - New users （`newUsers` - 新規ユーザー）
- `conversions` - Conversion events （`conversions` - 変換イベント）
- `engagementRate` - Engaged sessions rate （`engagementRate` - エンゲージメントセッション率）
- `averageSessionDuration` - Session duration （`averageSessionDuration` - セッション期間）

## When to Use （いつ使用するか）

- Tracking website traffic and user behavior （Web サイトのトラフィックとユーザーの行動を追跡する）
- Measuring marketing campaign performance （マーケティング キャンペーンのパフォーマンスの測定）
- Setting up conversion tracking （コンバージョン トラッキングの設定）
- Analyzing user journeys and funnels （ユーザージャーニーとファネルの分析）
- Attribution modeling （アトリビューションモデリング）

## Rate Limits （レート制限）

- Data API: 10 requests per second per property （データ API: プロパティごとに 1 秒あたり 10 リクエスト）
- Admin API: Varies by endpoint （管理 API: エンドポイントによって異なります）
- Measurement Protocol: 1M hits/day for free tier （測定プロトコル: 無料枠で 100 万ヒット/日）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- ab-test-setup （ab-テストのセットアップ）
- seo-audit （SEO監査）
- page-cro （ページクロ）
