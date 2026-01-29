# Mention Me （私に言及してください）

Enterprise referral marketing platform for customer advocacy. （顧客擁護のためのエンタープライズ紹介マーケティング プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for referrals, customers, rewards（紹介、顧客、特典用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | JavaScript widget for embedding（埋め込み用のJavaScriptウィジェット） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **Environment**: Separate keys for sandbox and production （**環境**: サンドボックスと実稼働用に別のキー）

## Common Agent Operations （エージェントの共通操作）

### Create referral offer （紹介オファーを作成する）

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

### Get referral link for customer （顧客の紹介リンクを取得する）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/share-links
```

### Record referee (referred customer) （レコードレフェリー（紹介された顧客））

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

### Get referral status （紹介ステータスを取得する）

```bash
GET https://api.mention-me.com/api/v2/referral/{referral_id}
```

### List referrals for customer （顧客の紹介をリストアップする）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/referrals
```

### Get reward balance （報酬残高を取得する）

```bash
GET https://api.mention-me.com/api/v2/referrer/{customer_id}/rewards
```

### Redeem reward （報酬を引き換える）

```bash
POST https://api.mention-me.com/api/v2/referrer/{customer_id}/rewards/redeem

{
  "reward_id": "RWD-123",
  "order_number": "ORD-789"
}
```

## JavaScript Widget （JavaScript ウィジェット）

### Embed referral widget （紹介ウィジェットを埋め込む）

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

### Name share widget （名前共有ウィジェット）

```javascript
MentionMe.push({
  type: 'nameShare',
  customer: {
    email: 'customer@example.com'
  }
});
```

## Webhook Events （Webhook イベント）

| Event（イベント） | When（いつ） |
|-------|------|
| `referral.created`（__コード0__） | New referral tracked（新しい紹介を追跡しました） |
| `referral.converted`（__コード0__） | Referral completed purchase（紹介による購入完了） |
| `reward.earned`（__コード0__） | Reward unlocked（報酬のロックが解除されました） |
| `reward.redeemed`（__コード0__） | Reward used（使用した報酬） |

## Key Features （主な特長）

- **A/B testing** - Built-in experiment framework （**A/B テスト** - 組み込みの実験フレームワーク）
- **Fraud prevention** - Automatic fraud detection （**不正行為の防止** - 不正行為の自動検出）
- **Multi-channel** - Share via link, email, social （**マルチチャネル** - リンク、電子メール、ソーシャル経由で共有）
- **Name sharing** - Refer by name, not code （**名前の共有** - コードではなく名前で参照します）
- **Segmentation** - Different offers by segment （**セグメンテーション** - セグメントごとに異なるオファー）
- **Analytics** - Referral program reporting （**分析** - 紹介プログラムのレポート）

## Key Objects （主要なオブジェクト）

- **Referrer** - Customer who refers （**紹介者** - 紹介する顧客）
- **Referee** - Customer who is referred （**紹介者** - 紹介された顧客）
- **Referral** - Connection between referrer and referee （**紹介** - 紹介者と被紹介者のつながり）
- **Offer** - Referral program configuration （**オファー** - 紹介プログラムの構成）
- **Reward** - Incentive earned （**報酬** - 獲得したインセンティブ）

## When to Use （いつ使用するか）

- Enterprise referral programs （企業紹介プログラム）
- Multi-market referral campaigns （マルチマーケット紹介キャンペーン）
- A/B testing referral offers （A/B テストの紹介オファー）
- Fraud-resistant referral tracking （不正行為に強い紹介追跡）
- Name-based sharing programs （名前ベースの共有プログラム）

## Rate Limits （レート制限）

- 1000 requests per minute （1 分あたり 1000 リクエスト）
- Contact for higher limits （より高い制限についてはお問い合わせください）

## Relevant Skills （関連するスキル）

- referral-program （紹介プログラム）
- pricing-strategy （価格戦略）
- analytics-tracking （分析追跡）
