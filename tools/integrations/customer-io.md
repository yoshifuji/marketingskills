# Customer.io （Customer.io）

Behavior-based messaging platform for email, push, SMS, and in-app. （電子メール、プッシュ、SMS、アプリ内向けの行動ベースのメッセージング プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Track API, App API, Journeys API（Track API、App API、Journeys API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | JavaScript, iOS, Android, Ruby, Python（JavaScript、iOS、Android、Ruby、Python） |

## Authentication （認証）

- **Track API**: Site ID + API Key (Basic auth) （**Track API**: サイト ID + API キー (基本認証)）
- **App API**: Bearer token （**アプリ API**: ベアラー トークン）
- **Header**: `Authorization: Basic {base64(site_id:api_key)}` （**ヘッダー**: `Authorization: Basic {base64(site_id:api_key)}`）

## Common Agent Operations （エージェントの共通操作）

### Identify customer （顧客を特定する）

```bash
PUT https://track.customer.io/api/v1/customers/{customer_id}

Authorization: Basic {base64(site_id:api_key)}

{
  "email": "user@example.com",
  "created_at": 1705312800,
  "first_name": "John",
  "plan": "pro"
}
```

### Track event （イベントを追跡する）

```bash
POST https://track.customer.io/api/v1/customers/{customer_id}/events

Authorization: Basic {base64(site_id:api_key)}

{
  "name": "purchase",
  "data": {
    "product": "Pro Plan",
    "amount": 99
  }
}
```

### Track anonymous event （匿名イベントを追跡する）

```bash
POST https://track.customer.io/api/v1/events

Authorization: Basic {base64(site_id:api_key)}

{
  "name": "page_viewed",
  "data": {
    "page": "/pricing"
  },
  "anonymous_id": "anon_123"
}
```

### Delete customer （顧客の削除）

```bash
DELETE https://track.customer.io/api/v1/customers/{customer_id}

Authorization: Basic {base64(site_id:api_key)}
```

### Get customer (App API) （顧客の獲得（アプリAPI））

```bash
GET https://api.customer.io/v1/customers/{customer_id}/attributes

Authorization: Bearer {app_api_key}
```

### List campaigns （リストキャンペーン）

```bash
GET https://api.customer.io/v1/campaigns

Authorization: Bearer {app_api_key}
```

### Get campaign metrics （キャンペーン指標を取得する）

```bash
GET https://api.customer.io/v1/campaigns/{campaign_id}/metrics

Authorization: Bearer {app_api_key}
```

### Trigger broadcast （トリガーブロードキャスト）

```bash
POST https://api.customer.io/v1/campaigns/{campaign_id}/triggers

Authorization: Bearer {app_api_key}

{
  "emails": ["user@example.com"],
  "data": {
    "coupon_code": "SAVE20"
  }
}
```

### Send transactional email （取引メールを送信する）

```bash
POST https://api.customer.io/v1/send/email

Authorization: Bearer {app_api_key}

{
  "transactional_message_id": "1",
  "to": "user@example.com",
  "identifiers": {
    "id": "user_123"
  },
  "message_data": {
    "order_id": "ORD-456"
  }
}
```

## JavaScript SDK （JavaScript SDK）

```javascript
// Initialize
_cio.identify({
  id: 'user_123',
  email: 'user@example.com',
  created_at: 1705312800,
  plan: 'pro'
});

// Track event
_cio.track('purchase', {
  product: 'Pro Plan',
  amount: 99
});

// Track page view
_cio.page();
```

## Key Concepts （主要な概念）

- **People** - Customers and leads （**人** - 顧客とリード）
- **Segments** - Dynamic groups based on attributes/behavior （**セグメント** - 属性/動作に基づく動的グループ）
- **Campaigns** - Automated message sequences （**キャンペーン** - 自動化されたメッセージ シーケンス）
- **Broadcasts** - One-time sends （**ブロードキャスト** - 1 回限りの送信）
- **Transactional** - Triggered messages （**トランザクション** - トリガーされたメッセージ）

## Attribute Types （属性の種類）

- Standard: `email`, `created_at`, `unsubscribed` （標準: `email`、`created_at`、`unsubscribed`）
- Custom: Any key you define （カスタム: 定義した任意のキー）
- Computed: Aggregations from events （計算: イベントからの集計）

## When to Use （いつ使用するか）

- Behavior-based email automation （行動ベースのメール自動化）
- Multi-channel messaging (email, push, SMS) （マルチチャネルメッセージング (電子メール、プッシュ、SMS)）
- Onboarding sequences （オンボーディングシーケンス）
- Re-engagement campaigns （リエンゲージメントキャンペーン）
- Transactional messages （トランザクションメッセージ）

## Rate Limits （レート制限）

- Track API: 100 requests/second （トラック API: 100 リクエスト/秒）
- App API: 10 requests/second （アプリAPI: 10リクエスト/秒）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- onboarding-cro （オンボーディングクロ）
- analytics-tracking （分析追跡）
