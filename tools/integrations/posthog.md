# PostHog （ポストホッグ）

Open-source product analytics with session replay and feature flags. （セッション リプレイと機能フラグを使用したオープンソースの製品分析。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Capture API, Query API, Feature Flags API（キャプチャ API、クエリ API、機能フラグ API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | `posthog` CLI for local development（`posthog` ローカル開発用の CLI） |
| SDK（SDK） | ✓ | JavaScript, Python, Ruby, Go, etc.（JavaScript、Python、Ruby、Go など） |

## Authentication （認証）

- **Type**: API Key (Personal or Project) （**タイプ**: API キー (個人またはプロジェクト)）
- **Header**: `Authorization: Bearer {api_key}` （**ヘッダー**: `Authorization: Bearer {api_key}`）
- **For capture**: Project API Key in payload （**キャプチャの場合**: ペイロード内のプロジェクト API キー）

## Common Agent Operations （エージェントの共通操作）

### Capture event （キャプチャイベント）

```bash
POST https://app.posthog.com/capture/

{
  "api_key": "{project_api_key}",
  "event": "signup_completed",
  "distinct_id": "user_123",
  "properties": {
    "plan": "pro",
    "$current_url": "https://example.com/signup"
  }
}
```

### Batch events （バッチイベント）

```bash
POST https://app.posthog.com/batch/

{
  "api_key": "{project_api_key}",
  "batch": [
    {"event": "pageview", "distinct_id": "user_1"},
    {"event": "signup", "distinct_id": "user_2"}
  ]
}
```

### Get person by distinct_id （unique_id で人物を取得する）

```bash
GET https://app.posthog.com/api/projects/{project_id}/persons/?distinct_id=user_123

Authorization: Bearer {api_key}
```

### Query events (HogQL) （クエリイベント (HogQL)）

```bash
POST https://app.posthog.com/api/projects/{project_id}/query/

{
  "query": {
    "kind": "HogQLQuery",
    "query": "SELECT event, count() FROM events WHERE timestamp > now() - interval 7 day GROUP BY event ORDER BY count() DESC LIMIT 10"
  }
}
```

### Get feature flag value （機能フラグ値を取得する）

```bash
POST https://app.posthog.com/decide?v=3

{
  "api_key": "{project_api_key}",
  "distinct_id": "user_123"
}
```

### Get insights （洞察を得る）

```bash
GET https://app.posthog.com/api/projects/{project_id}/insights/

Authorization: Bearer {api_key}
```

### Get session recordings （セッションの記録を取得する）

```bash
GET https://app.posthog.com/api/projects/{project_id}/session_recordings/

Authorization: Bearer {api_key}
```

## JavaScript SDK （JavaScript SDK）

```javascript
// Initialize
posthog.init('PROJECT_API_KEY', {
  api_host: 'https://app.posthog.com'
});

// Identify user
posthog.identify('user_123', {
  email: 'user@example.com',
  plan: 'pro'
});

// Track event
posthog.capture('signup_completed', {
  method: 'email'
});

// Check feature flag
if (posthog.isFeatureEnabled('new-pricing')) {
  // Show new pricing
}
```

## Key Features （主な特長）

- **Event tracking** - Product analytics （**イベント追跡** - 製品分析）
- **Session replay** - Watch user sessions （**セッションのリプレイ** - ユーザー セッションを監視します）
- **Feature flags** - Control feature rollout （**機能フラグ** - コントロール機能ロールアウト）
- **A/B testing** - Built-in experiments （**A/B テスト** - 組み込みの実験）
- **HogQL** - SQL-like query language （**HogQL** - SQL に似たクエリ言語）
- **Self-hostable** - Run on your infrastructure （**自己ホスト可能** - インフラストラクチャ上で実行）

## When to Use （いつ使用するか）

- Product analytics with privacy focus （プライバシーを重視した製品分析）
- Session replay for UX insights （セッションをリプレイしてUXに関する洞察を得る）
- Feature flag management （機能フラグ管理）
- Self-hosted analytics needs （自己ホスト型分析のニーズ）
- Open-source requirements （オープンソースの要件）

## Rate Limits （レート制限）

- Cloud: 10,000 events/second （クラウド: 10,000 イベント/秒）
- Self-hosted: Unlimited （セルフホスト型: 無制限）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- ab-test-setup （ab-テストのセットアップ）
- onboarding-cro （オンボーディングクロ）
