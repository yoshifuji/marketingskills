# Google Ads （日本語訳：Google 広告）

Pay-per-click advertising platform for search, display, and video campaigns. （日本語訳：検索、ディスプレイ、動画キャンペーン用のクリック課金型広告プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Google Ads API for campaign management（日本語訳：キャンペーン管理用の Google 広告 API） |
| MCP（日本語訳：MCP） | ✓ | Available via Google Ads MCP server（日本語訳：Google 広告 MCP サーバー経由で利用可能） |
| CLI（日本語訳：CLI） | - | Use gcloud or API scripts（日本語訳：gcloud または API スクリプトを使用する） |
| SDK（日本語訳：SDK） | ✓ | Client libraries for multiple languages（日本語訳：複数言語のクライアント ライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 （日本語訳：**タイプ**: OAuth 2.0）
- **Scopes**: `https://www.googleapis.com/auth/adwords` （日本語訳：**スコープ**: `https://www.googleapis.com/auth/adwords`）
- **Setup**: Create credentials in Google Cloud Console, link to Google Ads account （日本語訳：**セットアップ**: Google Cloud Console で認証情報を作成し、Google 広告アカウントにリンクします）
- **Headers**: `developer-token`, `login-customer-id` (for MCC) （日本語訳：**ヘッダー**: `developer-token`、`login-customer-id` (MCC の場合)）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get account info （日本語訳：アカウント情報を取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT customer.id, customer.descriptive_name FROM customer"
}
```

### List campaigns （日本語訳：リストキャンペーン）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT campaign.id, campaign.name, campaign.status, campaign_budget.amount_micros FROM campaign ORDER BY campaign.id"
}
```

### Get campaign performance （日本語訳：キャンペーンのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT campaign.name, metrics.impressions, metrics.clicks, metrics.cost_micros, metrics.conversions FROM campaign WHERE segments.date DURING LAST_30_DAYS"
}
```

### Get ad group performance （日本語訳：広告グループのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT ad_group.name, metrics.impressions, metrics.clicks, metrics.conversions FROM ad_group WHERE segments.date DURING LAST_7_DAYS"
}
```

### Get keyword performance （日本語訳：キーワードのパフォーマンスを取得する）

```bash
POST https://googleads.googleapis.com/v14/customers/{customer_id}/googleAds:searchStream

{
  "query": "SELECT ad_group_criterion.keyword.text, metrics.impressions, metrics.clicks, metrics.average_cpc FROM keyword_view WHERE segments.date DURING LAST_30_DAYS ORDER BY metrics.clicks DESC LIMIT 50"
}
```

### Pause campaign （日本語訳：キャンペーンを一時停止する）

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

### Update budget （日本語訳：予算を更新する）

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

## Key Metrics （日本語訳：主要な指標）

| Metric（日本語訳：メトリック） | Description（日本語訳：説明） |
|--------|-------------|
| `metrics.impressions`（日本語訳：__コード0__） | Ad impressions（日本語訳：広告のインプレッション数） |
| `metrics.clicks`（日本語訳：__コード0__） | Clicks（日本語訳：クリック数） |
| `metrics.cost_micros`（日本語訳：__コード0__） | Cost in micros (divide by 1M)（日本語訳：マイクロ単位のコスト (1M で割る)） |
| `metrics.conversions`（日本語訳：__コード0__） | Conversions（日本語訳：コンバージョン） |
| `metrics.conversions_value`（日本語訳：__コード0__） | Conversion value（日本語訳：コンバージョン値） |
| `metrics.average_cpc`（日本語訳：__コード0__） | Average cost per click（日本語訳：クリックあたりの平均コスト） |
| `metrics.ctr`（日本語訳：__コード0__） | Click-through rate（日本語訳：クリックスルー率） |
| `metrics.conversion_rate`（日本語訳：__コード0__） | Conversion rate（日本語訳：コンバージョン率） |

## Campaign Types （日本語訳：キャンペーンの種類）

- `SEARCH` - Search network text ads （日本語訳：`SEARCH` - 検索ネットワークのテキスト広告）
- `DISPLAY` - Display network （日本語訳：`DISPLAY` - ディスプレイ ネットワーク）
- `SHOPPING` - Product shopping ads （日本語訳：`SHOPPING` - 商品ショッピング広告）
- `VIDEO` - YouTube video ads （日本語訳：`VIDEO` - YouTube 動画広告）
- `PERFORMANCE_MAX` - AI-optimized across channels （日本語訳：`PERFORMANCE_MAX` - チャネル全体で AI によって最適化）
- `DEMAND_GEN` - Discovery/Demand Gen （日本語訳：`DEMAND_GEN` - ディスカバリー/デマンド生成）

## GAQL (Google Ads Query Language) （日本語訳：GAQL (Google 広告クエリ言語)）

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

## When to Use （日本語訳：いつ使用するか）

- Managing search advertising campaigns （日本語訳：検索広告キャンペーンの管理）
- Analyzing campaign performance （日本語訳：キャンペーンのパフォーマンスを分析する）
- Adjusting budgets and bids （日本語訳：予算と入札単価の調整）
- Keyword research and management （日本語訳：キーワードの調査と管理）
- Conversion tracking analysis （日本語訳：コンバージョントラッキング分析）

## Rate Limits （日本語訳：レート制限）

- 15,000 operations per day (basic) （日本語訳：1 日あたり 15,000 操作 (基本)）
- Higher limits with developer token levels （日本語訳：開発者トークンレベルによる上限の引き上げ）

## Relevant Skills （日本語訳：関連するスキル）

- paid-ads （日本語訳：有料広告）
- analytics-tracking （日本語訳：分析追跡）
- page-cro （日本語訳：ページクロ）
