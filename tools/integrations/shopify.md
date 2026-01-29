# Shopify （ショッピファイ）

E-commerce platform for online stores and retail. （オンラインストアや小売店向けの電子商取引プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST Admin API, Storefront API, GraphQL（REST管理API、ストアフロントAPI、GraphQL） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | Shopify CLI for themes and apps（テーマとアプリ用の Shopify CLI） |
| SDK（SDK） | ✓ | Official libraries for multiple languages（多言語の公式ライブラリ） |

## Authentication （認証）

- **Type**: Access Token (Custom App or OAuth) （**タイプ**: アクセス トークン (カスタム アプリまたは OAuth)）
- **Header**: `X-Shopify-Access-Token: {access_token}` （**ヘッダー**: `X-Shopify-Access-Token: {access_token}`）
- **Base URL**: `https://{shop}.myshopify.com/admin/api/2024-01/` （**ベース URL**: `https://{shop}.myshopify.com/admin/api/2024-01/`）

## Common Agent Operations （エージェントの共通操作）

### Get shop info （ショップ情報を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/shop.json

X-Shopify-Access-Token: {access_token}
```

### List products （製品一覧）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/products.json?limit=50

X-Shopify-Access-Token: {access_token}
```

### Get product （製品を入手）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/products/{product_id}.json

X-Shopify-Access-Token: {access_token}
```

### Create product （製品を作成する）

```bash
POST https://{shop}.myshopify.com/admin/api/2024-01/products.json

X-Shopify-Access-Token: {access_token}

{
  "product": {
    "title": "Product Name",
    "body_html": "<p>Description</p>",
    "vendor": "Brand",
    "product_type": "Category",
    "variants": [{
      "price": "99.00",
      "sku": "SKU-001"
    }]
  }
}
```

### List orders （注文をリストアップする）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/orders.json?status=any&limit=50

X-Shopify-Access-Token: {access_token}
```

### Get order （注文を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/orders/{order_id}.json

X-Shopify-Access-Token: {access_token}
```

### List customers （顧客をリストアップする）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/customers.json?limit=50

X-Shopify-Access-Token: {access_token}
```

### Search customers （顧客を検索する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/customers/search.json?query=email:user@example.com

X-Shopify-Access-Token: {access_token}
```

### Get analytics （分析を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/reports.json

X-Shopify-Access-Token: {access_token}
```

## GraphQL API （GraphQL API）

```graphql
{
  products(first: 10) {
    edges {
      node {
        id
        title
        totalInventory
        priceRangeV2 {
          minVariantPrice {
            amount
          }
        }
      }
    }
  }
}
```

## CLI Commands （CLIコマンド）

```bash
# Login
shopify login --store={shop}

# Create theme
shopify theme init

# Push theme
shopify theme push

# Preview theme
shopify theme dev

# Create app
shopify app create node
```

## Webhook Topics （Webhook トピック）

| Topic（トピック） | When（いつ） |
|-------|------|
| `orders/create`（__コード0__） | New order（新規注文） |
| `orders/paid`（__コード0__） | Order paid（注文が支払われた） |
| `orders/fulfilled`（__コード0__） | Order shipped（注文品が発送されました） |
| `customers/create`（__コード0__） | New customer（新規のお客様） |
| `products/update`（__コード0__） | Product changed（製品が変更されました） |
| `checkouts/create`（__コード0__） | Checkout started（チェックアウトが開始されました） |

## When to Use （いつ使用するか）

- E-commerce store management （ECストア運営）
- Product catalog operations （商品カタログ業務）
- Order processing （注文処理）
- Customer data management （顧客データ管理）
- Inventory tracking （在庫追跡）

## Rate Limits （レート制限）

- REST: 2 requests/second （REST: 2 リクエスト/秒）
- GraphQL: 50 points/second （GraphQL: 50 ポイント/秒）
- Bulk operations available （一括操作が可能）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- email-sequence （電子メールシーケンス）
- referral-program （紹介プログラム）
