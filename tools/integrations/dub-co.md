# Dub.co （日本語訳：ダブコ）

Link management and attribution platform for modern marketing teams. （日本語訳：最新のマーケティング チーム向けのリンク管理およびアトリビューション プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for links, analytics, domains（日本語訳：リンク、分析、ドメイン用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | TypeScript SDK available（日本語訳：TypeScript SDK が利用可能） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API Keys in Dub dashboard （日本語訳：**キーの取得**: Dub ダッシュボードの [設定] > [API キー]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Create short link （日本語訳：短いリンクを作成する）

```bash
POST https://api.dub.co/links

{
  "url": "https://example.com/landing-page",
  "domain": "link.example.com",
  "key": "summer-sale",
  "tags": ["campaign:summer", "channel:email"]
}
```

### Get link by key （日本語訳：キーによるリンクの取得）

```bash
GET https://api.dub.co/links?domain=link.example.com&key=summer-sale
```

### List links （日本語訳：リストリンク）

```bash
GET https://api.dub.co/links?domain=link.example.com&page=1
```

### Get link analytics （日本語訳：リンク分析を取得する）

```bash
GET https://api.dub.co/analytics?domain=link.example.com&key=summer-sale&interval=30d
```

### Get clicks by location （日本語訳：場所ごとにクリック数を取得する）

```bash
GET https://api.dub.co/analytics/country?domain=link.example.com&key=summer-sale
```

### Get clicks by device （日本語訳：デバイスごとのクリック数を取得する）

```bash
GET https://api.dub.co/analytics/device?domain=link.example.com&key=summer-sale
```

### Update link （日本語訳：リンクを更新する）

```bash
PATCH https://api.dub.co/links/{link_id}

{
  "url": "https://example.com/new-landing-page",
  "tags": ["campaign:summer", "channel:social"]
}
```

### Delete link （日本語訳：リンクを削除）

```bash
DELETE https://api.dub.co/links/{link_id}
```

### Bulk create links （日本語訳：リンクを一括作成）

```bash
POST https://api.dub.co/links/bulk

[
  {"url": "https://example.com/page1", "key": "page1"},
  {"url": "https://example.com/page2", "key": "page2"}
]
```

## TypeScript SDK （日本語訳：TypeScript SDK）

### Install （日本語訳：インストール）

```bash
npm install dub
```

### Usage （日本語訳：使用法）

```typescript
import { Dub } from "dub";

const dub = new Dub({ token: "YOUR_API_KEY" });

// Create link
const link = await dub.links.create({
  url: "https://example.com",
  domain: "link.example.com"
});

// Get analytics
const analytics = await dub.analytics.retrieve({
  domain: "link.example.com",
  key: "summer-sale"
});
```

## Key Features （日本語訳：主な特長）

- **Custom domains** - Use your own branded domains （日本語訳：**カスタム ドメイン** - 独自のブランド ドメインを使用します）
- **Link analytics** - Clicks, locations, devices, referrers （日本語訳：**リンク分析** - クリック数、場所、デバイス、参照元）
- **Tags** - Organize links by campaign, channel, etc. （日本語訳：**タグ** - キャンペーン、チャネルなどごとにリンクを整理します。）
- **QR codes** - Auto-generated for each link （日本語訳：**QR コード** - 各リンクに対して自動生成されます）
- **Password protection** - Secure sensitive links （日本語訳：**パスワード保護** - 機密リンクを保護します）
- **Expiration** - Time-limited links （日本語訳：**有効期限** - 期間限定リンク）
- **Geo-targeting** - Redirect based on location （日本語訳：**地域ターゲティング** - 場所に基づいたリダイレクト）

## Analytics Dimensions （日本語訳：分析のディメンション）

- `clicks` - Total click count （日本語訳：`clicks` - 合計クリック数）
- `country` - Clicks by country （日本語訳：`country` - 国別のクリック数）
- `city` - Clicks by city （日本語訳：`city` - 都市別のクリック数）
- `device` - Clicks by device type （日本語訳：`device` - デバイスの種類別のクリック数）
- `browser` - Clicks by browser （日本語訳：`browser` - ブラウザ別のクリック数）
- `os` - Clicks by operating system （日本語訳：`os` - オペレーティング システム別のクリック数）
- `referer` - Clicks by referrer （日本語訳：`referer` - 参照元によるクリック数）

## When to Use （日本語訳：いつ使用するか）

- Creating trackable marketing links （日本語訳：追跡可能なマーケティングリンクの作成）
- Building referral link systems （日本語訳：紹介リンクシステムの構築）
- Tracking campaign attribution （日本語訳：キャンペーンのアトリビューションの追跡）
- A/B testing landing pages via links （日本語訳：リンクを介したランディング ページの A/B テスト）
- Generating branded short URLs （日本語訳：ブランドの短縮URLの生成）
- Analyzing link performance （日本語訳：リンクパフォーマンスの分析）

## Rate Limits （日本語訳：レート制限）

- Free: 1,000 links, 5 API requests/second （日本語訳：無料: 1,000 リンク、5 API リクエスト/秒）
- Pro: Unlimited links, 50 API requests/second （日本語訳：Pro: 無制限のリンク、50 API リクエスト/秒）
- Enterprise: Custom limits （日本語訳：エンタープライズ: カスタム制限）

## Relevant Skills （日本語訳：関連するスキル）

- referral-program （日本語訳：紹介プログラム）
- analytics-tracking （日本語訳：分析追跡）
- paid-ads （日本語訳：有料広告）
