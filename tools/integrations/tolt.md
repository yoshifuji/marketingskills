# Tolt （プッシュされました）

Affiliate program management for SaaS, with Stripe and Paddle integration. （Stripe と Paddle を統合した、SaaS のアフィリエイト プログラム管理。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for affiliates, referrals, payouts（アフィリエイト、紹介、支払い用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | JavaScript snippet for tracking（追跡用の JavaScript スニペット） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API in Tolt dashboard （**キーの取得**: Tolt ダッシュボードの [設定] > [API]）

## Common Agent Operations （エージェントの共通操作）

### List affiliates （アフィリエイトをリストする）

```bash
GET https://api.tolt.io/v1/affiliates
```

### Get affiliate （アフィリエイトを取得する）

```bash
GET https://api.tolt.io/v1/affiliates/{affiliate_id}
```

### Create affiliate （アフィリエイトを作成する）

```bash
POST https://api.tolt.io/v1/affiliates

{
  "email": "affiliate@example.com",
  "name": "John Doe"
}
```

### List referrals （紹介をリストする）

```bash
GET https://api.tolt.io/v1/referrals?affiliate_id={affiliate_id}
```

### Get referral by customer （顧客からの紹介を受ける）

```bash
GET https://api.tolt.io/v1/referrals?customer_id={stripe_customer_id}
```

### List commissions （コミッションの一覧表示）

```bash
GET https://api.tolt.io/v1/commissions?affiliate_id={affiliate_id}
```

### Get payout history （支払い履歴を取得する）

```bash
GET https://api.tolt.io/v1/payouts?affiliate_id={affiliate_id}
```

### Update affiliate （アフィリエイトを更新する）

```bash
PATCH https://api.tolt.io/v1/affiliates/{affiliate_id}

{
  "commission_rate": 30,
  "payout_method": "paypal",
  "paypal_email": "affiliate@paypal.com"
}
```

## JavaScript Tracking （JavaScriptの追跡）

### Install snippet （スニペットをインストールする）

```html
<script src="https://cdn.tolt.io/tolt.js" data-tolt="YOUR_PUBLIC_KEY"></script>
```

### Track signup （サインアップを追跡する）

```javascript
window.tolt.signup(stripeCustomerId);
```

### Identify existing customer （既存の顧客を特定する）

```javascript
window.tolt.identify(stripeCustomerId);
```

## Webhook Events （Webhook イベント）

| Event（イベント） | When（いつ） |
|-------|------|
| `affiliate.created`（__コード0__） | New affiliate registered（新規アフィリエイト登録しました） |
| `affiliate.approved`（__コード0__） | Affiliate approved（アフィリエイトが承認されました） |
| `referral.created`（__コード0__） | New referral tracked（新しい紹介を追跡しました） |
| `referral.converted`（__コード0__） | Referral converted to customer（紹介が顧客に変換されました） |
| `commission.created`（__コード0__） | Commission earned（獲得したコミッション） |
| `payout.completed`（__コード0__） | Payout sent（支払いが送信されました） |

## Key Features （主な特長）

- **Stripe native** - Automatic commission tracking （**ストライプネイティブ** - 自動コミッション追跡）
- **Paddle support** - Works with Paddle billing （**Paddle サポート** - Paddle の請求に対応します）
- **Affiliate dashboard** - White-labeled portal （**アフィリエイト ダッシュボード** - ホワイトラベルのポータル）
- **Payout automation** - PayPal and Wise payouts （**支払いの自動化** - PayPal と Wise の支払い）
- **Custom commission tiers** - Different rates per affiliate （**カスタム手数料階層** - アフィリエイトごとに異なるレート）

## Key Objects （主要なオブジェクト）

- **Affiliate** - Partner in your program （**アフィリエイト** - プログラムのパートナー）
- **Referral** - Tracked conversion （**紹介** - 追跡されたコンバージョン）
- **Commission** - Earned affiliate payment （**コミッション** - 獲得したアフィリエイト支払い）
- **Payout** - Processed payment to affiliate （**支払い** - アフィリエイトへの支払いが処理されました）
- **Program** - Campaign configuration （**プログラム** - キャンペーン構成）

## When to Use （いつ使用するか）

- Setting up SaaS affiliate programs （SaaS アフィリエイト プログラムのセットアップ）
- Managing affiliate relationships （アフィリエイト関係の管理）
- Tracking Stripe or Paddle-based referrals （Stripe または Paddle ベースの紹介の追跡）
- Processing affiliate payouts （アフィリエイト支払いの処理）
- Building affiliate dashboards （アフィリエイトダッシュボードの構築）

## Rate Limits （レート制限）

- 100 requests per minute （1 分あたり 100 リクエスト）
- Higher limits on enterprise plans （エンタープライズプランの制限の引き上げ）

## Relevant Skills （関連するスキル）

- referral-program （紹介プログラム）
- pricing-strategy （価格戦略）
