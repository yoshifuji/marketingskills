# Webflow （日本語訳：ウェブフロー）

Visual web design and CMS platform for marketing sites. （日本語訳：マーケティング サイト向けのビジュアル Web デザインと CMS プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for sites, CMS, forms（日本語訳：サイト、CMS、フォーム用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | Webflow CLI for devlink and apps（日本語訳：devlink とアプリ用の Webflow CLI） |
| SDK（日本語訳：SDK） | ✓ | Official SDK for Node.js（日本語訳：Node.js の公式 SDK） |

## Authentication （日本語訳：認証）

- **Type**: API Token (Site token or OAuth) （日本語訳：**タイプ**: API トークン (サイト トークンまたは OAuth)）
- **Header**: `Authorization: Bearer {api_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_token}`）
- **Get token**: Site Settings > Integrations > API Access （日本語訳：**トークンの取得**: [サイト設定] > [統合] > [API アクセス]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List sites （日本語訳：サイトをリストする）

```bash
GET https://api.webflow.com/v2/sites

Authorization: Bearer {api_token}
```

### Get site （日本語訳：サイトを取得）

```bash
GET https://api.webflow.com/v2/sites/{site_id}

Authorization: Bearer {api_token}
```

### List collections （日本語訳：コレクションのリスト）

```bash
GET https://api.webflow.com/v2/sites/{site_id}/collections

Authorization: Bearer {api_token}
```

### List collection items （日本語訳：コレクションアイテムをリストアップする）

```bash
GET https://api.webflow.com/v2/collections/{collection_id}/items

Authorization: Bearer {api_token}
```

### Get collection item （日本語訳：コレクションアイテムを入手）

```bash
GET https://api.webflow.com/v2/collections/{collection_id}/items/{item_id}

Authorization: Bearer {api_token}
```

### Create collection item （日本語訳：コレクションアイテムの作成）

```bash
POST https://api.webflow.com/v2/collections/{collection_id}/items

Authorization: Bearer {api_token}

{
  "fieldData": {
    "name": "Item Name",
    "slug": "item-name",
    "custom-field": "value"
  }
}
```

### Update collection item （日本語訳：コレクションアイテムを更新）

```bash
PATCH https://api.webflow.com/v2/collections/{collection_id}/items/{item_id}

Authorization: Bearer {api_token}

{
  "fieldData": {
    "custom-field": "new value"
  }
}
```

### Publish collection items （日本語訳：コレクションアイテムを公開する）

```bash
POST https://api.webflow.com/v2/collections/{collection_id}/items/publish

Authorization: Bearer {api_token}

{
  "itemIds": ["item_id_1", "item_id_2"]
}
```

### List form submissions （日本語訳：フォーム送信の一覧表示）

```bash
GET https://api.webflow.com/v2/sites/{site_id}/forms/{form_id}/submissions

Authorization: Bearer {api_token}
```

### Publish site （日本語訳：サイトを公開する）

```bash
POST https://api.webflow.com/v2/sites/{site_id}/publish

Authorization: Bearer {api_token}

{
  "publishToWebflowSubdomain": true,
  "publishToCustomDomains": true
}
```

## Node.js SDK （日本語訳：Node.js SDK）

```javascript
const Webflow = require('webflow-api');

const webflow = new Webflow({ token: 'api_token' });

// List sites
const sites = await webflow.sites.list();

// Get collection items
const items = await webflow.collections.items.listItems(collectionId);

// Create item
const item = await webflow.collections.items.createItem(collectionId, {
  fieldData: {
    name: 'New Item',
    slug: 'new-item'
  }
});
```

## CLI Commands （日本語訳：CLIコマンド）

```bash
# Install
npm install -g @webflow/webflow-cli

# Login
webflow login

# Initialize devlink
webflow devlink init

# Sync components
webflow devlink sync
```

## CMS Structure （日本語訳：CMSの構造）

- **Collections** - Content types (like blog posts, team members) （日本語訳：**コレクション** - コンテンツ タイプ (ブログ投稿、チーム メンバーなど)）
- **Items** - Individual entries in a collection （日本語訳：**アイテム** - コレクション内の個々のエントリ）
- **Fields** - Data fields on items （日本語訳：**フィールド** - アイテムのデータ フィールド）

## Common Field Types （日本語訳：一般的なフィールドの種類）

- `PlainText` - Simple text （日本語訳：`PlainText` - 単純なテキスト）
- `RichText` - Formatted content （日本語訳：`RichText` - フォーマットされたコンテンツ）
- `Image` - Image upload （日本語訳：`Image` - 画像のアップロード）
- `Link` - URL or page reference （日本語訳：`Link` - URL またはページ参照）
- `Reference` - Link to another collection （日本語訳：`Reference` - 別のコレクションへのリンク）
- `Multi-Reference` - Multiple collection links （日本語訳：`Multi-Reference` - 複数のコレクション リンク）
- `Switch` - Boolean toggle （日本語訳：`Switch` - ブール値の切り替え）
- `Number` - Numeric value （日本語訳：`Number` - 数値）
- `Date` - Date/time （日本語訳：`Date` - 日付/時刻）

## When to Use （日本語訳：いつ使用するか）

- Marketing site CMS management （日本語訳：マーケティングサイトのCMS管理）
- Blog/content publishing （日本語訳：ブログ/コンテンツの公開）
- Form submission handling （日本語訳：フォーム送信の処理）
- Automated content updates （日本語訳：コンテンツの自動更新）
- Programmatic SEO pages （日本語訳：プログラマティックSEOページ）

## Rate Limits （日本語訳：レート制限）

- 60 requests/minute (general) （日本語訳：60 リクエスト/分 (一般)）
- 10 requests/minute (publishing) （日本語訳：10 リクエスト/分 (パブリッシュ)）

## Relevant Skills （日本語訳：関連するスキル）

- programmatic-seo （日本語訳：プログラマティックSEO）
- content-strategy （日本語訳：コンテンツ戦略）
- page-cro （日本語訳：ページクロ）
