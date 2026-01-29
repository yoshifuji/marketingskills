# PostHog （日本語訳：ポストホッグ）

Open-source product analytics with session replay and feature flags. （日本語訳：セッション リプレイと機能フラグを使用したオープンソースの製品分析。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Capture API, Query API, Feature Flags API（日本語訳：キャプチャ API、クエリ API、機能フラグ API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | `posthog` CLI for local development（日本語訳：`posthog` ローカル開発用の CLI） |
| SDK（日本語訳：SDK） | ✓ | JavaScript, Python, Ruby, Go, etc.（日本語訳：JavaScript、Python、Ruby、Go など） |

## Authentication （日本語訳：認証）

- **Type**: API Key (Personal or Project) （日本語訳：**タイプ**: API キー (個人またはプロジェクト)）
- **Header**: `Authorization: Bearer {api_key}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_key}`）
- **For capture**: Project API Key in payload （日本語訳：**キャプチャの場合**: ペイロード内のプロジェクト API キー）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Capture event （日本語訳：キャプチャイベント）

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

### Batch events （日本語訳：バッチイベント）

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

### Get person by distinct_id （日本語訳：unique_id で人物を取得する）

```bash
GET https://app.posthog.com/api/projects/{project_id}/persons/?distinct_id=user_123

Authorization: Bearer {api_key}
```

### Query events (HogQL) （日本語訳：クエリイベント (HogQL)）

```bash
POST https://app.posthog.com/api/projects/{project_id}/query/

{
  "query": {
    "kind": "HogQLQuery",
    "query": "SELECT event, count() FROM events WHERE timestamp > now() - interval 7 day GROUP BY event ORDER BY count() DESC LIMIT 10"
  }
}
```

### Get feature flag value （日本語訳：機能フラグ値を取得する）

```bash
POST https://app.posthog.com/decide?v=3

{
  "api_key": "{project_api_key}",
  "distinct_id": "user_123"
}
```

### Get insights （日本語訳：洞察を得る）

```bash
GET https://app.posthog.com/api/projects/{project_id}/insights/

Authorization: Bearer {api_key}
```

### Get session recordings （日本語訳：セッションの記録を取得する）

```bash
GET https://app.posthog.com/api/projects/{project_id}/session_recordings/

Authorization: Bearer {api_key}
```

## JavaScript SDK （日本語訳：JavaScript SDK）

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

## Key Features （日本語訳：主な特長）

- **Event tracking** - Product analytics （日本語訳：**イベント追跡** - 製品分析）
- **Session replay** - Watch user sessions （日本語訳：**セッションのリプレイ** - ユーザー セッションを監視します）
- **Feature flags** - Control feature rollout （日本語訳：**機能フラグ** - コントロール機能ロールアウト）
- **A/B testing** - Built-in experiments （日本語訳：**A/B テスト** - 組み込みの実験）
- **HogQL** - SQL-like query language （日本語訳：**HogQL** - SQL に似たクエリ言語）
- **Self-hostable** - Run on your infrastructure （日本語訳：**自己ホスト可能** - インフラストラクチャ上で実行）

## When to Use （日本語訳：いつ使用するか）

- Product analytics with privacy focus （日本語訳：プライバシーを重視した製品分析）
- Session replay for UX insights （日本語訳：セッションをリプレイしてUXに関する洞察を得る）
- Feature flag management （日本語訳：機能フラグ管理）
- Self-hosted analytics needs （日本語訳：自己ホスト型分析のニーズ）
- Open-source requirements （日本語訳：オープンソースの要件）

## Rate Limits （日本語訳：レート制限）

- Cloud: 10,000 events/second （日本語訳：クラウド: 10,000 イベント/秒）
- Self-hosted: Unlimited （日本語訳：セルフホスト型: 無制限）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- ab-test-setup （日本語訳：ab-テストのセットアップ）
- onboarding-cro （日本語訳：オンボーディングクロ）
