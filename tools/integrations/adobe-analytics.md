# Adobe Analytics （アドビアナリティクス）

Enterprise analytics platform for cross-channel measurement and attribution. （クロスチャネル測定とアトリビューションのためのエンタープライズ分析プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Reporting API 2.0, Data Insertion API（レポート API 2.0、データ挿入 API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | AppMeasurement.js, Mobile SDKs, Launch（AppMeasurement.js、モバイル SDK、起動） |

## Authentication （認証）

- **Type**: OAuth 2.0 (Service Account JWT) （**タイプ**: OAuth 2.0 (サービス アカウント JWT)）
- **Setup**: Create integration in Adobe Developer Console （**セットアップ**: Adob​​e Developer Console で統合を作成する）
- **Header**: `Authorization: Bearer {access_token}` （**ヘッダー**: `Authorization: Bearer {access_token}`）

## Common Agent Operations （エージェントの共通操作）

### Get report suite info （レポート スイートの情報を取得する）

```bash
GET https://analytics.adobe.io/api/{company_id}/reportsuites

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Get dimensions （寸法の取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/dimensions?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Get metrics （メトリクスの取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/metrics?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Run report （レポートの実行）

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

### Get segments （セグメントの取得）

```bash
GET https://analytics.adobe.io/api/{company_id}/segments?rsid={report_suite_id}

Authorization: Bearer {access_token}
x-api-key: {client_id}
```

### Data Insertion (server-side) （データ挿入 (サーバー側)）

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

## AppMeasurement.js （AppMeasurement.js）

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

## Key Concepts （主要な概念）

- **Report Suite** - Data container （**レポートスイート** - データコンテナ）
- **eVars** - Conversion variables (persistent) （**eVars** - 変換変数 (永続)）
- **props** - Traffic variables (hit-level) （**props** - トラフィック変数 (ヒットレベル)）
- **Events** - Success metrics （**イベント** - 成功指標）
- **Segments** - User/visit filters （**セグメント** - ユーザー/訪問フィルター）
- **Calculated Metrics** - Derived metrics （**計算されたメトリクス** - 派生メトリクス）

## Common Dimensions （共通寸法）

- `variables/page` - Page name （`variables/page` - ページ名）
- `variables/evar1` - Custom conversion variable （`variables/evar1` - カスタム変換変数）
- `variables/prop1` - Custom traffic variable （`variables/prop1` - カスタム トラフィック変数）
- `variables/marketingchannel` - Marketing channel （`variables/marketingchannel` - マーケティング チャネル）
- `variables/referringdomain` - Referring domain （`variables/referringdomain` - 参照元ドメイン）

## Common Metrics （一般的な指標）

- `metrics/visits` - Visits （`metrics/visits` - 訪問数）
- `metrics/pageviews` - Page views （`metrics/pageviews` - ページビュー）
- `metrics/uniquevisitors` - Unique visitors （`metrics/uniquevisitors` - ユニークな訪問者）
- `metrics/orders` - Orders （`metrics/orders` - 注文）
- `metrics/revenue` - Revenue （`metrics/revenue` - 収益）

## When to Use （いつ使用するか）

- Enterprise-scale analytics （エンタープライズ規模の分析）
- Cross-channel attribution （クロスチャネルアトリビューション）
- Integration with Adobe Experience Cloud （Adobe Experience Cloudとの統合）
- Advanced segmentation （高度なセグメンテーション）
- Data warehouse exports （データウェアハウスのエクスポート）

## Rate Limits （レート制限）

- 12 requests/second per company （1 企業あたり 12 リクエスト/秒）
- 120 requests/minute （120 リクエスト/分）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- ab-test-setup （ab-テストのセットアップ）
- paid-ads （有料広告）
