# Webflow （ウェブフロー）

Visual web design and CMS platform for marketing sites. （マーケティング サイト向けのビジュアル Web デザインと CMS プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for sites, CMS, forms（サイト、CMS、フォーム用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | Webflow CLI for devlink and apps（devlink とアプリ用の Webflow CLI） |
| SDK（SDK） | ✓ | Official SDK for Node.js（Node.js の公式 SDK） |

## Authentication （認証）

- **Type**: API Token (Site token or OAuth) （**タイプ**: API トークン (サイト トークンまたは OAuth)）
- **Header**: `Authorization: Bearer {api_token}` （**ヘッダー**: `Authorization: Bearer {api_token}`）
- **Get token**: Site Settings > Integrations > API Access （**トークンの取得**: [サイト設定] > [統合] > [API アクセス]）

## Common Agent Operations （エージェントの共通操作）

### List sites （サイトをリストする）

```bash
GET https://api.webflow.com/v2/sites

Authorization: Bearer {api_token}
```

### Get site （サイトを取得）

```bash
GET https://api.webflow.com/v2/sites/{site_id}

Authorization: Bearer {api_token}
```

### List collections （コレクションのリスト）

```bash
GET https://api.webflow.com/v2/sites/{site_id}/collections

Authorization: Bearer {api_token}
```

### List collection items （コレクションアイテムをリストアップする）

```bash
GET https://api.webflow.com/v2/collections/{collection_id}/items

Authorization: Bearer {api_token}
```

### Get collection item （コレクションアイテムを入手）

```bash
GET https://api.webflow.com/v2/collections/{collection_id}/items/{item_id}

Authorization: Bearer {api_token}
```

### Create collection item （コレクションアイテムの作成）

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

### Update collection item （コレクションアイテムを更新）

```bash
PATCH https://api.webflow.com/v2/collections/{collection_id}/items/{item_id}

Authorization: Bearer {api_token}

{
  "fieldData": {
    "custom-field": "new value"
  }
}
```

### Publish collection items （コレクションアイテムを公開する）

```bash
POST https://api.webflow.com/v2/collections/{collection_id}/items/publish

Authorization: Bearer {api_token}

{
  "itemIds": ["item_id_1", "item_id_2"]
}
```

### List form submissions （フォーム送信の一覧表示）

```bash
GET https://api.webflow.com/v2/sites/{site_id}/forms/{form_id}/submissions

Authorization: Bearer {api_token}
```

### Publish site （サイトを公開する）

```bash
POST https://api.webflow.com/v2/sites/{site_id}/publish

Authorization: Bearer {api_token}

{
  "publishToWebflowSubdomain": true,
  "publishToCustomDomains": true
}
```

## Node.js SDK （Node.js SDK）

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

## CLI Commands （CLIコマンド）

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

## CMS Structure （CMSの構造）

- **Collections** - Content types (like blog posts, team members) （**コレクション** - コンテンツ タイプ (ブログ投稿、チーム メンバーなど)）
- **Items** - Individual entries in a collection （**アイテム** - コレクション内の個々のエントリ）
- **Fields** - Data fields on items （**フィールド** - アイテムのデータ フィールド）

## Common Field Types （一般的なフィールドの種類）

- `PlainText` - Simple text （`PlainText` - 単純なテキスト）
- `RichText` - Formatted content （`RichText` - フォーマットされたコンテンツ）
- `Image` - Image upload （`Image` - 画像のアップロード）
- `Link` - URL or page reference （`Link` - URL またはページ参照）
- `Reference` - Link to another collection （`Reference` - 別のコレクションへのリンク）
- `Multi-Reference` - Multiple collection links （`Multi-Reference` - 複数のコレクション リンク）
- `Switch` - Boolean toggle （`Switch` - ブール値の切り替え）
- `Number` - Numeric value （`Number` - 数値）
- `Date` - Date/time （`Date` - 日付/時刻）

## When to Use （いつ使用するか）

- Marketing site CMS management （マーケティングサイトのCMS管理）
- Blog/content publishing （ブログ/コンテンツの公開）
- Form submission handling （フォーム送信の処理）
- Automated content updates （コンテンツの自動更新）
- Programmatic SEO pages （プログラマティックSEOページ）

## Rate Limits （レート制限）

- 60 requests/minute (general) （60 リクエスト/分 (一般)）
- 10 requests/minute (publishing) （10 リクエスト/分 (パブリッシュ)）

## Relevant Skills （関連するスキル）

- programmatic-seo （プログラマティックSEO）
- content-strategy （コンテンツ戦略）
- page-cro （ページクロ）
