# Mention Me （日本語訳：私に言及してください）

Enterprise referral marketing platform for customer advocacy. （日本語訳：顧客擁護のためのエンタープライズ紹介マーケティング プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for referrals, customers, rewards（日本語訳：紹介、顧客、特典用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | JavaScript widget for embedding（日本語訳：埋め込み用のJavaScriptウィジェット） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Environment**: Separate keys for sandbox and production （日本語訳：**環境**: サンドボックスと実稼働用に別のキー）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Create referral offer （日本語訳：紹介オファーを作成する）

```bash
POST https://api.mention-me.com/api/v2/referrer-offer

{
  "email": "customer@example.com",
  "firstname": "John",
  "lastname": "Doe",
  "order_number": "ORD-123",
  "order_total": 99.99,
  "order_currency": "USD"
}
```

### Get referral link for customer （日本語訳：顧客の紹介リンクを取得する）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/share-links
```

### Record referee (referred customer) （日本語訳：レコードレフェリー（紹介された顧客））

```bash
POST https://api.mention-me.com/api/v2/referee

{
  "email": "referred@example.com",
  "firstname": "Jane",
  "referrer_code": "JOHN123",
  "order_number": "ORD-456",
  "order_total": 149.99
}
```

### Get referral status （日本語訳：紹介ステータスを取得する）

```bash
GET https://api.mention-me.com/api/v2/referral/{referral_id}
```

### List referrals for customer （日本語訳：顧客の紹介をリストアップする）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/referrals
```

### Get reward balance （日本語訳：報酬残高を取得する）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/rewards
```

### Redeem reward （日本語訳：報酬を引き換える）

```bash
POST https://api.mention-me.com/api/v2/referrer/{customer_id}/rewards/redeem

{
  "reward_id": "RWD-123",
  "order_number": "ORD-789"
}
```

## JavaScript Widget （日本語訳：JavaScript ウィジェット）

### Embed referral widget （日本語訳：紹介ウィジェットを埋め込む）

```html
<div id="mmWrapper"></div>
<script>
  window.MentionMe = window.MentionMe || [];
  MentionMe.push({
    type: 'offer',
    customer: {
      email: 'customer@example.com',
      firstname: 'John',
      order_number: 'ORD-123'
    }
  });
</script>
<script src="https://tag.mention-me.com/client/{partner_code}.js" async></script>
```

### Name share widget （日本語訳：名前共有ウィジェット）

```javascript
MentionMe.push({
  type: 'nameShare',
  customer: {
    email: 'customer@example.com'
  }
});
```

## Webhook Events （日本語訳：Webhook イベント）

| Event（日本語訳：イベント） | When（日本語訳：いつ） |
|-------|------|
| `referral.created`（日本語訳：__コード0__） | New referral tracked（日本語訳：新しい紹介を追跡しました） |
| `referral.converted`（日本語訳：__コード0__） | Referral completed purchase（日本語訳：紹介による購入完了） |
| `reward.earned`（日本語訳：__コード0__） | Reward unlocked（日本語訳：報酬のロックが解除されました） |
| `reward.redeemed`（日本語訳：__コード0__） | Reward used（日本語訳：使用した報酬） |

## Key Features （日本語訳：主な特長）

- **A/B testing** - Built-in experiment framework （日本語訳：**A/B テスト** - 組み込みの実験フレームワーク）
- **Fraud prevention** - Automatic fraud detection （日本語訳：**不正行為の防止** - 不正行為の自動検出）
- **Multi-channel** - Share via link, email, social （日本語訳：**マルチチャネル** - リンク、電子メール、ソーシャル経由で共有）
- **Name sharing** - Refer by name, not code （日本語訳：**名前の共有** - コードではなく名前で参照します）
- **Segmentation** - Different offers by segment （日本語訳：**セグメンテーション** - セグメントごとに異なるオファー）
- **Analytics** - Referral program reporting （日本語訳：**分析** - 紹介プログラムのレポート）

## Key Objects （日本語訳：主要なオブジェクト）

- **Referrer** - Customer who refers （日本語訳：**紹介者** - 紹介する顧客）
- **Referee** - Customer who is referred （日本語訳：**紹介者** - 紹介された顧客）
- **Referral** - Connection between referrer and referee （日本語訳：**紹介** - 紹介者と被紹介者のつながり）
- **Offer** - Referral program configuration （日本語訳：**オファー** - 紹介プログラムの構成）
- **Reward** - Incentive earned （日本語訳：**報酬** - 獲得したインセンティブ）

## When to Use （日本語訳：いつ使用するか）

- Enterprise referral programs （日本語訳：企業紹介プログラム）
- Multi-market referral campaigns （日本語訳：マルチマーケット紹介キャンペーン）
- A/B testing referral offers （日本語訳：A/B テストの紹介オファー）
- Fraud-resistant referral tracking （日本語訳：不正行為に強い紹介追跡）
- Name-based sharing programs （日本語訳：名前ベースの共有プログラム）

## Rate Limits （日本語訳：レート制限）

- 1000 requests per minute （日本語訳：1 分あたり 1000 リクエスト）
- Contact for higher limits （日本語訳：より高い制限についてはお問い合わせください）

## Relevant Skills （日本語訳：関連するスキル）

- referral-program （日本語訳：紹介プログラム）
- pricing-strategy （日本語訳：価格戦略）
- analytics-tracking （日本語訳：分析追跡）
