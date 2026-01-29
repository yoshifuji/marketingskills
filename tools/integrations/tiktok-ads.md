# TikTok Ads （日本語訳：TikTok広告）

Advertising platform for TikTok's short-form video audience. （日本語訳：TikTok の短編動画視聴者向けの広告プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Marketing API for campaigns, audiences, reporting（日本語訳：キャンペーン、オーディエンス、レポート用のマーケティング API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | Python SDK available（日本語訳：Python SDKが利用可能） |

## Authentication （日本語訳：認証）

- **Type**: Access Token （日本語訳：**タイプ**: アクセストークン）
- **Header**: `Access-Token: {access_token}` （日本語訳：**ヘッダー**: `Access-Token: {access_token}`）
- **Setup**: Create app in TikTok for Business, get access token （日本語訳：**セットアップ**: TikTok for Businessでアプリを作成し、アクセストークンを取得します）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get advertiser info （日本語訳：広告主情報を取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/advertiser/info/?advertiser_ids=["{advertiser_id}"]

Access-Token: {access_token}
```

### Get campaigns （日本語訳：キャンペーンを取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/campaign/get/?advertiser_id={advertiser_id}&page=1&page_size=20

Access-Token: {access_token}
```

### Get campaign report （日本語訳：キャンペーンレポートを入手する）

```bash
POST https://business-api.tiktok.com/open_api/v1.3/report/integrated/get/

Access-Token: {access_token}

{
  "advertiser_id": "{advertiser_id}",
  "report_type": "BASIC",
  "dimensions": ["campaign_id"],
  "metrics": ["spend", "impressions", "clicks", "conversion"],
  "data_level": "AUCTION_CAMPAIGN",
  "start_date": "2024-01-01",
  "end_date": "2024-01-31"
}
```

### Create campaign （日本語訳：キャンペーンの作成）

```bash
POST https://business-api.tiktok.com/open_api/v1.3/campaign/create/

Access-Token: {access_token}

{
  "advertiser_id": "{advertiser_id}",
  "campaign_name": "Campaign Name",
  "objective_type": "CONVERSIONS",
  "budget_mode": "BUDGET_MODE_DAY",
  "budget": 100
}
```

### Update campaign status （日本語訳：キャンペーンステータスを更新する）

```bash
POST https://business-api.tiktok.com/open_api/v1.3/campaign/status/update/

Access-Token: {access_token}

{
  "advertiser_id": "{advertiser_id}",
  "campaign_ids": ["{campaign_id}"],
  "opt_status": "ENABLE"
}
```

### Get ad groups （日本語訳：広告グループを取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/adgroup/get/?advertiser_id={advertiser_id}&campaign_ids=["{campaign_id}"]

Access-Token: {access_token}
```

### Get audiences （日本語訳：視聴者を獲得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/dmp/custom_audience/list/?advertiser_id={advertiser_id}

Access-Token: {access_token}
```

## Key Metrics （日本語訳：主要な指標）

| Metric（日本語訳：メトリック） | Description（日本語訳：説明） |
|--------|-------------|
| `spend`（日本語訳：__コード0__） | Amount spent（日本語訳：使用金額） |
| `impressions`（日本語訳：__コード0__） | Ad impressions（日本語訳：広告のインプレッション数） |
| `clicks`（日本語訳：__コード0__） | Clicks（日本語訳：クリック数） |
| `ctr`（日本語訳：__コード0__） | Click-through rate（日本語訳：クリックスルー率） |
| `cpc`（日本語訳：__コード0__） | Cost per click（日本語訳：クリックあたりのコスト） |
| `cpm`（日本語訳：__コード0__） | Cost per 1000 impressions（日本語訳：1000 インプレッションあたりのコスト） |
| `conversion`（日本語訳：__コード0__） | Conversions（日本語訳：コンバージョン） |
| `cost_per_conversion`（日本語訳：__コード0__） | CPA（日本語訳：公認会計士） |
| `video_play_actions`（日本語訳：__コード0__） | Video views（日本語訳：ビデオの再生回数） |
| `video_watched_6s`（日本語訳：__コード0__） | 6s views（日本語訳：6秒のビュー） |

## Campaign Objectives （日本語訳：キャンペーンの目的）

- `REACH` - Brand awareness （日本語訳：`REACH` - ブランド認知度）
- `TRAFFIC` - Website traffic （日本語訳：`TRAFFIC` - Web サイトのトラフィック）
- `VIDEO_VIEWS` - Video views （日本語訳：`VIDEO_VIEWS` - ビデオの再生回数）
- `LEAD_GENERATION` - Lead forms （日本語訳：`LEAD_GENERATION` - リードフォーム）
- `CONVERSIONS` - Website conversions （日本語訳：`CONVERSIONS` - ウェブサイトのコンバージョン）
- `APP_PROMOTION` - App installs （日本語訳：`APP_PROMOTION` - アプリのインストール）

## Targeting Options （日本語訳：ターゲティングオプション）

### Demographics （日本語訳：人口統計）
- Age ranges （日本語訳：年齢層）
- Gender （日本語訳：性別）
- Languages （日本語訳：言語）
- Locations （日本語訳：所在地）

### Interests & Behavior （日本語訳：興味と行動）
- Interest categories （日本語訳：興味のあるカテゴリ）
- Video interactions （日本語訳：ビデオインタラクション）
- Creator interactions （日本語訳：クリエイターとの交流）
- Hashtag interactions （日本語訳：ハッシュタグのインタラクション）

### Custom Audiences （日本語訳：カスタムオーディエンス）
- Customer file uploads （日本語訳：顧客ファイルのアップロード）
- Website visitors (pixel) （日本語訳：ウェブサイト訪問者 (ピクセル)）
- App activity （日本語訳：アプリのアクティビティ）
- Engagement audiences （日本語訳：エンゲージメントの対象者）

## When to Use （日本語訳：いつ使用するか）

- Reaching younger demographics (18-34) （日本語訳：より若い層（18 ～ 34 歳）にリーチする）
- Video-first advertising （日本語訳：ビデオファースト広告）
- Viral/creative campaigns （日本語訳：バイラル/クリエイティブ キャンペーン）
- App promotion （日本語訳：アプリのプロモーション）

## Rate Limits （日本語訳：レート制限）

- 10 requests/second （日本語訳：10 リクエスト/秒）
- 100,000 requests/day （日本語訳：100,000 リクエスト/日）

## Relevant Skills （日本語訳：関連するスキル）

- paid-ads （日本語訳：有料広告）
- analytics-tracking （日本語訳：分析追跡）
