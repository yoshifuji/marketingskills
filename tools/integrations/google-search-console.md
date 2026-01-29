# Google Search Console （日本語訳：Googleサーチコンソール）

Free tool for monitoring website search performance and indexing. （日本語訳：Web サイトの検索パフォーマンスとインデックス作成を監視するための無料ツール。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Search Analytics API, URL Inspection API（日本語訳：検索分析 API、URL 検査 API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Use gcloud or API scripts（日本語訳：gcloud または API スクリプトを使用する） |
| SDK（日本語訳：SDK） | ✓ | Google API client libraries（日本語訳：Google APIクライアントライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 or Service Account （日本語訳：**タイプ**: OAuth 2.0 またはサービス アカウント）
- **Scopes**: `https://www.googleapis.com/auth/webmasters.readonly` （日本語訳：**スコープ**: `https://www.googleapis.com/auth/webmasters.readonly`）
- **Setup**: Create credentials in Google Cloud Console （日本語訳：**セットアップ**: Google Cloud Console で認証情報を作成する）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get search analytics （日本語訳：検索分析を取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["query"],
  "rowLimit": 100
}
```

### Get performance by page （日本語訳：ページごとのパフォーマンスを取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["page"],
  "rowLimit": 50
}
```

### Get performance by country （日本語訳：国ごとのパフォーマンスを取得する）

```bash
POST https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/searchAnalytics/query

{
  "startDate": "2024-01-01",
  "endDate": "2024-01-31",
  "dimensions": ["country", "query"],
  "rowLimit": 100
}
```

### Inspect URL （日本語訳：URLを検査する）

```bash
POST https://searchconsole.googleapis.com/v1/urlInspection/index:inspect

{
  "inspectionUrl": "https://example.com/page",
  "siteUrl": "https://example.com/"
}
```

### List sitemaps （日本語訳：サイトマップをリストする）

```bash
GET https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/sitemaps

Authorization: Bearer {access_token}
```

### Submit sitemap （日本語訳：サイトマップを送信する）

```bash
PUT https://searchconsole.googleapis.com/webmasters/v3/sites/{site_url}/sitemaps/{sitemap_url}

Authorization: Bearer {access_token}
```

### Request indexing （日本語訳：インデックス作成のリクエスト）

```bash
POST https://indexing.googleapis.com/v3/urlNotifications:publish

{
  "url": "https://example.com/new-page",
  "type": "URL_UPDATED"
}
```

## Dimensions （日本語訳：寸法）

- `query` - Search query （日本語訳：`query` - 検索クエリ）
- `page` - Page URL （日本語訳：`page` - ページの URL）
- `country` - Country code （日本語訳：`country` - 国コード）
- `device` - Device type (MOBILE, DESKTOP, TABLET) （日本語訳：`device` - デバイスのタイプ (モバイル、デスクトップ、タブレット)）
- `date` - Date （日本語訳：`date` - 日付）
- `searchAppearance` - Search result type （日本語訳：`searchAppearance` - 検索結果のタイプ）

## Metrics （日本語訳：メトリクス）

- `clicks` - Clicks from search （日本語訳：`clicks` - 検索からのクリック数）
- `impressions` - Search impressions （日本語訳：`impressions` - 検索インプレッション数）
- `ctr` - Click-through rate （日本語訳：`ctr` - クリックスルー率）
- `position` - Average position （日本語訳：`position` - 平均掲載順位）

## Filters （日本語訳：フィルター）

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

## When to Use （日本語訳：いつ使用するか）

- Analyzing search performance （日本語訳：検索パフォーマンスの分析）
- Finding keyword opportunities （日本語訳：キーワードの機会を見つける）
- Monitoring indexing status （日本語訳：インデックス作成ステータスの監視）
- Submitting new pages for indexing （日本語訳：インデックス作成のために新しいページを送信する）
- Identifying crawl issues （日本語訳：クロールの問題の特定）
- Tracking position changes （日本語訳：位置変化の追跡）

## Rate Limits （日本語訳：レート制限）

- 200 queries per minute （日本語訳：1 分あたり 200 クエリ）
- 1,200 requests per minute （日本語訳：1 分あたり 1,200 リクエスト）

## Relevant Skills （日本語訳：関連するスキル）

- seo-audit （日本語訳：SEO監査）
- programmatic-seo （日本語訳：プログラマティックSEO）
- analytics-tracking （日本語訳：分析追跡）
