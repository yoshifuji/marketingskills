# Kit (formerly ConvertKit) （キット (以前の ConvertKit)）

Email marketing platform for creators and newsletter businesses. （クリエイターおよびニュースレター ビジネス向けの電子メール マーケティング プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for subscribers, forms, sequences（サブスクライバー、フォーム、シーケンス用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | JavaScript, Ruby gems available（JavaScript、Ruby gem が利用可能） |

## Authentication （認証）

- **Type**: API Key or API Secret （**タイプ**: API キーまたは API シークレット）
- **Parameter**: `api_key={key}` or `api_secret={secret}` in query/body （**パラメータ**: クエリ/本文の `api_key={key}` または `api_secret={secret}`）
- **Get key**: Settings > Advanced in Kit dashboard （**キーの取得**: キット ダッシュボードの [設定] > [詳細設定]）

## Common Agent Operations （エージェントの共通操作）

### List subscribers （購読者のリストを表示する）

```bash
GET https://api.convertkit.com/v3/subscribers?api_secret={api_secret}&page=1

```

### Get subscriber （購読者の取得）

```bash
GET https://api.convertkit.com/v3/subscribers/{subscriber_id}?api_secret={api_secret}
```

### Add subscriber to form （購読者をフォームに追加）

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

### Add subscriber to sequence （サブスクライバをシーケンスに追加）

```bash
POST https://api.convertkit.com/v3/sequences/{sequence_id}/subscribe

{
  "api_key": "{api_key}",
  "email": "user@example.com"
}
```

### Tag subscriber （タグ登録者）

```bash
POST https://api.convertkit.com/v3/tags/{tag_id}/subscribe

{
  "api_key": "{api_key}",
  "email": "user@example.com"
}
```

### Remove tag from subscriber （購読者からタグを削除する）

```bash
DELETE https://api.convertkit.com/v3/subscribers/{subscriber_id}/tags/{tag_id}?api_secret={api_secret}
```

### Update subscriber （購読者を更新する）

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

### Unsubscribe （購読を解除する）

```bash
PUT https://api.convertkit.com/v3/unsubscribe

{
  "api_secret": "{api_secret}",
  "email": "user@example.com"
}
```

### List forms （リストフォーム）

```bash
GET https://api.convertkit.com/v3/forms?api_key={api_key}
```

### List sequences （リストシーケンス）

```bash
GET https://api.convertkit.com/v3/sequences?api_key={api_key}
```

### List tags （リストタグ）

```bash
GET https://api.convertkit.com/v3/tags?api_key={api_key}
```

### Create broadcast （ブロードキャストの作成）

```bash
POST https://api.convertkit.com/v3/broadcasts

{
  "api_secret": "{api_secret}",
  "subject": "Newsletter Subject",
  "content": "<p>Email content here</p>",
  "email_layout_template": "default"
}
```

## Key Concepts （主要な概念）

- **Subscribers** - Email contacts （**購読者** - 電子メール連絡先）
- **Forms** - Signup forms （**フォーム** - 登録フォーム）
- **Sequences** - Automated email series （**シーケンス** - 一連の自動電子メール）
- **Tags** - Subscriber labels （**タグ** - 購読者ラベル）
- **Broadcasts** - One-time sends （**ブロードキャスト** - 1 回限りの送信）
- **Custom Fields** - Subscriber attributes （**カスタム フィールド** - 購読者の属性）

## Subscriber States （加入者の州）

- `active` - Can receive emails （`active` - 電子メールを受信できます）
- `unsubscribed` - Opted out （`unsubscribed` - オプトアウトしました）
- `bounced` - Email bounced （`bounced` - 電子メールが返送されました）
- `complained` - Marked as spam （`complained` - スパムとしてマークされています）
- `inactive` - Cold subscriber （`inactive` - コールドサブスクライバ）

## When to Use （いつ使用するか）

- Creator/newsletter businesses （クリエイター・ニュースレター事業）
- Simple email automation （シンプルなメール自動化）
- Form-based list building （フォームベースのリスト構築）
- Tagging and segmentation （タグ付けとセグメンテーション）
- Course email sequences （コースメールシーケンス）

## Rate Limits （レート制限）

- 120 requests per minute （1 分あたり 120 リクエスト）
- Batch endpoints available （利用可能なバッチエンドポイント）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- content-strategy （コンテンツ戦略）
