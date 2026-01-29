# Amplitude （日本語訳：振幅）

Product analytics platform for user behavior, retention, and experimentation. （日本語訳：ユーザーの行動、維持、実験のための製品分析プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | HTTP API for events, User Profile API, Export API（日本語訳：イベント用のHTTP API、ユーザープロファイルAPI、エクスポートAPI） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | JavaScript, iOS, Android, Python, etc.（日本語訳：JavaScript、iOS、Android、Python など） |

## Authentication （日本語訳：認証）

- **HTTP API**: API Key (public for events) （日本語訳：**HTTP API**: API キー (イベント用に公開)）
- **Export/Dashboard API**: API Key + Secret Key （日本語訳：**エクスポート/ダッシュボード API**: API キー + 秘密キー）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Track event （日本語訳：イベントを追跡する）

```bash
POST https://api2.amplitude.com/2/httpapi

{
  "api_key": "{api_key}",
  "events": [{
    "user_id": "user_123",
    "event_type": "signup_completed",
    "event_properties": {
      "plan": "pro"
    },
    "user_properties": {
      "email": "user@example.com"
    }
  }]
}
```

### Batch events （日本語訳：バッチイベント）

```bash
POST https://api2.amplitude.com/batch

{
  "api_key": "{api_key}",
  "events": [
    {"user_id": "user_1", "event_type": "pageview"},
    {"user_id": "user_2", "event_type": "signup"}
  ]
}
```

### Get user activity （日本語訳：ユーザーアクティビティを取得する）

```bash
GET https://amplitude.com/api/2/useractivity?user={user_id}

Authorization: Basic {base64(api_key:secret_key)}
```

### Export events （日本語訳：イベントのエクスポート）

```bash
GET https://amplitude.com/api/2/export?start=20240101T00&end=20240131T23

Authorization: Basic {base64(api_key:secret_key)}
```

### Get retention data （日本語訳：保持データを取得する）

```bash
GET https://amplitude.com/api/2/retention?e={"event_type":"signup_completed"}&start=20240101&end=20240131

Authorization: Basic {base64(api_key:secret_key)}
```

### Query with SQL (Snowflake) （日本語訳：SQL によるクエリ (スノーフレーク)）

For Amplitude customers with SQL access: （日本語訳：SQL アクセスを持つ Amplitude のお客様の場合:）
```sql
SELECT event_type, COUNT(*) as count
FROM events
WHERE event_time > '2024-01-01'
GROUP BY event_type
```

## JavaScript SDK （日本語訳：JavaScript SDK）

```javascript
// Initialize
amplitude.init('API_KEY');

// Identify user
amplitude.setUserId('user_123');

// Set user properties
const identify = new amplitude.Identify();
identify.set('plan', 'pro');
amplitude.identify(identify);

// Track event
amplitude.track('Feature Used', {
  feature_name: 'export'
});
```

## Key Concepts （日本語訳：主要な概念）

- **Events** - User actions with properties （日本語訳：**イベント** - プロパティを使用したユーザー アクション）
- **User Properties** - Persistent user attributes （日本語訳：**ユーザー プロパティ** - 永続的なユーザー属性）
- **Cohorts** - Behavioral segments （日本語訳：**コホート** - 行動セグメント）
- **Funnels** - Multi-step conversion analysis （日本語訳：**ファネル** - 複数ステップの変換分析）
- **Retention** - User return patterns （日本語訳：**リテンション** - ユーザーの復帰パターン）
- **Journeys** - User path analysis （日本語訳：**ジャーニー** - ユーザー パス分析）

## When to Use （日本語訳：いつ使用するか）

- Tracking product analytics （日本語訳：製品分析の追跡）
- Analyzing user funnels （日本語訳：ユーザーファネルの分析）
- Cohort analysis and retention （日本語訳：コホート分析と保持）
- Experimentation and A/B testing （日本語訳：実験とA/Bテスト）
- User journey mapping （日本語訳：ユーザージャーニーマッピング）

## Rate Limits （日本語訳：レート制限）

- HTTP API: 1000 events/second （日本語訳：HTTP API: 1000 イベント/秒）
- Export API: 360 requests/hour （日本語訳：API のエクスポート: 360 リクエスト/時間）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- ab-test-setup （日本語訳：ab-テストのセットアップ）
- onboarding-cro （日本語訳：オンボーディングクロ）
