# Stripe （ストライプ）

Payment processing, subscriptions, and billing for internet businesses. （インターネット ビジネスの支払い処理、サブスクリプション、請求。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Comprehensive REST API（包括的なREST API） |
| MCP（MCP） | ✓ | Available via Stripe MCP server（Stripe MCP サーバー経由で利用可能） |
| CLI（CLI） | ✓ | `stripe` CLI for testing and webhooks（`stripe` テストと Webhook 用の CLI） |
| SDK（SDK） | ✓ | Official SDKs for most languages（ほとんどの言語に対応した公式 SDK） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer sk_live_xxx` or `sk_test_xxx` （**ヘッダー**: `Authorization: Bearer sk_live_xxx` または `sk_test_xxx`）
- **Keys**: Secret key (server), Publishable key (client) （**キー**: 秘密キー (サーバー)、公開可能キー (クライアント)）

## Common Agent Operations （エージェントの共通操作）

### List customers （顧客をリストアップする）

```bash
GET https://api.stripe.com/v1/customers?limit=10
```

### Get customer by email （メールで顧客を獲得する）

```bash
GET https://api.stripe.com/v1/customers?email=user@example.com
```

### Get subscription （サブスクリプションを取得する）

```bash
GET https://api.stripe.com/v1/subscriptions/{subscription_id}
```

### List subscriptions for customer （顧客のサブスクリプションをリストする）

```bash
GET https://api.stripe.com/v1/subscriptions?customer={customer_id}
```

### Create checkout session （チェックアウトセッションを作成する）

```bash
POST https://api.stripe.com/v1/checkout/sessions

customer={customer_id}
&line_items[0][price]={price_id}
&line_items[0][quantity]=1
&mode=subscription
&success_url=https://example.com/success
&cancel_url=https://example.com/cancel
```

### Create customer portal session （カスタマーポータルセッションの作成）

```bash
POST https://api.stripe.com/v1/billing_portal/sessions

customer={customer_id}
&return_url=https://example.com/account
```

### List recent invoices （最近の請求書をリストする）

```bash
GET https://api.stripe.com/v1/invoices?customer={customer_id}&limit=10
```

### Get payment intent （支払い意図を取得する）

```bash
GET https://api.stripe.com/v1/payment_intents/{payment_intent_id}
```

## Webhook Events （Webhook イベント）

Key events to handle: （処理すべき主なイベント:）

| Event（イベント） | When（いつ） | Action（アクション） |
|-------|------|--------|
| `checkout.session.completed`（__コード0__） | Successful checkout（チェックアウトが成功しました） | Provision access（プロビジョニングアクセス） |
| `customer.subscription.created`（__コード0__） | New subscription（新規購読） | Update user record（ユーザーレコードを更新する） |
| `customer.subscription.updated`（__コード0__） | Plan change（計画変更） | Update entitlements（権利を更新する） |
| `customer.subscription.deleted`（__コード0__） | Cancellation（キャンセル） | Revoke access（アクセスを取り消す） |
| `invoice.payment_failed`（__コード0__） | Payment failed（支払いに失敗しました） | Notify user, retry（ユーザーに通知し、再試行してください） |
| `invoice.paid`（__コード0__） | Invoice paid（支払われた請求書） | Confirm payment（支払いを確認する） |

### Verify webhook signature （Webhook 署名を検証する）

```javascript
const event = stripe.webhooks.constructEvent(
  payload,
  sig,
  webhookSecret
);
```

## CLI Commands （CLIコマンド）

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

## Key Objects （主要なオブジェクト）

- **Customer** - User billing profile （**顧客** - ユーザーの請求プロファイル）
- **Subscription** - Recurring billing （**サブスクリプション** - 定期的な請求）
- **Price** - Pricing configuration （**価格** - 価格設定）
- **Product** - What you sell （**製品** - 販売するもの）
- **Invoice** - Billing document （**請求書** - 請求書）
- **PaymentIntent** - One-time payment （**PaymentIntent** - 1 回限りの支払い）
- **Checkout Session** - Hosted payment page （**チェックアウト セッション** - ホストされた支払いページ）

## When to Use （いつ使用するか）

- Processing payments （支払いの処理）
- Managing subscriptions （サブスクリプションの管理）
- Creating checkout flows （チェックアウトフローの作成）
- Handling billing portal （請求ポータルの処理）
- Querying customer data （顧客データのクエリ）
- Revenue analytics （収益分析）

## Rate Limits （レート制限）

- 100 read requests per second （1 秒あたり 100 件の読み取りリクエスト）
- 100 write requests per second （1 秒あたり 100 件の書き込みリクエスト）
- Higher limits available on request （リクエストに応じてより高い制限も利用可能）

## Relevant Skills （関連するスキル）

- pricing-strategy （価格戦略）
- referral-program (Stripe-integrated affiliate tools) （紹介プログラム (Stripe 統合アフィリエイト ツール)）
- analytics-tracking (revenue tracking) （分析追跡 (収益追跡)）
