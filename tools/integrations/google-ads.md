# Google Ads （Google 広告）

Pay-per-click advertising platform for search, display, and video campaigns. （検索、ディスプレイ、動画キャンペーン用のクリック課金型広告プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Google Ads API for campaign management（キャンペーン管理用の Google 広告 API） |
| MCP（MCP） | ✓ | Available via Google Ads MCP server（Google 広告 MCP サーバー経由で利用可能） |
| CLI（CLI） | - | Use gcloud or API scripts（gcloud または API スクリプトを使用する） |
| SDK（SDK） | ✓ | Client libraries for multiple languages（複数言語のクライアント ライブラリ） |

## Authentication （認証）

- **Type**: OAuth 2.0 （**タイプ**: OAuth 2.0）
- **Scopes**: `https://www.googleapis.com/auth/adwords` （**スコープ**: `https://www.googleapis.com/auth/adwords`）
- **Setup**: Create credentials in Google Cloud Console, link to Google Ads account （**セットアップ**: Google Cloud Console で認証情報を作成し、Google 広告アカウントにリンクします）
- **Headers**: `developer-token`, `login-customer-id` (for MCC) （**ヘッダー**: `developer-token`、`login-customer-id` (MCC の場合)）

## Common Agent Operations （エージェントの共通操作）

### Get account info （アカウント情報を取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT customer.id, customer.descriptive_name FROM customer"
}
```

### List campaigns （リストキャンペーン）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT campaign.id, campaign.name, campaign.status, campaign_budget.amount_micros FROM campaign ORDER BY campaign.id"
}
```

### Get campaign performance （キャンペーンのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT campaign.name, metrics.impressions, metrics.clicks, metrics.cost_micros, metrics.conversions FROM campaign WHERE segments.date DURING LAST_30_DAYS"
}
```

### Get ad group performance （広告グループのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT ad_group.name, metrics.impressions, metrics.clicks, metrics.conversions FROM ad_group WHERE segments.date DURING LAST_7_DAYS"
}
```

### Get keyword performance （キーワードのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT ad_group_criterion.keyword.text, metrics.impressions, metrics.clicks, metrics.average_cpc FROM keyword_view WHERE segments.date DURING LAST_30_DAYS ORDER BY metrics.clicks DESC LIMIT 50"
}
```

### Pause campaign （キャンペーンを一時停止する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/campaigns:mutate

{
  "operations": [{
    "update": {
      "resourceName": "customers/{customer_id}/campaigns/{campaign_id}",
      "status": "PAUSED"
    },
    "updateMask": "status"
  }]
}
```

### Update budget （予算を更新する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/campaignBudgets:mutate

{
  "operations": [{
    "update": {
      "resourceName": "customers/{customer_id}/campaignBudgets/{budget_id}",
      "amountMicros": "50000000"
    },
    "updateMask": "amountMicros"
  }]
}
```

## Key Metrics （主要な指標）

| Metric（メトリック） | Description（説明） |
|--------|-------------|
| `metrics.impressions`（__コード0__） | Ad impressions（広告のインプレッション数） |
| `metrics.clicks`（__コード0__） | Clicks（クリック数） |
| `metrics.cost_micros`（__コード0__） | Cost in micros (divide by 1M)（マイクロ単位のコスト (1M で割る)） |
| `metrics.conversions`（__コード0__） | Conversions（コンバージョン） |
| `metrics.conversions_value`（__コード0__） | Conversion value（コンバージョン値） |
| `metrics.average_cpc`（__コード0__） | Average cost per click（クリックあたりの平均コスト） |
| `metrics.ctr`（__コード0__） | Click-through rate（クリックスルー率） |
| `metrics.conversion_rate`（__コード0__） | Conversion rate（コンバージョン率） |

## Campaign Types （キャンペーンの種類）

- `SEARCH` - Search network text ads （`SEARCH` - 検索ネットワークのテキスト広告）
- `DISPLAY` - Display network （`DISPLAY` - ディスプレイ ネットワーク）
- `SHOPPING` - Product shopping ads （`SHOPPING` - 商品ショッピング広告）
- `VIDEO` - YouTube video ads （`VIDEO` - YouTube 動画広告）
- `PERFORMANCE_MAX` - AI-optimized across channels （`PERFORMANCE_MAX` - チャネル全体で AI によって最適化）
- `DEMAND_GEN` - Discovery/Demand Gen （`DEMAND_GEN` - ディスカバリー/デマンド生成）

## GAQL (Google Ads Query Language) （GAQL (Google 広告クエリ言語)）

```sql
SELECT
  campaign.name,
  metrics.clicks,
  metrics.conversions
FROM campaign
WHERE
  campaign.status = 'ENABLED'
  AND segments.date DURING LAST_30_DAYS
ORDER BY metrics.conversions DESC
LIMIT 10
```

## When to Use （いつ使用するか）

- Managing search advertising campaigns （検索広告キャンペーンの管理）
- Analyzing campaign performance （キャンペーンのパフォーマンスを分析する）
- Adjusting budgets and bids （予算と入札単価の調整）
- Keyword research and management （キーワードの調査と管理）
- Conversion tracking analysis （コンバージョントラッキング分析）

## Rate Limits （レート制限）

- 15,000 operations per day (basic) （1 日あたり 15,000 操作 (基本)）
- Higher limits with developer token levels （開発者トークンレベルによる上限の引き上げ）

## Relevant Skills （関連するスキル）

- paid-ads （有料広告）
- analytics-tracking （分析追跡）
- page-cro （ページクロ）
