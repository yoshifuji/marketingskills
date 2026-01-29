# LinkedIn Ads （日本語訳：LinkedIn の広告）

B2B advertising platform with professional targeting. （日本語訳：プロフェッショナルなターゲティングを備えた B2B 広告プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Marketing API for campaigns, audiences, analytics（日本語訳：キャンペーン、オーディエンス、分析のためのマーケティング API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | API-only (community libraries available)（日本語訳：API のみ (コミュニティ ライブラリが利用可能)） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 （日本語訳：**タイプ**: OAuth 2.0）
- **Header**: `Authorization: Bearer {access_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Scopes**: `r_ads`, `r_ads_reporting`, `rw_ads` （日本語訳：**スコープ**: `r_ads`、`r_ads_reporting`、`rw_ads`）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get ad accounts （日本語訳：広告アカウントを取得する）

```bash
GET https://api.linkedin.com/v2/adAccountsV2?q=search

Authorization: Bearer {access_token}
```

### Get campaigns （日本語訳：キャンペーンを取得する）

```bash
GET https://api.linkedin.com/v2/adCampaignsV2?q=search&search.account.values[0]=urn:li:sponsoredAccount:{account_id}

Authorization: Bearer {access_token}
```

### Get campaign analytics （日本語訳：キャンペーン分析を取得する）

```bash
GET https://api.linkedin.com/v2/adAnalyticsV2?q=analytics&pivot=CAMPAIGN&dateRange.start.year=2024&dateRange.start.month=1&dateRange.start.day=1&dateRange.end.year=2024&dateRange.end.month=1&dateRange.end.day=31&campaigns=urn:li:sponsoredCampaign:{campaign_id}&fields=impressions,clicks,costInLocalCurrency,conversions

Authorization: Bearer {access_token}
```

### Create campaign （日本語訳：キャンペーンの作成）

```bash
POST https://api.linkedin.com/v2/adCampaignsV2

Authorization: Bearer {access_token}

{
  "account": "urn:li:sponsoredAccount:{account_id}",
  "name": "Campaign Name",
  "type": "SPONSORED_UPDATES",
  "costType": "CPC",
  "unitCost": {
    "amount": "5.00",
    "currencyCode": "USD"
  },
  "dailyBudget": {
    "amount": "100.00",
    "currencyCode": "USD"
  },
  "status": "PAUSED"
}
```

### Update campaign status （日本語訳：キャンペーンステータスを更新する）

```bash
POST https://api.linkedin.com/v2/adCampaignsV2/{campaign_id}

Authorization: Bearer {access_token}

{
  "patch": {
    "$set": {
      "status": "ACTIVE"
    }
  }
}
```

### Get creatives （日本語訳：クリエイティブを取得する）

```bash
GET https://api.linkedin.com/v2/adCreativesV2?q=search&search.campaign.values[0]=urn:li:sponsoredCampaign:{campaign_id}

Authorization: Bearer {access_token}
```

### Get audience counts （日本語訳：視聴者数を取得する）

```bash
POST https://api.linkedin.com/v2/audienceCountsV2

{
  "audienceCriteria": {
    "include": {
      "and": [{
        "or": {
          "urn:li:adTargetingFacet:titles": ["urn:li:title:123"]
        }
      }]
    }
  }
}
```

## Key Metrics （日本語訳：主要な指標）

| Metric（日本語訳：メトリック） | Description（日本語訳：説明） |
|--------|-------------|
| `impressions`（日本語訳：__コード0__） | Ad impressions（日本語訳：広告のインプレッション数） |
| `clicks`（日本語訳：__コード0__） | Total clicks（日本語訳：合計クリック数） |
| `costInLocalCurrency`（日本語訳：__コード0__） | Spend（日本語訳：過ごす） |
| `conversions`（日本語訳：__コード0__） | Conversion count（日本語訳：コンバージョン数） |
| `leadGenerationMailContactInfoShares`（日本語訳：__コード0__） | Lead form submissions（日本語訳：リードフォームの送信） |

## Campaign Types （日本語訳：キャンペーンの種類）

- `SPONSORED_UPDATES` - Sponsored content （日本語訳：`SPONSORED_UPDATES` - スポンサー付きコンテンツ）
- `TEXT_AD` - Text ads （日本語訳：`TEXT_AD` - テキスト広告）
- `SPONSORED_INMAILS` - Message ads （日本語訳：`SPONSORED_INMAILS` - メッセージ広告）
- `DYNAMIC` - Dynamic ads （日本語訳：`DYNAMIC` - 動的広告）

## Targeting Options （日本語訳：ターゲティングオプション）

### Job-Based （日本語訳：ジョブベース）
- Job titles （日本語訳：役職名）
- Job functions （日本語訳：職務内容）
- Seniority levels （日本語訳：年功序列）
- Years of experience （日本語訳：長年の経験）

### Company-Based （日本語訳：企業ベース）
- Company names （日本語訳：会社名）
- Industries （日本語訳：産業）
- Company size （日本語訳：企業規模）
- Company followers （日本語訳：会社のフォロワー）

### Professional （日本語訳：プロ）
- Skills （日本語訳：スキル）
- Groups （日本語訳：グループ）
- Schools （日本語訳：学校）
- Degrees （日本語訳：学位）

## When to Use （日本語訳：いつ使用するか）

- B2B advertising （日本語訳：B2B広告）
- Job title targeting （日本語訳：役職ターゲティング）
- Account-based marketing （日本語訳：アカウントベースのマーケティング）
- Lead generation campaigns （日本語訳：リードジェネレーションキャンペーン）

## Rate Limits （日本語訳：レート制限）

- 100 requests/day (basic) （日本語訳：100 リクエスト/日 (基本)）
- 10,000 requests/day (Marketing Developer Platform) （日本語訳：10,000 リクエスト/日 (マーケティング開発者プラットフォーム)）

## Relevant Skills （日本語訳：関連するスキル）

- paid-ads （日本語訳：有料広告）
- analytics-tracking （日本語訳：分析追跡）
