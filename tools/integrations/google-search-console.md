# Google Search Console （Googleサーチコンソール）

Free tool for monitoring website search performance and indexing. （Web サイトの検索パフォーマンスとインデックス作成を監視するための無料ツール。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Search Analytics API, URL Inspection API（検索分析 API、URL 検査 API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Use gcloud or API scripts（gcloud または API スクリプトを使用する） |
| SDK（SDK） | ✓ | Google API client libraries（Google APIクライアントライブラリ） |

## Authentication （認証）

- **Type**: OAuth 2.0 or Service Account （**タイプ**: OAuth 2.0 またはサービス アカウント）
- **Scopes**: `https://www.googleapis.com/auth/webmasters.readonly` （**スコープ**: `https://www.googleapis.com/auth/webmasters.readonly`）
- **Setup**: Create credentials in Google Cloud Console （**セットアップ**: Google Cloud Console で認証情報を作成する）

## Common Agent Operations （エージェントの共通操作）

### Get search analytics （検索分析を取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["query"],
  "rowLimit": 100
}
```

### Get performance by page （ページごとのパフォーマンスを取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["page"],
  "rowLimit": 50
}
```

### Get performance by country （国ごとのパフォーマンスを取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["country", "query"],
  "rowLimit": 100
}
```

### Inspect URL （URLを検査する）

```bash
POST https://searchconsole.googleapis.com/v1/urlInspection/index:inspect

{
  "inspectionUrl": "https://example.com/page",
  "siteUrl": "https://example.com/"
}
```

### List sitemaps （サイトマップをリストする）

```bash
GET https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/sitemaps

Authorization: Bearer {access_token}
```

### Submit sitemap （サイトマップを送信する）

```bash
PUT https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/sitemaps/{sitemap_url}

Authorization: Bearer {access_token}
```

### Request indexing （インデックス作成のリクエスト）

```bash
POST https://indexing.googleapis.com/v3/urlNotifications:publish

{
  "url": "https://example.com/new-page",
  "type": "URL_UPDATED"
}
```

## Dimensions （寸法）

- `query` - Search query （`query` - 検索クエリ）
- `page` - Page URL （`page` - ページの URL）
- `country` - Country code （`country` - 国コード）
- `device` - Device type (MOBILE, DESKTOP, TABLET) （`device` - デバイスのタイプ (モバイル、デスクトップ、タブレット)）
- `date` - Date （`date` - 日付）
- `searchAppearance` - Search result type （`searchAppearance` - 検索結果のタイプ）

## Metrics （メトリクス）

- `clicks` - Clicks from search （`clicks` - 検索からのクリック数）
- `impressions` - Search impressions （`impressions` - 検索インプレッション数）
- `ctr` - Click-through rate （`ctr` - クリックスルー率）
- `position` - Average position （`position` - 平均掲載順位）

## Filters （フィルター）

```json
{
  "dimensionFilterGroups": [{
    "filters": [{
      "dimension": "query",
      "operator": "contains",
      "expression": "keyword"
    }]
  }]
}
```

## When to Use （いつ使用するか）

- Analyzing search performance （検索パフォーマンスの分析）
- Finding keyword opportunities （キーワードの機会を見つける）
- Monitoring indexing status （インデックス作成ステータスの監視）
- Submitting new pages for indexing （インデックス作成のために新しいページを送信する）
- Identifying crawl issues （クロールの問題の特定）
- Tracking position changes （位置変化の追跡）

## Rate Limits （レート制限）

- 200 queries per minute （1 分あたり 200 クエリ）
- 1,200 requests per minute （1 分あたり 1,200 リクエスト）

## Relevant Skills （関連するスキル）

- seo-audit （SEO監査）
- programmatic-seo （プログラマティックSEO）
- analytics-tracking （分析追跡）
