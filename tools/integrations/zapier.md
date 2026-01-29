# Zapier （日本語訳：ザピエル）

Workflow automation platform connecting apps without code. （日本語訳：コードなしでアプリを接続するワークフロー自動化プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for Zaps, tasks, and webhooks（日本語訳：Zaps、タスク、Webhook 用の REST API） |
| MCP（日本語訳：MCP） | ✓ | Available via Zapier MCP server（日本語訳：Zapier MCP サーバー経由で利用可能） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | API and webhooks only（日本語訳：APIとWebhookのみ） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Header**: `X-API-Key: {api_key}` （日本語訳：**ヘッダー**: `X-API-Key: {api_key}`）
- **Get key**: Settings > API in Zapier account （日本語訳：**キーの取得**: Zapier アカウントの [設定] > [API]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List Zaps （日本語訳：ザップをリストする）

```bash
GET https://api.zapier.com/v1/zaps
```

### Get Zap details （日本語訳：ザップの詳細を取得する）

```bash
GET https://api.zapier.com/v1/zaps/{zap_id}
```

### Turn Zap on/off （日本語訳：ザップのオン/オフを切り替える）

```bash
POST https://api.zapier.com/v1/zaps/{zap_id}/on
POST https://api.zapier.com/v1/zaps/{zap_id}/off
```

### Get task history （日本語訳：タスク履歴を取得する）

```bash
GET https://api.zapier.com/v1/zaps/{zap_id}/tasks
```

### Get profile info （日本語訳：プロフィール情報を取得する）

```bash
GET https://api.zapier.com/v1/profiles/me
```

## Webhooks (Triggers) （日本語訳：Webhook (トリガー)）

### Catch Hook (receive data) （日本語訳：キャッチフック（データ受信））

Create a "Webhooks by Zapier" trigger to receive data: （日本語訳：データを受信するための「Webhooks by Zapier」トリガーを作成します。）

```bash
POST https://hooks.zapier.com/hooks/catch/{webhook_id}/

{
  "event": "user.created",
  "user_id": "123",
  "email": "user@example.com"
}
```

### Send data to Zapier （日本語訳：Zapier にデータを送信する）

Most common: trigger a Zap from your app: （日本語訳：最も一般的な方法: アプリから Zap をトリガーします。）

```bash
POST https://hooks.zapier.com/hooks/catch/{account_id}/{hook_id}/

{
  "name": "John Doe",
  "email": "john@example.com",
  "plan": "pro"
}
```

## Common Marketing Automations （日本語訳：一般的なマーケティングオートメーション）

### Lead capture to CRM （日本語訳：CRMへのリード獲得）
```
Typeform → Zapier → HubSpot
```

### New customer notifications （日本語訳：新規のお客様へのお知らせ）
```
Stripe (new customer) → Zapier → Slack
```

### Email sequence triggers （日本語訳：電子メールシーケンストリガー）
```
Form submission → Zapier → Customer.io
```

### Social proof automation （日本語訳：社会的証明の自動化）
```
New review → Zapier → Twitter/Slack
```

### Referral tracking （日本語訳：紹介追跡）
```
New referral → Zapier → Spreadsheet + Slack
```

## Webhook Payload Structure （日本語訳：Webhook ペイロード構造）

When sending to Zapier, structure data as flat JSON: （日本語訳：Zapier に送信する場合は、データをフラットな JSON として構造化します。）

```json
{
  "customer_name": "John Doe",
  "customer_email": "john@example.com",
  "plan_name": "Pro",
  "plan_price": 99,
  "signup_date": "2024-01-15"
}
```

## Key Concepts （日本語訳：主要な概念）

- **Zap** - Automated workflow （日本語訳：**Zap** - 自動化されたワークフロー）
- **Trigger** - Event that starts a Zap （日本語訳：**トリガー** - ザップを開始するイベント）
- **Action** - Task performed by Zap （日本語訳：**アクション** - Zap によって実行されるタスク）
- **Task** - Single action execution （日本語訳：**タスク** - 単一アクションの実行）
- **Filter** - Conditional logic （日本語訳：**フィルター** - 条件付きロジック）
- **Path** - Branching logic （日本語訳：**パス** - 分岐ロジック）

## When to Use （日本語訳：いつ使用するか）

- Connecting marketing tools without code （日本語訳：コードなしでマーケティング ツールを接続する）
- Automating lead routing （日本語訳：リードルーティングの自動化）
- Syncing data between platforms （日本語訳：プラットフォーム間でのデータの同期）
- Triggering notifications （日本語訳：通知のトリガー）
- Building marketing workflows （日本語訳：マーケティングワークフローの構築）

## Rate Limits （日本語訳：レート制限）

- 100 requests per minute （日本語訳：1 分あたり 100 リクエスト）
- Task limits by plan tier （日本語訳：プラン階層ごとのタスク制限）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- analytics-tracking （日本語訳：分析追跡）
- referral-program （日本語訳：紹介プログラム）
