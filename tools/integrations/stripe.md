# Stripe （日本語訳：ストライプ）

Payment processing, subscriptions, and billing for internet businesses. （日本語訳：インターネット ビジネスの支払い処理、サブスクリプション、請求。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Comprehensive REST API（日本語訳：包括的なREST API） |
| MCP（日本語訳：MCP） | ✓ | Available via Stripe MCP server（日本語訳：Stripe MCP サーバー経由で利用可能） |
| CLI（日本語訳：CLI） | ✓ | `stripe` CLI for testing and webhooks（日本語訳：`stripe` テストと Webhook 用の CLI） |
| SDK（日本語訳：SDK） | ✓ | Official SDKs for most languages（日本語訳：ほとんどの言語に対応した公式 SDK） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer sk_live_xxx` or `sk_test_xxx` （日本語訳：**ヘッダー**: `Authorization: Bearer sk_live_xxx` または `sk_test_xxx`）
- **Keys**: Secret key (server), Publishable key (client) （日本語訳：**キー**: 秘密キー (サーバー)、公開可能キー (クライアント)）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List customers （日本語訳：顧客をリストアップする）

```bash
GET https://api.stripe.com/v1/customers?limit=10
```

### Get customer by email （日本語訳：メールで顧客を獲得する）

```bash
GET https://api.stripe.com/v1/customers?email=user@example.com
```

### Get subscription （日本語訳：サブスクリプションを取得する）

```bash
GET https://api.stripe.com/v1/subscriptions/{subscription_id}
```

### List subscriptions for customer （日本語訳：顧客のサブスクリプションをリストする）

```bash
GET https://api.stripe.com/v1/subscriptions?customer={customer_id}
```

### Create checkout session （日本語訳：チェックアウトセッションを作成する）

```bash
POST https://api.stripe.com/v1/checkout/sessions

customer={customer_id}
&line_items[0][price]={price_id}
&line_items[0][quantity]=1
&mode=subscription
&success_url=https://example.com/success
&cancel_url=https://example.com/cancel
```

### Create customer portal session （日本語訳：カスタマーポータルセッションの作成）

```bash
POST https://api.stripe.com/v1/billing_portal/sessions

customer={customer_id}
&return_url=https://example.com/account
```

### List recent invoices （日本語訳：最近の請求書をリストする）

```bash
GET https://api.stripe.com/v1/invoices?customer={customer_id}&limit=10
```

### Get payment intent （日本語訳：支払い意図を取得する）

```bash
GET https://api.stripe.com/v1/payment_intents/{payment_intent_id}
```

## Webhook Events （日本語訳：Webhook イベント）

Key events to handle: （日本語訳：処理すべき主なイベント:）

| Event（日本語訳：イベント） | When（日本語訳：いつ） | Action（日本語訳：アクション） |
|-------|------|--------|
| `checkout.session.completed`（日本語訳：__コード0__） | Successful checkout（日本語訳：チェックアウトが成功しました） | Provision access（日本語訳：プロビジョニングアクセス） |
| `customer.subscription.created`（日本語訳：__コード0__） | New subscription（日本語訳：新規購読） | Update user record（日本語訳：ユーザーレコードを更新する） |
| `customer.subscription.updated`（日本語訳：__コード0__） | Plan change（日本語訳：計画変更） | Update entitlements（日本語訳：権利を更新する） |
| `customer.subscription.deleted`（日本語訳：__コード0__） | Cancellation（日本語訳：キャンセル） | Revoke access（日本語訳：アクセスを取り消す） |
| `invoice.payment_failed`（日本語訳：__コード0__） | Payment failed（日本語訳：支払いに失敗しました） | Notify user, retry（日本語訳：ユーザーに通知し、再試行してください） |
| `invoice.paid`（日本語訳：__コード0__） | Invoice paid（日本語訳：支払われた請求書） | Confirm payment（日本語訳：支払いを確認する） |

### Verify webhook signature （日本語訳：Webhook 署名を検証する）

```javascript
const event = stripe.webhooks.constructEvent(
  payload,
  sig,
  webhookSecret
);
```

## CLI Commands （日本語訳：CLIコマンド）

```bash
# Listen to webhooks locally
stripe listen --forward-to localhost:3000/webhooks

# Trigger test events
stripe trigger checkout.session.completed

# List recent events
stripe events list --limit 10

# Get resource
stripe customers retrieve cus_xxx
```

## Key Objects （日本語訳：主要なオブジェクト）

- **Customer** - User billing profile （日本語訳：**顧客** - ユーザーの請求プロファイル）
- **Subscription** - Recurring billing （日本語訳：**サブスクリプション** - 定期的な請求）
- **Price** - Pricing configuration （日本語訳：**価格** - 価格設定）
- **Product** - What you sell （日本語訳：**製品** - 販売するもの）
- **Invoice** - Billing document （日本語訳：**請求書** - 請求書）
- **PaymentIntent** - One-time payment （日本語訳：**PaymentIntent** - 1 回限りの支払い）
- **Checkout Session** - Hosted payment page （日本語訳：**チェックアウト セッション** - ホストされた支払いページ）

## When to Use （日本語訳：いつ使用するか）

- Processing payments （日本語訳：支払いの処理）
- Managing subscriptions （日本語訳：サブスクリプションの管理）
- Creating checkout flows （日本語訳：チェックアウトフローの作成）
- Handling billing portal （日本語訳：請求ポータルの処理）
- Querying customer data （日本語訳：顧客データのクエリ）
- Revenue analytics （日本語訳：収益分析）

## Rate Limits （日本語訳：レート制限）

- 100 read requests per second （日本語訳：1 秒あたり 100 件の読み取りリクエスト）
- 100 write requests per second （日本語訳：1 秒あたり 100 件の書き込みリクエスト）
- Higher limits available on request （日本語訳：リクエストに応じてより高い制限も利用可能）

## Relevant Skills （日本語訳：関連するスキル）

- pricing-strategy （日本語訳：価格戦略）
- referral-program (Stripe-integrated affiliate tools) （日本語訳：紹介プログラム (Stripe 統合アフィリエイト ツール)）
- analytics-tracking (revenue tracking) （日本語訳：分析追跡 (収益追跡)）
