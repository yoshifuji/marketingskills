# Mixpanel （日本語訳：ミックスパネル）

Product analytics platform for tracking user behavior and retention. （日本語訳：ユーザーの行動と維持を追跡するための製品分析プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Ingestion API, Query API, Data Export（日本語訳：インジェスト API、クエリ API、データ エクスポート） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | ✓ | JavaScript, iOS, Android, Python, etc.（日本語訳：JavaScript、iOS、Android、Python など） |

## Authentication （日本語訳：認証）

- **Ingestion**: Project token (public) （日本語訳：**取り込み**: プロジェクト トークン (パブリック)）
- **Query API**: Service Account (username:secret as Basic auth) （日本語訳：**クエリ API**: サービス アカウント (ユーザー名: 基本認証としてのシークレット)）
- **Export**: API Secret （日本語訳：**エクスポート**: API シークレット）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Track event (Ingestion API) （日本語訳：イベントの追跡 (取り込み API)）

```bash
POST https://api.mixpanel.com/track

{
  "event": "signup_completed",
  "properties": {
    "token": "{project_token}",
    "distinct_id": "user_123",
    "plan": "pro",
    "time": 1705312800
  }
}
```

### Set user profile （日本語訳：ユーザープロファイルを設定する）

```bash
POST https://api.mixpanel.com/engage

{
  "$token": "{project_token}",
  "$distinct_id": "user_123",
  "$set": {
    "$email": "user@example.com",
    "$name": "John Doe",
    "plan": "pro"
  }
}
```

### Query events (Query API) （日本語訳：クエリイベント（クエリAPI））

```bash
POST https://mixpanel.com/api/2.0/insights

{
  "project_id": {project_id},
  "bookmark_id": null,
  "params": {
    "events": [{"event": "signup_completed"}],
    "time_range": {
      "from_date": "2024-01-01",
      "to_date": "2024-01-31"
    }
  }
}
```

### Get funnel data （日本語訳：ファネルデータを取得する）

```bash
GET https://mixpanel.com/api/2.0/funnels?funnel_id={funnel_id}&from_date=2024-01-01&to_date=2024-01-31
```

### Export raw events （日本語訳：未処理のイベントをエクスポートする）

```bash
GET https://data.mixpanel.com/api/2.0/export?from_date=2024-01-01&to_date=2024-01-01
```

### Get retention data （日本語訳：保持データを取得する）

```bash
GET https://mixpanel.com/api/2.0/retention?from_date=2024-01-01&to_date=2024-01-31&retention_type=birth&born_event=signup_completed
```

## JavaScript SDK （日本語訳：JavaScript SDK）

```javascript
// Initialize
mixpanel.init('YOUR_TOKEN');

// Identify user
mixpanel.identify('user_123');

// Set user properties
mixpanel.people.set({
  '$email': 'user@example.com',
  'plan': 'pro'
});

// Track event
mixpanel.track('Feature Used', {
  'feature_name': 'export'
});
```

## Key Concepts （日本語訳：主要な概念）

- **Events** - User actions (signup, purchase, etc.) （日本語訳：**イベント** - ユーザーのアクション (サインアップ、購入など)）
- **Properties** - Attributes on events （日本語訳：**プロパティ** - イベントの属性）
- **User Profiles** - Persistent user data （日本語訳：**ユーザー プロファイル** - 永続的なユーザー データ）
- **Cohorts** - Saved user segments （日本語訳：**コホート** - 保存されたユーザー セグメント）
- **Funnels** - Conversion sequences （日本語訳：**ファネル** - 変換シーケンス）
- **Retention** - User return patterns （日本語訳：**リテンション** - ユーザーの復帰パターン）

## When to Use （日本語訳：いつ使用するか）

- Tracking product usage events （日本語訳：製品使用イベントの追跡）
- Analyzing conversion funnels （日本語訳：コンバージョンファネルの分析）
- Measuring feature adoption （日本語訳：機能の導入を測定する）
- Retention analysis （日本語訳：保持率分析）
- User segmentation （日本語訳：ユーザーのセグメンテーション）

## Rate Limits （日本語訳：レート制限）

- Ingestion: No hard limit (batch recommended) （日本語訳：取り込み: ハードリミットなし (バッチ推奨)）
- Query API: Varies by plan （日本語訳：クエリAPI: プランによって異なります）

## Relevant Skills （日本語訳：関連するスキル）

- analytics-tracking （日本語訳：分析追跡）
- ab-test-setup （日本語訳：ab-テストのセットアップ）
- onboarding-cro （日本語訳：オンボーディングクロ）
