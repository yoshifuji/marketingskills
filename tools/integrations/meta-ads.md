# Meta Ads (Facebook/Instagram) （日本語訳：メタ広告 (Facebook/Instagram)）

Advertising platform for Facebook, Instagram, Messenger, and Audience Network. （日本語訳：Facebook、Instagram、メッセンジャー、オーディエンス ネットワークの広告プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Marketing API for campaigns, audiences, reporting（日本語訳：キャンペーン、オーディエンス、レポート用のマーケティング API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | Official SDKs for Python, PHP, Node.js（日本語訳：Python、PHP、Node.js 用の公式 SDK） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 Access Token （日本語訳：**タイプ**: OAuth 2.0 アクセス トークン）
- **Header**: Access token as query parameter （日本語訳：**ヘッダー**: クエリパラメータとしてのアクセストークン）
- **Setup**: Create app in Meta Business Suite, generate System User token （日本語訳：**セットアップ**: Meta Business Suite でアプリを作成し、システム ユーザー トークンを生成します）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get ad accounts （日本語訳：広告アカウントを取得する）

```bash
GET https://graph.facebook.com/v18.0/me/adaccounts?access_token={access_token}&fields=id,name,account_status
```

### Get campaigns （日本語訳：キャンペーンを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/campaigns?access_token={access_token}&fields=id,name,status,objective,daily_budget
```

### Get campaign insights （日本語訳：キャンペーンに関する洞察を得る）

```bash
GET https://graph.facebook.com/v18.0/{campaign_id}/insights?access_token={access_token}&fields=impressions,clicks,spend,actions,cost_per_action_type&date_preset=last_30d
```

### Get ad sets （日本語訳：広告セットを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/adsets?access_token={access_token}&fields=id,name,status,targeting,daily_budget,bid_amount
```

### Get ads （日本語訳：広告を取得する）

```bash
GET https://graph.facebook.com/v18.0/{ad_set_id}/ads?access_token={access_token}&fields=id,name,status,creative
```

### Create campaign （日本語訳：キャンペーンの作成）

```bash
POST https://graph.facebook.com/v18.0/act_{ad_account_id}/campaigns

access_token={access_token}
&name=Campaign Name
&objective=CONVERSIONS
&status=PAUSED
&special_ad_categories=[]
```

### Update campaign status （日本語訳：キャンペーンステータスを更新する）

```bash
POST https://graph.facebook.com/v18.0/{campaign_id}

access_token={access_token}
&status=ACTIVE
```

### Get custom audiences （日本語訳：カスタム オーディエンスを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/customaudiences?access_token={access_token}&fields=id,name,approximate_count
```

### Create lookalike audience （日本語訳：類似視聴者を作成する）

```bash
POST https://graph.facebook.com/v18.0/act_{ad_account_id}/customaudiences

access_token={access_token}
&name=Lookalike - Top Customers
&subtype=LOOKALIKE
&origin_audience_id={source_audience_id}
&lookalike_spec={"type":"similarity","country":"US"}
```

## Key Metrics （日本語訳：主要な指標）

| Metric（日本語訳：メトリック） | Description（日本語訳：説明） |
|--------|-------------|
| `impressions`（日本語訳：__コード0__） | Ad impressions（日本語訳：広告のインプレッション数） |
| `clicks`（日本語訳：__コード0__） | All clicks（日本語訳：すべてのクリック） |
| `spend`（日本語訳：__コード0__） | Amount spent（日本語訳：使用金額） |
| `reach`（日本語訳：__コード0__） | Unique people reached（日本語訳：ユニークな人々が到達） |
| `frequency`（日本語訳：__コード0__） | Avg impressions per person（日本語訳：1 人あたりの平均インプレッション数） |
| `cpm`（日本語訳：__コード0__） | Cost per 1000 impressions（日本語訳：1000 インプレッションあたりのコスト） |
| `cpc`（日本語訳：__コード0__） | Cost per click（日本語訳：クリックあたりのコスト） |
| `actions`（日本語訳：__コード0__） | Conversions array（日本語訳：変換配列） |
| `cost_per_action_type`（日本語訳：__コード0__） | CPA by action（日本語訳：アクション別の CPA） |

## Campaign Objectives （日本語訳：キャンペーンの目的）

- `AWARENESS` - Brand awareness （日本語訳：`AWARENESS` - ブランド認知度）
- `TRAFFIC` - Website traffic （日本語訳：`TRAFFIC` - Web サイトのトラフィック）
- `ENGAGEMENT` - Post engagement （日本語訳：`ENGAGEMENT` - エンゲージメント後）
- `LEADS` - Lead generation （日本語訳：`LEADS` - 見込み客の発掘）
- `APP_PROMOTION` - App installs （日本語訳：`APP_PROMOTION` - アプリのインストール）
- `SALES` - Conversions/catalog sales （日本語訳：`SALES` - コンバージョン/カタログ販売）

## Targeting Options （日本語訳：ターゲティングオプション）

```json
{
  "geo_locations": {
    "countries": ["US"],
    "cities": [{"key": "2420379"}]
  },
  "age_min": 25,
  "age_max": 45,
  "genders": [1, 2],
  "interests": [{"id": "6003139266461", "name": "Marketing"}],
  "behaviors": [{"id": "6002714895372"}]
}
```

## When to Use （日本語訳：いつ使用するか）

- Creating/managing Facebook and Instagram ads （日本語訳：FacebookおよびInstagram広告の作成/管理）
- Audience targeting and lookalikes （日本語訳：視聴者ターゲティングと類似商品）
- Campaign performance analysis （日本語訳：キャンペーンのパフォーマンス分析）
- Retargeting setup （日本語訳：リターゲティング設定）

## Rate Limits （日本語訳：レート制限）

- 200 calls/hour per ad account （日本語訳：広告アカウントごとに 200 件の通話/時間）
- 60 calls/hour for marketing API （日本語訳：マーケティング API の場合、1 時間あたり 60 件の呼び出し）
- Use batch requests for efficiency （日本語訳：バッチリクエストを使用して効率化する）

## Relevant Skills （日本語訳：関連するスキル）

- paid-ads （日本語訳：有料広告）
- analytics-tracking （日本語訳：分析追跡）
- page-cro （日本語訳：ページクロ）
