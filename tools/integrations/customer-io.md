# Customer.io （日本語訳：Customer.io）

Behavior-based messaging platform for email, push, SMS, and in-app. （日本語訳：電子メール、プッシュ、SMS、アプリ内向けの行動ベースのメッセージング プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Track API, App API, Journeys API（日本語訳：Track API、App API、Journeys API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | JavaScript, iOS, Android, Ruby, Python（日本語訳：JavaScript、iOS、Android、Ruby、Python） |

## Authentication （日本語訳：認証）

- **Track API**: Site ID + API Key (Basic auth) （日本語訳：**Track API**: サイト ID + API キー (基本認証)）
- **App API**: Bearer token （日本語訳：**アプリ API**: ベアラー トークン）
- **Header**: `Authorization: Basic {base64(site_id:api_key)}` （日本語訳：**ヘッダー**: `Authorization: Basic {base64(site_id:api_key)}`）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Identify customer （日本語訳：顧客を特定する）

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

### Track event （日本語訳：イベントを追跡する）

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

### Track anonymous event （日本語訳：匿名イベントを追跡する）

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

### Delete customer （日本語訳：顧客の削除）

```bash
DELETE https://track.customer.io/api/v1/customers/{customer_id}

Authorization: Basic {base64(site_id:api_key)}
```

### Get customer (App API) （日本語訳：顧客の獲得（アプリAPI））

```bash
GET https://api.customer.io/v1/customers/{customer_id}/attributes

Authorization: Bearer {app_api_key}
```

### List campaigns （日本語訳：リストキャンペーン）

```bash
GET https://api.customer.io/v1/campaigns

Authorization: Bearer {app_api_key}
```

### Get campaign metrics （日本語訳：キャンペーン指標を取得する）

```bash
GET https://api.customer.io/v1/campaigns/{campaign_id}/metrics

Authorization: Bearer {app_api_key}
```

### Trigger broadcast （日本語訳：トリガーブロードキャスト）

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

### Send transactional email （日本語訳：取引メールを送信する）

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

## JavaScript SDK （日本語訳：JavaScript SDK）

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

## Key Concepts （日本語訳：主要な概念）

- **People** - Customers and leads （日本語訳：**人** - 顧客とリード）
- **Segments** - Dynamic groups based on attributes/behavior （日本語訳：**セグメント** - 属性/動作に基づく動的グループ）
- **Campaigns** - Automated message sequences （日本語訳：**キャンペーン** - 自動化されたメッセージ シーケンス）
- **Broadcasts** - One-time sends （日本語訳：**ブロードキャスト** - 1 回限りの送信）
- **Transactional** - Triggered messages （日本語訳：**トランザクション** - トリガーされたメッセージ）

## Attribute Types （日本語訳：属性の種類）

- Standard: `email`, `created_at`, `unsubscribed` （日本語訳：標準: `email`、`created_at`、`unsubscribed`）
- Custom: Any key you define （日本語訳：カスタム: 定義した任意のキー）
- Computed: Aggregations from events （日本語訳：計算: イベントからの集計）

## When to Use （日本語訳：いつ使用するか）

- Behavior-based email automation （日本語訳：行動ベースのメール自動化）
- Multi-channel messaging (email, push, SMS) （日本語訳：マルチチャネルメッセージング (電子メール、プッシュ、SMS)）
- Onboarding sequences （日本語訳：オンボーディングシーケンス）
- Re-engagement campaigns （日本語訳：リエンゲージメントキャンペーン）
- Transactional messages （日本語訳：トランザクションメッセージ）

## Rate Limits （日本語訳：レート制限）

- Track API: 100 requests/second （日本語訳：トラック API: 100 リクエスト/秒）
- App API: 10 requests/second （日本語訳：アプリAPI: 10リクエスト/秒）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- onboarding-cro （日本語訳：オンボーディングクロ）
- analytics-tracking （日本語訳：分析追跡）
