# Meta Ads (Facebook/Instagram) （メタ広告 (Facebook/Instagram)）

Advertising platform for Facebook, Instagram, Messenger, and Audience Network. （Facebook、Instagram、メッセンジャー、オーディエンス ネットワークの広告プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Marketing API for campaigns, audiences, reporting（キャンペーン、オーディエンス、レポート用のマーケティング API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | Official SDKs for Python, PHP, Node.js（Python、PHP、Node.js 用の公式 SDK） |

## Authentication （認証）

- **Type**: OAuth 2.0 Access Token （**タイプ**: OAuth 2.0 アクセス トークン）
- **Header**: Access token as query parameter （**ヘッダー**: クエリパラメータとしてのアクセストークン）
- **Setup**: Create app in Meta Business Suite, generate System User token （**セットアップ**: Meta Business Suite でアプリを作成し、システム ユーザー トークンを生成します）

## Common Agent Operations （エージェントの共通操作）

### Get ad accounts （広告アカウントを取得する）

```bash
GET https://graph.facebook.com/v18.0/me/adaccounts?access_token={access_token}&fields=id,name,account_status
```

### Get campaigns （キャンペーンを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/campaigns?access_token={access_token}&fields=id,name,status,objective,daily_budget
```

### Get campaign insights （キャンペーンに関する洞察を得る）

```bash
GET https://graph.facebook.com/v18.0/{campaign_id}/insights?access_token={access_token}&fields=impressions,clicks,spend,actions,cost_per_action_type&date_preset=last_30d
```

### Get ad sets （広告セットを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/adsets?access_token={access_token}&fields=id,name,status,targeting,daily_budget,bid_amount
```

### Get ads （広告を取得する）

```bash
GET https://graph.facebook.com/v18.0/{ad_set_id}/ads?access_token={access_token}&fields=id,name,status,creative
```

### Create campaign （キャンペーンの作成）

```bash
POST https://graph.facebook.com/v18.0/act_{ad_account_id}/campaigns

access_token={access_token}
&name=Campaign Name
&objective=CONVERSIONS
&status=PAUSED
&special_ad_categories=[]
```

### Update campaign status （キャンペーンステータスを更新する）

```bash
POST https://graph.facebook.com/v18.0/{campaign_id}

access_token={access_token}
&status=ACTIVE
```

### Get custom audiences （カスタム オーディエンスを取得する）

```bash
GET https://graph.facebook.com/v18.0/act_{ad_account_id}/customaudiences?access_token={access_token}&fields=id,name,approximate_count
```

### Create lookalike audience （類似視聴者を作成する）

```bash
POST https://graph.facebook.com/v18.0/act_{ad_account_id}/customaudiences

access_token={access_token}
&name=Lookalike - Top Customers
&subtype=LOOKALIKE
&origin_audience_id={source_audience_id}
&lookalike_spec={"type":"similarity","country":"US"}
```

## Key Metrics （主要な指標）

| Metric（メトリック） | Description（説明） |
|--------|-------------|
| `impressions`（__コード0__） | Ad impressions（広告のインプレッション数） |
| `clicks`（__コード0__） | All clicks（すべてのクリック） |
| `spend`（__コード0__） | Amount spent（使用金額） |
| `reach`（__コード0__） | Unique people reached（ユニークな人々が到達） |
| `frequency`（__コード0__） | Avg impressions per person（1 人あたりの平均インプレッション数） |
| `cpm`（__コード0__） | Cost per 1000 impressions（1000 インプレッションあたりのコスト） |
| `cpc`（__コード0__） | Cost per click（クリックあたりのコスト） |
| `actions`（__コード0__） | Conversions array（変換配列） |
| `cost_per_action_type`（__コード0__） | CPA by action（アクション別の CPA） |

## Campaign Objectives （キャンペーンの目的）

- `AWARENESS` - Brand awareness （`AWARENESS` - ブランド認知度）
- `TRAFFIC` - Website traffic （`TRAFFIC` - Web サイトのトラフィック）
- `ENGAGEMENT` - Post engagement （`ENGAGEMENT` - エンゲージメント後）
- `LEADS` - Lead generation （`LEADS` - 見込み客の発掘）
- `APP_PROMOTION` - App installs （`APP_PROMOTION` - アプリのインストール）
- `SALES` - Conversions/catalog sales （`SALES` - コンバージョン/カタログ販売）

## Targeting Options （ターゲティングオプション）

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

## When to Use （いつ使用するか）

- Creating/managing Facebook and Instagram ads （FacebookおよびInstagram広告の作成/管理）
- Audience targeting and lookalikes （視聴者ターゲティングと類似商品）
- Campaign performance analysis （キャンペーンのパフォーマンス分析）
- Retargeting setup （リターゲティング設定）

## Rate Limits （レート制限）

- 200 calls/hour per ad account （広告アカウントごとに 200 件の通話/時間）
- 60 calls/hour for marketing API （マーケティング API の場合、1 時間あたり 60 件の呼び出し）
- Use batch requests for efficiency （バッチリクエストを使用して効率化する）

## Relevant Skills （関連するスキル）

- paid-ads （有料広告）
- analytics-tracking （分析追跡）
- page-cro （ページクロ）
