# TikTok Ads （TikTok広告）

Advertising platform for TikTok's short-form video audience. （TikTok の短編動画視聴者向けの広告プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Marketing API for campaigns, audiences, reporting（キャンペーン、オーディエンス、レポート用のマーケティング API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | Python SDK available（Python SDKが利用可能） |

## Authentication （認証）

- **Type**: Access Token （**タイプ**: アクセストークン）
- **Header**: `Access-Token: {access_token}` （**ヘッダー**: `Access-Token: {access_token}`）
- **Setup**: Create app in TikTok for Business, get access token （**セットアップ**: TikTok for Businessでアプリを作成し、アクセストークンを取得します）

## Common Agent Operations （エージェントの共通操作）

### Get advertiser info （広告主情報を取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/advertiser/info/?advertiser_ids=["{advertiser_id}"]

Access-Token: {access_token}
```

### Get campaigns （キャンペーンを取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/campaign/get/?advertiser_id={advertiser_id}&page=1&page_size=20

Access-Token: {access_token}
```

### Get campaign report （キャンペーンレポートを入手する）

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

### Create campaign （キャンペーンの作成）

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

### Update campaign status （キャンペーンステータスを更新する）

```bash
POST https://business-api.tiktok.com/open_api/v1.3/campaign/status/update/

Access-Token: {access_token}

{
  "advertiser_id": "{advertiser_id}",
  "campaign_ids": ["{campaign_id}"],
  "opt_status": "ENABLE"
}
```

### Get ad groups （広告グループを取得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/adgroup/get/?advertiser_id={advertiser_id}&campaign_ids=["{campaign_id}"]

Access-Token: {access_token}
```

### Get audiences （視聴者を獲得する）

```bash
GET https://business-api.tiktok.com/open_api/v1.3/dmp/custom_audience/list/?advertiser_id={advertiser_id}

Access-Token: {access_token}
```

## Key Metrics （主要な指標）

| Metric（メトリック） | Description（説明） |
|--------|-------------|
| `spend`（__コード0__） | Amount spent（使用金額） |
| `impressions`（__コード0__） | Ad impressions（広告のインプレッション数） |
| `clicks`（__コード0__） | Clicks（クリック数） |
| `ctr`（__コード0__） | Click-through rate（クリックスルー率） |
| `cpc`（__コード0__） | Cost per click（クリックあたりのコスト） |
| `cpm`（__コード0__） | Cost per 1000 impressions（1000 インプレッションあたりのコスト） |
| `conversion`（__コード0__） | Conversions（コンバージョン） |
| `cost_per_conversion`（__コード0__） | CPA（公認会計士） |
| `video_play_actions`（__コード0__） | Video views（ビデオの再生回数） |
| `video_watched_6s`（__コード0__） | 6s views（6秒のビュー） |

## Campaign Objectives （キャンペーンの目的）

- `REACH` - Brand awareness （`REACH` - ブランド認知度）
- `TRAFFIC` - Website traffic （`TRAFFIC` - Web サイトのトラフィック）
- `VIDEO_VIEWS` - Video views （`VIDEO_VIEWS` - ビデオの再生回数）
- `LEAD_GENERATION` - Lead forms （`LEAD_GENERATION` - リードフォーム）
- `CONVERSIONS` - Website conversions （`CONVERSIONS` - ウェブサイトのコンバージョン）
- `APP_PROMOTION` - App installs （`APP_PROMOTION` - アプリのインストール）

## Targeting Options （ターゲティングオプション）

### Demographics （人口統計）
- Age ranges （年齢層）
- Gender （性別）
- Languages （言語）
- Locations （所在地）

### Interests & Behavior （興味と行動）
- Interest categories （興味のあるカテゴリ）
- Video interactions （ビデオインタラクション）
- Creator interactions （クリエイターとの交流）
- Hashtag interactions （ハッシュタグのインタラクション）

### Custom Audiences （カスタムオーディエンス）
- Customer file uploads （顧客ファイルのアップロード）
- Website visitors (pixel) （ウェブサイト訪問者 (ピクセル)）
- App activity （アプリのアクティビティ）
- Engagement audiences （エンゲージメントの対象者）

## When to Use （いつ使用するか）

- Reaching younger demographics (18-34) （より若い層（18 ～ 34 歳）にリーチする）
- Video-first advertising （ビデオファースト広告）
- Viral/creative campaigns （バイラル/クリエイティブ キャンペーン）
- App promotion （アプリのプロモーション）

## Rate Limits （レート制限）

- 10 requests/second （10 リクエスト/秒）
- 100,000 requests/day （100,000 リクエスト/日）

## Relevant Skills （関連するスキル）

- paid-ads （有料広告）
- analytics-tracking （分析追跡）
