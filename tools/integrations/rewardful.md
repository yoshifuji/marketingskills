# Rewardful （やりがいのある）

Affiliate and referral tracking for Stripe-based SaaS businesses. （Stripe ベースの SaaS ビジネスのアフィリエイトと紹介の追跡。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for affiliates, referrals, commissions（アフィリエイト、紹介、コミッションのための REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | API-only, JavaScript snippet for tracking（API のみ、追跡用の JavaScript スニペット） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_secret}` （**ヘッダー**: `Authorization: Bearer {api_secret}`）
- **Get key**: Settings > API in Rewardful dashboard （**キーの取得**: Rewardful ダッシュボードの [設定] > [API]）

## Common Agent Operations （エージェントの共通操作）

### List affiliates （アフィリエイトをリストする）

```bash
GET https://api.getrewardful.com/v1/affiliates
```

### Get affiliate by ID （IDでアフィリエイトを取得）

```bash
GET https://api.getrewardful.com/v1/affiliates/{affiliate_id}
```

### Search affiliate by email （メールでアフィリエイトを検索）

```bash
GET https://api.getrewardful.com/v1/affiliates?email=affiliate@example.com
```

### Get referral by Stripe customer （Stripe の顧客から紹介を受ける）

```bash
GET https://api.getrewardful.com/v1/referrals?stripe_customer_id={customer_id}
```

### List referrals for affiliate （アフィリエイトの紹介をリストする）

```bash
GET https://api.getrewardful.com/v1/referrals?affiliate_id={affiliate_id}
```

### Get commission details （コミッションの詳細を取得する）

```bash
GET https://api.getrewardful.com/v1/commissions/{commission_id}
```

### List commissions （コミッションの一覧表示）

```bash
GET https://api.getrewardful.com/v1/commissions?affiliate_id={affiliate_id}
```

### Create affiliate link （アフィリエイトリンクを作成する）

```bash
POST https://api.getrewardful.com/v1/affiliates/{affiliate_id}/links

{
  "token": "custom-link-token",
  "url": "https://example.com/pricing"
}
```

### Update affiliate （アフィリエイトを更新する）

```bash
PUT https://api.getrewardful.com/v1/affiliates/{affiliate_id}

{
  "first_name": "John",
  "last_name": "Doe",
  "paypal_email": "john@example.com"
}
```

## JavaScript Tracking （JavaScriptの追跡）

### Install snippet （スニペットをインストールする）

```html
<script>
(function(w,r){w._rwq=r;w[r]=w[r]||function(){(w[r].q=w[r].q||[]).push(arguments)}})(window,'rewardful');
</script>
<script async src='https://r.wdfl.co/rw.js' data-rewardful='YOUR_API_KEY'></script>
```

### Track conversion manually （コンバージョンを手動で追跡する）

```javascript
rewardful('convert', { email: 'customer@example.com' });
```

## Webhook Events （Webhook イベント）

| Event（イベント） | When（いつ） |
|-------|------|
| `affiliate.created`（__コード0__） | New affiliate signs up（新しいアフィリエイトの登録） |
| `affiliate.approved`（__コード0__） | Affiliate approved（アフィリエイトが承認されました） |
| `referral.created`（__コード0__） | New referral tracked（新しい紹介を追跡しました） |
| `referral.converted`（__コード0__） | Referral becomes customer（紹介者が顧客になる） |
| `commission.created`（__コード0__） | Commission generated（手数料発生） |
| `commission.paid`（__コード0__） | Commission paid out（支払われたコミッション） |

## Key Objects （主要なオブジェクト）

- **Affiliate** - Partner promoting your product （**アフィリエイト** - 製品を宣伝するパートナー）
- **Referral** - Tracked visit/lead from affiliate （**紹介** - アフィリエイトからの訪問/見込み客の追跡）
- **Commission** - Earned payment for affiliate （**コミッション** - アフィリエイトに対して獲得した支払い）
- **Campaign** - Program with specific terms （**キャンペーン** - 特定の条件を伴うプログラム）
- **Link** - Tracking URL for affiliate （**リンク** - アフィリエイトのトラッキング URL）

## Integration with Stripe （Stripe との統合）

Rewardful automatically: （自動的に特典が付与されます:）
1. Tracks referral cookie when user visits via affiliate link （ユーザーがアフィリエイトリンク経由でアクセスしたときに紹介クッキーを追跡します）
2. Associates Stripe customer with referral on checkout （Stripe 顧客をチェックアウト時の紹介に関連付けます）
3. Creates commissions when subscriptions are paid （サブスクリプションの支払い時に手数料が発生します）
4. Handles recurring commissions for subscriptions （サブスクリプションの定期的な手数料を処理します）

## When to Use （いつ使用するか）

- Setting up affiliate/referral programs for SaaS （SaaS のアフィリエイト/紹介プログラムのセットアップ）
- Tracking referral attribution from Stripe payments （Stripe 支払いからの紹介帰属の追跡）
- Managing affiliate relationships （アフィリエイト関係の管理）
- Processing affiliate payouts （アフィリエイト支払いの処理）
- Analyzing referral program performance （紹介プログラムのパフォーマンスの分析）

## Rate Limits （レート制限）

- 120 requests per minute （1 分あたり 120 リクエスト）
- Contact support for higher limits （より高い制限についてはサポートにお問い合わせください）

## Relevant Skills （関連するスキル）

- referral-program （紹介プログラム）
- pricing-strategy （価格戦略）
