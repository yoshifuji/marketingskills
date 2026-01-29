# Shopify （日本語訳：ショッピファイ）

E-commerce platform for online stores and retail. （日本語訳：オンラインストアや小売店向けの電子商取引プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST Admin API, Storefront API, GraphQL（日本語訳：REST管理API、ストアフロントAPI、GraphQL） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | Shopify CLI for themes and apps（日本語訳：テーマとアプリ用の Shopify CLI） |
| SDK（日本語訳：SDK） | ✓ | Official libraries for multiple languages（日本語訳：多言語の公式ライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: Access Token (Custom App or OAuth) （日本語訳：**タイプ**: アクセス トークン (カスタム アプリまたは OAuth)）
- **Header**: `X-Shopify-Access-Token: {access_token}` （日本語訳：**ヘッダー**: `X-Shopify-Access-Token: {access_token}`）
- **Base URL**: `https://{shop}.myshopify.com/admin/api/2024-01/` （日本語訳：**ベース URL**: `https://{shop}.myshopify.com/admin/api/2024-01/`）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get shop info （日本語訳：ショップ情報を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/shop.json

X-Shopify-Access-Token: {access_token}
```

### List products （日本語訳：製品一覧）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/products.json?limit=50

X-Shopify-Access-Token: {access_token}
```

### Get product （日本語訳：製品を入手）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/products/{product_id}.json

X-Shopify-Access-Token: {access_token}
```

### Create product （日本語訳：製品を作成する）

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

### List orders （日本語訳：注文をリストアップする）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/orders.json?status=any&limit=50

X-Shopify-Access-Token: {access_token}
```

### Get order （日本語訳：注文を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/orders/{order_id}.json

X-Shopify-Access-Token: {access_token}
```

### List customers （日本語訳：顧客をリストアップする）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/customers.json?limit=50

X-Shopify-Access-Token: {access_token}
```

### Search customers （日本語訳：顧客を検索する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/customers/search.json?query=email:user@example.com

X-Shopify-Access-Token: {access_token}
```

### Get analytics （日本語訳：分析を取得する）

```bash
GET https://{shop}.myshopify.com/admin/api/2024-01/reports.json

X-Shopify-Access-Token: {access_token}
```

## GraphQL API （日本語訳：GraphQL API）

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

## CLI Commands （日本語訳：CLIコマンド）

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

## Webhook Topics （日本語訳：Webhook トピック）

| Topic（日本語訳：トピック） | When（日本語訳：いつ） |
|-------|------|
| `orders/create`（日本語訳：__コード0__） | New order（日本語訳：新規注文） |
| `orders/paid`（日本語訳：__コード0__） | Order paid（日本語訳：注文が支払われた） |
| `orders/fulfilled`（日本語訳：__コード0__） | Order shipped（日本語訳：注文品が発送されました） |
| `customers/create`（日本語訳：__コード0__） | New customer（日本語訳：新規のお客様） |
| `products/update`（日本語訳：__コード0__） | Product changed（日本語訳：製品が変更されました） |
| `checkouts/create`（日本語訳：__コード0__） | Checkout started（日本語訳：チェックアウトが開始されました） |

## When to Use （日本語訳：いつ使用するか）

- E-commerce store management （日本語訳：ECストア運営）
- Product catalog operations （日本語訳：商品カタログ業務）
- Order processing （日本語訳：注文処理）
- Customer data management （日本語訳：顧客データ管理）
- Inventory tracking （日本語訳：在庫追跡）

## Rate Limits （日本語訳：レート制限）

- REST: 2 requests/second （日本語訳：REST: 2 リクエスト/秒）
- GraphQL: 50 points/second （日本語訳：GraphQL: 50 ポイント/秒）
- Bulk operations available （日本語訳：一括操作が可能）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- email-sequence （日本語訳：電子メールシーケンス）
- referral-program （日本語訳：紹介プログラム）
