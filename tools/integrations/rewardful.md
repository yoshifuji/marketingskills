# Rewardful （日本語訳：やりがいのある）

Affiliate and referral tracking for Stripe-based SaaS businesses. （日本語訳：Stripe ベースの SaaS ビジネスのアフィリエイトと紹介の追跡。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for affiliates, referrals, commissions（日本語訳：アフィリエイト、紹介、コミッションのための REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | API-only, JavaScript snippet for tracking（日本語訳：API のみ、追跡用の JavaScript スニペット） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_secret}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_secret}`）
- **Get key**: Settings > API in Rewardful dashboard （日本語訳：**キーの取得**: Rewardful ダッシュボードの [設定] > [API]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List affiliates （日本語訳：アフィリエイトをリストする）

```bash
GET https://api.getrewardful.com/v1/affiliates
```

### Get affiliate by ID （日本語訳：IDでアフィリエイトを取得）

```bash
GET https://api.getrewardful.com/v1/affiliates/{affiliate_id}
```

### Search affiliate by email （日本語訳：メールでアフィリエイトを検索）

```bash
GET https://api.getrewardful.com/v1/affiliates?email=affiliate@example.com
```

### Get referral by Stripe customer （日本語訳：Stripe の顧客から紹介を受ける）

```bash
GET https://api.getrewardful.com/v1/referrals?stripe_customer_id={customer_id}
```

### List referrals for affiliate （日本語訳：アフィリエイトの紹介をリストする）

```bash
GET https://api.getrewardful.com/v1/referrals?affiliate_id={affiliate_id}
```

### Get commission details （日本語訳：コミッションの詳細を取得する）

```bash
GET https://api.getrewardful.com/v1/commissions/{commission_id}
```

### List commissions （日本語訳：コミッションの一覧表示）

```bash
GET https://api.getrewardful.com/v1/commissions?affiliate_id={affiliate_id}
```

### Create affiliate link （日本語訳：アフィリエイトリンクを作成する）

```bash
POST https://api.getrewardful.com/v1/affiliates/{affiliate_id}/links

{
  "token": "custom-link-token",
  "url": "https://example.com/pricing"
}
```

### Update affiliate （日本語訳：アフィリエイトを更新する）

```bash
PUT https://api.getrewardful.com/v1/affiliates/{affiliate_id}

{
  "first_name": "John",
  "last_name": "Doe",
  "paypal_email": "john@example.com"
}
```

## JavaScript Tracking （日本語訳：JavaScriptの追跡）

### Install snippet （日本語訳：スニペットをインストールする）

```html
<script>
(function(w,r){w._rwq=r;w[r]=w[r]||function(){(w[r].q=w[r].q||[]).push(arguments)}})(window,'rewardful');
</script>
<script async src='https://r.wdfl.co/rw.js' data-rewardful='YOUR_API_KEY'></script>
```

### Track conversion manually （日本語訳：コンバージョンを手動で追跡する）

```javascript
rewardful('convert', { email: 'customer@example.com' });
```

## Webhook Events （日本語訳：Webhook イベント）

| Event（日本語訳：イベント） | When（日本語訳：いつ） |
|-------|------|
| `affiliate.created`（日本語訳：__コード0__） | New affiliate signs up（日本語訳：新しいアフィリエイトの登録） |
| `affiliate.approved`（日本語訳：__コード0__） | Affiliate approved（日本語訳：アフィリエイトが承認されました） |
| `referral.created`（日本語訳：__コード0__） | New referral tracked（日本語訳：新しい紹介を追跡しました） |
| `referral.converted`（日本語訳：__コード0__） | Referral becomes customer（日本語訳：紹介者が顧客になる） |
| `commission.created`（日本語訳：__コード0__） | Commission generated（日本語訳：手数料発生） |
| `commission.paid`（日本語訳：__コード0__） | Commission paid out（日本語訳：支払われたコミッション） |

## Key Objects （日本語訳：主要なオブジェクト）

- **Affiliate** - Partner promoting your product （日本語訳：**アフィリエイト** - 製品を宣伝するパートナー）
- **Referral** - Tracked visit/lead from affiliate （日本語訳：**紹介** - アフィリエイトからの訪問/見込み客の追跡）
- **Commission** - Earned payment for affiliate （日本語訳：**コミッション** - アフィリエイトに対して獲得した支払い）
- **Campaign** - Program with specific terms （日本語訳：**キャンペーン** - 特定の条件を伴うプログラム）
- **Link** - Tracking URL for affiliate （日本語訳：**リンク** - アフィリエイトのトラッキング URL）

## Integration with Stripe （日本語訳：Stripe との統合）

Rewardful automatically: （日本語訳：自動的に特典が付与されます:）
1. Tracks referral cookie when user visits via affiliate link （日本語訳：ユーザーがアフィリエイトリンク経由でアクセスしたときに紹介クッキーを追跡します）
2. Associates Stripe customer with referral on checkout （日本語訳：Stripe 顧客をチェックアウト時の紹介に関連付けます）
3. Creates commissions when subscriptions are paid （日本語訳：サブスクリプションの支払い時に手数料が発生します）
4. Handles recurring commissions for subscriptions （日本語訳：サブスクリプションの定期的な手数料を処理します）

## When to Use （日本語訳：いつ使用するか）

- Setting up affiliate/referral programs for SaaS （日本語訳：SaaS のアフィリエイト/紹介プログラムのセットアップ）
- Tracking referral attribution from Stripe payments （日本語訳：Stripe 支払いからの紹介帰属の追跡）
- Managing affiliate relationships （日本語訳：アフィリエイト関係の管理）
- Processing affiliate payouts （日本語訳：アフィリエイト支払いの処理）
- Analyzing referral program performance （日本語訳：紹介プログラムのパフォーマンスの分析）

## Rate Limits （日本語訳：レート制限）

- 120 requests per minute （日本語訳：1 分あたり 120 リクエスト）
- Contact support for higher limits （日本語訳：より高い制限についてはサポートにお問い合わせください）

## Relevant Skills （日本語訳：関連するスキル）

- referral-program （日本語訳：紹介プログラム）
- pricing-strategy （日本語訳：価格戦略）
