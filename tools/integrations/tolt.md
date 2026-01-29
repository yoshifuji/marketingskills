# Tolt （日本語訳：プッシュされました）

Affiliate program management for SaaS, with Stripe and Paddle integration. （日本語訳：Stripe と Paddle を統合した、SaaS のアフィリエイト プログラム管理。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for affiliates, referrals, payouts（日本語訳：アフィリエイト、紹介、支払い用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | JavaScript snippet for tracking（日本語訳：追跡用の JavaScript スニペット） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Get key**: Settings > API in Tolt dashboard （日本語訳：**キーの取得**: Tolt ダッシュボードの [設定] > [API]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List affiliates （日本語訳：アフィリエイトをリストする）

```bash
GET https://api.tolt.io/v1/affiliates
```

### Get affiliate （日本語訳：アフィリエイトを取得する）

```bash
GET https://api.tolt.io/v1/affiliates/{affiliate_id}
```

### Create affiliate （日本語訳：アフィリエイトを作成する）

```bash
POST https://api.tolt.io/v1/affiliates

{
  "email": "affiliate@example.com",
  "name": "John Doe"
}
```

### List referrals （日本語訳：紹介をリストする）

```bash
GET https://api.tolt.io/v1/referrals?affiliate_id={affiliate_id}
```

### Get referral by customer （日本語訳：顧客からの紹介を受ける）

```bash
GET https://api.tolt.io/v1/referrals?customer_id={stripe_customer_id}
```

### List commissions （日本語訳：コミッションの一覧表示）

```bash
GET https://api.tolt.io/v1/commissions?affiliate_id={affiliate_id}
```

### Get payout history （日本語訳：支払い履歴を取得する）

```bash
GET https://api.tolt.io/v1/payouts?affiliate_id={affiliate_id}
```

### Update affiliate （日本語訳：アフィリエイトを更新する）

```bash
PATCH https://api.tolt.io/v1/affiliates/{affiliate_id}

{
  "commission_rate": 30,
  "payout_method": "paypal",
  "paypal_email": "affiliate@paypal.com"
}
```

## JavaScript Tracking （日本語訳：JavaScriptの追跡）

### Install snippet （日本語訳：スニペットをインストールする）

```html
<script src="https://cdn.tolt.io/tolt.js" data-tolt="YOUR_PUBLIC_KEY"></script>
```

### Track signup （日本語訳：サインアップを追跡する）

```javascript
window.tolt.signup(stripeCustomerId);
```

### Identify existing customer （日本語訳：既存の顧客を特定する）

```javascript
window.tolt.identify(stripeCustomerId);
```

## Webhook Events （日本語訳：Webhook イベント）

| Event（日本語訳：イベント） | When（日本語訳：いつ） |
|-------|------|
| `affiliate.created`（日本語訳：__コード0__） | New affiliate registered（日本語訳：新規アフィリエイト登録しました） |
| `affiliate.approved`（日本語訳：__コード0__） | Affiliate approved（日本語訳：アフィリエイトが承認されました） |
| `referral.created`（日本語訳：__コード0__） | New referral tracked（日本語訳：新しい紹介を追跡しました） |
| `referral.converted`（日本語訳：__コード0__） | Referral converted to customer（日本語訳：紹介が顧客に変換されました） |
| `commission.created`（日本語訳：__コード0__） | Commission earned（日本語訳：獲得したコミッション） |
| `payout.completed`（日本語訳：__コード0__） | Payout sent（日本語訳：支払いが送信されました） |

## Key Features （日本語訳：主な特長）

- **Stripe native** - Automatic commission tracking （日本語訳：**ストライプネイティブ** - 自動コミッション追跡）
- **Paddle support** - Works with Paddle billing （日本語訳：**Paddle サポート** - Paddle の請求に対応します）
- **Affiliate dashboard** - White-labeled portal （日本語訳：**アフィリエイト ダッシュボード** - ホワイトラベルのポータル）
- **Payout automation** - PayPal and Wise payouts （日本語訳：**支払いの自動化** - PayPal と Wise の支払い）
- **Custom commission tiers** - Different rates per affiliate （日本語訳：**カスタム手数料階層** - アフィリエイトごとに異なるレート）

## Key Objects （日本語訳：主要なオブジェクト）

- **Affiliate** - Partner in your program （日本語訳：**アフィリエイト** - プログラムのパートナー）
- **Referral** - Tracked conversion （日本語訳：**紹介** - 追跡されたコンバージョン）
- **Commission** - Earned affiliate payment （日本語訳：**コミッション** - 獲得したアフィリエイト支払い）
- **Payout** - Processed payment to affiliate （日本語訳：**支払い** - アフィリエイトへの支払いが処理されました）
- **Program** - Campaign configuration （日本語訳：**プログラム** - キャンペーン構成）

## When to Use （日本語訳：いつ使用するか）

- Setting up SaaS affiliate programs （日本語訳：SaaS アフィリエイト プログラムのセットアップ）
- Managing affiliate relationships （日本語訳：アフィリエイト関係の管理）
- Tracking Stripe or Paddle-based referrals （日本語訳：Stripe または Paddle ベースの紹介の追跡）
- Processing affiliate payouts （日本語訳：アフィリエイト支払いの処理）
- Building affiliate dashboards （日本語訳：アフィリエイトダッシュボードの構築）

## Rate Limits （日本語訳：レート制限）

- 100 requests per minute （日本語訳：1 分あたり 100 リクエスト）
- Higher limits on enterprise plans （日本語訳：エンタープライズプランの制限の引き上げ）

## Relevant Skills （日本語訳：関連するスキル）

- referral-program （日本語訳：紹介プログラム）
- pricing-strategy （日本語訳：価格戦略）
