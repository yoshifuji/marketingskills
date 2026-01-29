# Amplitude （振幅）

Product analytics platform for user behavior, retention, and experimentation. （ユーザーの行動、維持、実験のための製品分析プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | HTTP API for events, User Profile API, Export API（イベント用のHTTP API、ユーザープロファイルAPI、エクスポートAPI） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | JavaScript, iOS, Android, Python, etc.（JavaScript、iOS、Android、Python など） |

## Authentication （認証）

- **HTTP API**: API Key (public for events) （**HTTP API**: API キー (イベント用に公開)）
- **Export/Dashboard API**: API Key + Secret Key （**エクスポート/ダッシュボード API**: API キー + 秘密キー）

## Common Agent Operations （エージェントの共通操作）

### Track event （イベントを追跡する）

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

### Batch events （バッチイベント）

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

### Get user activity （ユーザーアクティビティを取得する）

```bash
GET https://amplitude.com/api/2/useractivity?user={user_id}

Authorization: Basic {base64(api_key:secret_key)}
```

### Export events （イベントのエクスポート）

```bash
GET https://amplitude.com/api/2/export?start=20240101T00&end=20240131T23

Authorization: Basic {base64(api_key:secret_key)}
```

### Get retention data （保持データを取得する）

```bash
GET https://amplitude.com/api/2/retention?e={"event_type":"signup_completed"}&start=20240101&end=20240131

Authorization: Basic {base64(api_key:secret_key)}
```

### Query with SQL (Snowflake) （SQL によるクエリ (スノーフレーク)）

For Amplitude customers with SQL access: （SQL アクセスを持つ Amplitude のお客様の場合:）
```sql
SELECT event_type, COUNT(*) as count
FROM events
WHERE event_time > '2024-01-01'
GROUP BY event_type
```

## JavaScript SDK （JavaScript SDK）

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

## Key Concepts （主要な概念）

- **Events** - User actions with properties （**イベント** - プロパティを使用したユーザー アクション）
- **User Properties** - Persistent user attributes （**ユーザー プロパティ** - 永続的なユーザー属性）
- **Cohorts** - Behavioral segments （**コホート** - 行動セグメント）
- **Funnels** - Multi-step conversion analysis （**ファネル** - 複数ステップの変換分析）
- **Retention** - User return patterns （**リテンション** - ユーザーの復帰パターン）
- **Journeys** - User path analysis （**ジャーニー** - ユーザー パス分析）

## When to Use （いつ使用するか）

- Tracking product analytics （製品分析の追跡）
- Analyzing user funnels （ユーザーファネルの分析）
- Cohort analysis and retention （コホート分析と保持）
- Experimentation and A/B testing （実験とA/Bテスト）
- User journey mapping （ユーザージャーニーマッピング）

## Rate Limits （レート制限）

- HTTP API: 1000 events/second （HTTP API: 1000 イベント/秒）
- Export API: 360 requests/hour （API のエクスポート: 360 リクエスト/時間）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- ab-test-setup （ab-テストのセットアップ）
- onboarding-cro （オンボーディングクロ）
