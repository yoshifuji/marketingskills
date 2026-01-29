# Dub.co （ダブコ）

Link management and attribution platform for modern marketing teams. （最新のマーケティング チーム向けのリンク管理およびアトリビューション プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for links, analytics, domains（リンク、分析、ドメイン用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | TypeScript SDK available（TypeScript SDK が利用可能） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API Keys in Dub dashboard （**キーの取得**: Dub ダッシュボードの [設定] > [API キー]）

## Common Agent Operations （エージェントの共通操作）

### Create short link （短いリンクを作成する）

```bash
POST https://api.dub.co/links

{
  "url": "https://example.com/landing-page",
  "domain": "link.example.com",
  "key": "summer-sale",
  "tags": ["campaign:summer", "channel:email"]
}
```

### Get link by key （キーによるリンクの取得）

```bash
GET https://api.dub.co/links?domain=link.example.com&key=summer-sale
```

### List links （リストリンク）

```bash
GET https://api.dub.co/links?domain=link.example.com&page=1
```

### Get link analytics （リンク分析を取得する）

```bash
GET https://api.dub.co/analytics?domain=link.example.com&key=summer-sale&interval=30d
```

### Get clicks by location （場所ごとにクリック数を取得する）

```bash
GET https://api.dub.co/analytics/country?domain=link.example.com&key=summer-sale
```

### Get clicks by device （デバイスごとのクリック数を取得する）

```bash
GET https://api.dub.co/analytics/device?domain=link.example.com&key=summer-sale
```

### Update link （リンクを更新する）

```bash
PATCH https://api.dub.co/links/{link_id}

{
  "url": "https://example.com/new-landing-page",
  "tags": ["campaign:summer", "channel:social"]
}
```

### Delete link （リンクを削除）

```bash
DELETE https://api.dub.co/links/{link_id}
```

### Bulk create links （リンクを一括作成）

```bash
POST https://api.dub.co/links/bulk

[
  {"url": "https://example.com/page1", "key": "page1"},
  {"url": "https://example.com/page2", "key": "page2"}
]
```

## TypeScript SDK （TypeScript SDK）

### Install （インストール）

```bash
npm install dub
```

### Usage （使用法）

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

## Key Features （主な特長）

- **Custom domains** - Use your own branded domains （**カスタム ドメイン** - 独自のブランド ドメインを使用します）
- **Link analytics** - Clicks, locations, devices, referrers （**リンク分析** - クリック数、場所、デバイス、参照元）
- **Tags** - Organize links by campaign, channel, etc. （**タグ** - キャンペーン、チャネルなどごとにリンクを整理します。）
- **QR codes** - Auto-generated for each link （**QR コード** - 各リンクに対して自動生成されます）
- **Password protection** - Secure sensitive links （**パスワード保護** - 機密リンクを保護します）
- **Expiration** - Time-limited links （**有効期限** - 期間限定リンク）
- **Geo-targeting** - Redirect based on location （**地域ターゲティング** - 場所に基づいたリダイレクト）

## Analytics Dimensions （分析のディメンション）

- `clicks` - Total click count （`clicks` - 合計クリック数）
- `country` - Clicks by country （`country` - 国別のクリック数）
- `city` - Clicks by city （`city` - 都市別のクリック数）
- `device` - Clicks by device type （`device` - デバイスの種類別のクリック数）
- `browser` - Clicks by browser （`browser` - ブラウザ別のクリック数）
- `os` - Clicks by operating system （`os` - オペレーティング システム別のクリック数）
- `referer` - Clicks by referrer （`referer` - 参照元によるクリック数）

## When to Use （いつ使用するか）

- Creating trackable marketing links （追跡可能なマーケティングリンクの作成）
- Building referral link systems （紹介リンクシステムの構築）
- Tracking campaign attribution （キャンペーンのアトリビューションの追跡）
- A/B testing landing pages via links （リンクを介したランディング ページの A/B テスト）
- Generating branded short URLs （ブランドの短縮URLの生成）
- Analyzing link performance （リンクパフォーマンスの分析）

## Rate Limits （レート制限）

- Free: 1,000 links, 5 API requests/second （無料: 1,000 リンク、5 API リクエスト/秒）
- Pro: Unlimited links, 50 API requests/second （Pro: 無制限のリンク、50 API リクエスト/秒）
- Enterprise: Custom limits （エンタープライズ: カスタム制限）

## Relevant Skills （関連するスキル）

- referral-program （紹介プログラム）
- analytics-tracking （分析追跡）
- paid-ads （有料広告）
