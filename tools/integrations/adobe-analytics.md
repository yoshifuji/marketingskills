# Adobe Analytics （日本語訳：アドビアナリティクス）

Enterprise analytics platform for cross-channel measurement and attribution. （日本語訳：クロスチャネル測定とアトリビューションのためのエンタープライズ分析プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Reporting API 2.0, Data Insertion API（日本語訳：レポート API 2.0、データ挿入 API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | AppMeasurement.js, Mobile SDKs, Launch（日本語訳：AppMeasurement.js、モバイル SDK、起動） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 (Service Account JWT) （日本語訳：**タイプ**: OAuth 2.0 (サービス アカウント JWT)）
- **Setup**: Create integration in Adobe Developer Console （日本語訳：**セットアップ**: Adob​​e Developer Console で統合を作成する）
- **Header**: `Authorization: Bearer {access_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {access_token}`）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get report suite info （日本語訳：レポート スイートの情報を取得する）

```bash
GET https://analytics.adobe.io/api/{company_id}/reportsuites

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Get dimensions （日本語訳：寸法の取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/dimensions?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Get metrics （日本語訳：メトリクスの取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/metrics?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Run report （日本語訳：レポートの実行）

```bash
POST https://analytics.adobe.io/api/{company_id}/reports

{
  "rsid": "{report_suite_id}",
  "globalFilters": [{
    "type": "dateRange",
    "dateRange": "2024-01-01T00:00:00/2024-01-31T23:59:59"
  }],
  "metricContainer": {
    "metrics": [
      {"id": "metrics/visits"},
      {"id": "metrics/pageviews"},
      {"id": "metrics/orders"}
    ]
  },
  "dimension": "variables/evar1"
}
```

### Get segments （日本語訳：セグメントの取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/segments?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Data Insertion (server-side) （日本語訳：データ挿入 (サーバー側)）

```bash
POST https://{tracking_server}/b/ss/{report_suite_id}/0

<?xml version="1.0" encoding="UTF-8"?>
<request>
  <visitorID>user_123</visitorID>
  <events>event1</events>
  <eVar1>campaign_name</eVar1>
  <prop1>page_type</prop1>
</request>
```

## AppMeasurement.js （日本語訳：AppMeasurement.js）

```javascript
// Initialize
var s = s_gi('report_suite_id');
s.trackingServer = 'metrics.example.com';

// Set variables
s.pageName = 'Home Page';
s.channel = 'Marketing';
s.eVar1 = 'campaign_name';
s.events = 'event1';

// Track page view
s.t();

// Track link
s.tl(this, 'o', 'Button Click');
```

## Key Concepts （日本語訳：主要な概念）

- **Report Suite** - Data container （日本語訳：**レポートスイート** - データコンテナ）
- **eVars** - Conversion variables (persistent) （日本語訳：**eVars** - 変換変数 (永続)）
- **props** - Traffic variables (hit-level) （日本語訳：**props** - トラフィック変数 (ヒットレベル)）
- **Events** - Success metrics （日本語訳：**イベント** - 成功指標）
- **Segments** - User/visit filters （日本語訳：**セグメント** - ユーザー/訪問フィルター）
- **Calculated Metrics** - Derived metrics （日本語訳：**計算されたメトリクス** - 派生メトリクス）

## Common Dimensions （日本語訳：共通寸法）

- `variables/page` - Page name （日本語訳：`variables/page` - ページ名）
- `variables/evar1` - Custom conversion variable （日本語訳：`variables/evar1` - カスタム変換変数）
- `variables/prop1` - Custom traffic variable （日本語訳：`variables/prop1` - カスタム トラフィック変数）
- `variables/marketingchannel` - Marketing channel （日本語訳：`variables/marketingchannel` - マーケティング チャネル）
- `variables/referringdomain` - Referring domain （日本語訳：`variables/referringdomain` - 参照元ドメイン）

## Common Metrics （日本語訳：一般的な指標）

- `metrics/visits` - Visits （日本語訳：`metrics/visits` - 訪問数）
- `metrics/pageviews` - Page views （日本語訳：`metrics/pageviews` - ページビュー）
- `metrics/uniquevisitors` - Unique visitors （日本語訳：`metrics/uniquevisitors` - ユニークな訪問者）
- `metrics/orders` - Orders （日本語訳：`metrics/orders` - 注文）
- `metrics/revenue` - Revenue （日本語訳：`metrics/revenue` - 収益）

## When to Use （日本語訳：いつ使用するか）

- Enterprise-scale analytics （日本語訳：エンタープライズ規模の分析）
- Cross-channel attribution （日本語訳：クロスチャネルアトリビューション）
- Integration with Adobe Experience Cloud （日本語訳：Adobe Experience Cloudとの統合）
- Advanced segmentation （日本語訳：高度なセグメンテーション）
- Data warehouse exports （日本語訳：データウェアハウスのエクスポート）

## Rate Limits （日本語訳：レート制限）

- 12 requests/second per company （日本語訳：1 企業あたり 12 リクエスト/秒）
- 120 requests/minute （日本語訳：120 リクエスト/分）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- ab-test-setup （日本語訳：ab-テストのセットアップ）
- paid-ads （日本語訳：有料広告）
