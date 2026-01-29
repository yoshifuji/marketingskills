# Zapier （ザピエル）

Workflow automation platform connecting apps without code. （コードなしでアプリを接続するワークフロー自動化プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for Zaps, tasks, and webhooks（Zaps、タスク、Webhook 用の REST API） |
| MCP（MCP） | ✓ | Available via Zapier MCP server（Zapier MCP サーバー経由で利用可能） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | API and webhooks only（APIとWebhookのみ） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Header**: `X-API-Key: {api_key}` （**ヘッダー**: `X-API-Key: {api_key}`）
- **Get key**: Settings > API in Zapier account （**キーの取得**: Zapier アカウントの [設定] > [API]）

## Common Agent Operations （エージェントの共通操作）

### List Zaps （ザップをリストする）

```bash
GET https://api.zapier.com/v1/zaps
```

### Get Zap details （ザップの詳細を取得する）

```bash
GET https://api.zapier.com/v1/zaps/{zap_id}
```

### Turn Zap on/off （ザップのオン/オフを切り替える）

```bash
POST https://api.zapier.com/v1/zaps/{zap_id}/on
POST https://api.zapier.com/v1/zaps/{zap_id}/off
```

### Get task history （タスク履歴を取得する）

```bash
GET https://api.zapier.com/v1/zaps/{zap_id}/tasks
```

### Get profile info （プロフィール情報を取得する）

```bash
GET https://api.zapier.com/v1/profiles/me
```

## Webhooks (Triggers) （Webhook (トリガー)）

### Catch Hook (receive data) （キャッチフック（データ受信））

Create a "Webhooks by Zapier" trigger to receive data: （データを受信するための「Webhooks by Zapier」トリガーを作成します。）

```bash
POST https://hooks.zapier.com/hooks/catch/{webhook_id}/

{
  "event": "user.created",
  "user_id": "123",
  "email": "user@example.com"
}
```

### Send data to Zapier （Zapier にデータを送信する）

Most common: trigger a Zap from your app: （最も一般的な方法: アプリから Zap をトリガーします。）

```bash
POST https://hooks.zapier.com/hooks/catch/{account_id}/{hook_id}/

{
  "name": "John Doe",
  "email": "john@example.com",
  "plan": "pro"
}
```

## Common Marketing Automations （一般的なマーケティングオートメーション）

### Lead capture to CRM （CRMへのリード獲得）
```
Typeform → Zapier → HubSpot
```

### New customer notifications （新規のお客様へのお知らせ）
```
Stripe (new customer) → Zapier → Slack
```

### Email sequence triggers （電子メールシーケンストリガー）
```
Form submission → Zapier → Customer.io
```

### Social proof automation （社会的証明の自動化）
```
New review → Zapier → Twitter/Slack
```

### Referral tracking （紹介追跡）
```
New referral → Zapier → Spreadsheet + Slack
```

## Webhook Payload Structure （Webhook ペイロード構造）

When sending to Zapier, structure data as flat JSON: （Zapier に送信する場合は、データをフラットな JSON として構造化します。）

```json
{
  "customer_name": "John Doe",
  "customer_email": "john@example.com",
  "plan_name": "Pro",
  "plan_price": 99,
  "signup_date": "2024-01-15"
}
```

## Key Concepts （主要な概念）

- **Zap** - Automated workflow （**Zap** - 自動化されたワークフロー）
- **Trigger** - Event that starts a Zap （**トリガー** - ザップを開始するイベント）
- **Action** - Task performed by Zap （**アクション** - Zap によって実行されるタスク）
- **Task** - Single action execution （**タスク** - 単一アクションの実行）
- **Filter** - Conditional logic （**フィルター** - 条件付きロジック）
- **Path** - Branching logic （**パス** - 分岐ロジック）

## When to Use （いつ使用するか）

- Connecting marketing tools without code （コードなしでマーケティング ツールを接続する）
- Automating lead routing （リードルーティングの自動化）
- Syncing data between platforms （プラットフォーム間でのデータの同期）
- Triggering notifications （通知のトリガー）
- Building marketing workflows （マーケティングワークフローの構築）

## Rate Limits （レート制限）

- 100 requests per minute （1 分あたり 100 リクエスト）
- Task limits by plan tier （プラン階層ごとのタスク制限）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- analytics-tracking （分析追跡）
- referral-program （紹介プログラム）
