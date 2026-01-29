# LinkedIn Ads （LinkedIn の広告）

B2B advertising platform with professional targeting. （プロフェッショナルなターゲティングを備えた B2B 広告プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Marketing API for campaigns, audiences, analytics（キャンペーン、オーディエンス、分析のためのマーケティング API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | API-only (community libraries available)（API のみ (コミュニティ ライブラリが利用可能)） |

## Authentication （認証）

- **Type**: OAuth 2.0 （**タイプ**: OAuth 2.0）
- **Header**: `Authorization: Bearer {access_token}` （**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Scopes**: `r_ads`, `r_ads_reporting`, `rw_ads` （**スコープ**: `r_ads`、`r_ads_reporting`、`rw_ads`）

## Common Agent Operations （エージェントの共通操作）

### Get ad accounts （広告アカウントを取得する）

```bash
GET https://api.linkedin.com/v2/adAccountsV2?q=search

Authorization: Bearer {access_token}
```

### Get campaigns （キャンペーンを取得する）

```bash
GET https://api.linkedin.com/v2/adCampaignsV2?q=search&search.account.values[0]=urn:li:sponsoredAccount:{account_id}

Authorization: Bearer {access_token}
```

### Get campaign analytics （キャンペーン分析を取得する）

```bash
GET https://api.linkedin.com/v2/adAnalyticsV2?q=analytics&pivot=CAMPAIGN&dateRange.start.year=2024&dateRange.start.month=1&dateRange.start.day=1&dateRange.end.year=2024&dateRange.end.month=1&dateRange.end.day=31&campaigns=urn:li:sponsoredCampaign:{campaign_id}&fields=impressions,clicks,costInLocalCurrency,conversions

Authorization: Bearer {access_token}
```

### Create campaign （キャンペーンの作成）

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

### Update campaign status （キャンペーンステータスを更新する）

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

### Get creatives （クリエイティブを取得する）

```bash
GET https://api.linkedin.com/v2/adCreativesV2?q=search&search.campaign.values[0]=urn:li:sponsoredCampaign:{campaign_id}

Authorization: Bearer {access_token}
```

### Get audience counts （視聴者数を取得する）

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

## Key Metrics （主要な指標）

| Metric（メトリック） | Description（説明） |
|--------|-------------|
| `impressions`（__コード0__） | Ad impressions（広告のインプレッション数） |
| `clicks`（__コード0__） | Total clicks（合計クリック数） |
| `costInLocalCurrency`（__コード0__） | Spend（過ごす） |
| `conversions`（__コード0__） | Conversion count（コンバージョン数） |
| `leadGenerationMailContactInfoShares`（__コード0__） | Lead form submissions（リードフォームの送信） |

## Campaign Types （キャンペーンの種類）

- `SPONSORED_UPDATES` - Sponsored content （`SPONSORED_UPDATES` - スポンサー付きコンテンツ）
- `TEXT_AD` - Text ads （`TEXT_AD` - テキスト広告）
- `SPONSORED_INMAILS` - Message ads （`SPONSORED_INMAILS` - メッセージ広告）
- `DYNAMIC` - Dynamic ads （`DYNAMIC` - 動的広告）

## Targeting Options （ターゲティングオプション）

### Job-Based （ジョブベース）
- Job titles （役職名）
- Job functions （職務内容）
- Seniority levels （年功序列）
- Years of experience （長年の経験）

### Company-Based （企業ベース）
- Company names （会社名）
- Industries （産業）
- Company size （企業規模）
- Company followers （会社のフォロワー）

### Professional （プロ）
- Skills （スキル）
- Groups （グループ）
- Schools （学校）
- Degrees （学位）

## When to Use （いつ使用するか）

- B2B advertising （B2B広告）
- Job title targeting （役職ターゲティング）
- Account-based marketing （アカウントベースのマーケティング）
- Lead generation campaigns （リードジェネレーションキャンペーン）

## Rate Limits （レート制限）

- 100 requests/day (basic) （100 リクエスト/日 (基本)）
- 10,000 requests/day (Marketing Developer Platform) （10,000 リクエスト/日 (マーケティング開発者プラットフォーム)）

## Relevant Skills （関連するスキル）

- paid-ads （有料広告）
- analytics-tracking （分析追跡）
