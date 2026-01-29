# Kit (formerly ConvertKit) （日本語訳：キット (以前の ConvertKit)）

Email marketing platform for creators and newsletter businesses. （日本語訳：クリエイターおよびニュースレター ビジネス向けの電子メール マーケティング プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for subscribers, forms, sequences（日本語訳：サブスクライバー、フォーム、シーケンス用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | JavaScript, Ruby gems available（日本語訳：JavaScript、Ruby gem が利用可能） |

## Authentication （日本語訳：認証）

- **Type**: API Key or API Secret （日本語訳：**タイプ**: API キーまたは API シークレット）
- **Parameter**: `api_key={key}` or `api_secret={secret}` in query/body （日本語訳：**パラメータ**: クエリ/本文の `api_key={key}` または `api_secret={secret}`）
- **Get key**: Settings > Advanced in Kit dashboard （日本語訳：**キーの取得**: キット ダッシュボードの [設定] > [詳細設定]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List subscribers （日本語訳：購読者のリストを表示する）

```bash
GET https://api.convertkit.com/v3/subscribers?api_secret={api_secret}&page=1

```

### Get subscriber （日本語訳：購読者の取得）

```bash
GET https://api.convertkit.com/v3/subscribers/{subscriber_id}?api_secret={api_secret}
```

### Add subscriber to form （日本語訳：購読者をフォームに追加）

```bash
POST https://api.convertkit.com/v3/forms/{form_id}/subscribe

{
  "api_key": "{api_key}",
  "email": "user@example.com",
  "first_name": "John",
  "fields": {
    "company": "Example Inc"
  }
}
```

### Add subscriber to sequence （日本語訳：サブスクライバをシーケンスに追加）

```bash
POST https://api.convertkit.com/v3/sequences/{sequence_id}/subscribe

{
  "api_key": "{api_key}",
  "email": "user@example.com"
}
```

### Tag subscriber （日本語訳：タグ登録者）

```bash
POST https://api.convertkit.com/v3/tags/{tag_id}/subscribe

{
  "api_key": "{api_key}",
  "email": "user@example.com"
}
```

### Remove tag from subscriber （日本語訳：購読者からタグを削除する）

```bash
DELETE https://api.convertkit.com/v3/subscribers/{subscriber_id}/tags/{tag_id}?api_secret={api_secret}
```

### Update subscriber （日本語訳：購読者を更新する）

```bash
PUT https://api.convertkit.com/v3/subscribers/{subscriber_id}

{
  "api_secret": "{api_secret}",
  "first_name": "Jane",
  "fields": {
    "plan": "pro"
  }
}
```

### Unsubscribe （日本語訳：購読を解除する）

```bash
PUT https://api.convertkit.com/v3/unsubscribe

{
  "api_secret": "{api_secret}",
  "email": "user@example.com"
}
```

### List forms （日本語訳：リストフォーム）

```bash
GET https://api.convertkit.com/v3/forms?api_key={api_key}
```

### List sequences （日本語訳：リストシーケンス）

```bash
GET https://api.convertkit.com/v3/sequences?api_key={api_key}
```

### List tags （日本語訳：リストタグ）

```bash
GET https://api.convertkit.com/v3/tags?api_key={api_key}
```

### Create broadcast （日本語訳：ブロードキャストの作成）

```bash
POST https://api.convertkit.com/v3/broadcasts

{
  "api_secret": "{api_secret}",
  "subject": "Newsletter Subject",
  "content": "<p>Email content here</p>",
  "email_layout_template": "default"
}
```

## Key Concepts （日本語訳：主要な概念）

- **Subscribers** - Email contacts （日本語訳：**購読者** - 電子メール連絡先）
- **Forms** - Signup forms （日本語訳：**フォーム** - 登録フォーム）
- **Sequences** - Automated email series （日本語訳：**シーケンス** - 一連の自動電子メール）
- **Tags** - Subscriber labels （日本語訳：**タグ** - 購読者ラベル）
- **Broadcasts** - One-time sends （日本語訳：**ブロードキャスト** - 1 回限りの送信）
- **Custom Fields** - Subscriber attributes （日本語訳：**カスタム フィールド** - 購読者の属性）

## Subscriber States （日本語訳：加入者の州）

- `active` - Can receive emails （日本語訳：`active` - 電子メールを受信できます）
- `unsubscribed` - Opted out （日本語訳：`unsubscribed` - オプトアウトしました）
- `bounced` - Email bounced （日本語訳：`bounced` - 電子メールが返送されました）
- `complained` - Marked as spam （日本語訳：`complained` - スパムとしてマークされています）
- `inactive` - Cold subscriber （日本語訳：`inactive` - コールドサブスクライバ）

## When to Use （日本語訳：いつ使用するか）

- Creator/newsletter businesses （日本語訳：クリエイター・ニュースレター事業）
- Simple email automation （日本語訳：シンプルなメール自動化）
- Form-based list building （日本語訳：フォームベースのリスト構築）
- Tagging and segmentation （日本語訳：タグ付けとセグメンテーション）
- Course email sequences （日本語訳：コースメールシーケンス）

## Rate Limits （日本語訳：レート制限）

- 120 requests per minute （日本語訳：1 分あたり 120 リクエスト）
- Batch endpoints available （日本語訳：利用可能なバッチエンドポイント）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- content-strategy （日本語訳：コンテンツ戦略）
