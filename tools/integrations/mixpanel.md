# Mixpanel （ミックスパネル）

Product analytics platform for tracking user behavior and retention. （ユーザーの行動と維持を追跡するための製品分析プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Ingestion API, Query API, Data Export（インジェスト API、クエリ API、データ エクスポート） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | ✓ | JavaScript, iOS, Android, Python, etc.（JavaScript、iOS、Android、Python など） |

## Authentication （認証）

- **Ingestion**: Project token (public) （**取り込み**: プロジェクト トークン (パブリック)）
- **Query API**: Service Account (username:secret as Basic auth) （**クエリ API**: サービス アカウント (ユーザー名: 基本認証としてのシークレット)）
- **Export**: API Secret （**エクスポート**: API シークレット）

## Common Agent Operations （エージェントの共通操作）

### Track event (Ingestion API) （イベントの追跡 (取り込み API)）

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

### Set user profile （ユーザープロファイルを設定する）

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

### Query events (Query API) （クエリイベント（クエリAPI））

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

### Get funnel data （ファネルデータを取得する）

```bash
GET https://mixpanel.com/api/2.0/funnels?funnel_id={funnel_id}&from_date=2024-01-01&to_date=2024-01-31
```

### Export raw events （未処理のイベントをエクスポートする）

```bash
GET https://data.mixpanel.com/api/2.0/export?from_date=2024-01-01&to_date=2024-01-01
```

### Get retention data （保持データを取得する）

```bash
GET https://mixpanel.com/api/2.0/retention?from_date=2024-01-01&to_date=2024-01-31&retention_type=birth&born_event=signup_completed
```

## JavaScript SDK （JavaScript SDK）

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

## Key Concepts （主要な概念）

- **Events** - User actions (signup, purchase, etc.) （**イベント** - ユーザーのアクション (サインアップ、購入など)）
- **Properties** - Attributes on events （**プロパティ** - イベントの属性）
- **User Profiles** - Persistent user data （**ユーザー プロファイル** - 永続的なユーザー データ）
- **Cohorts** - Saved user segments （**コホート** - 保存されたユーザー セグメント）
- **Funnels** - Conversion sequences （**ファネル** - 変換シーケンス）
- **Retention** - User return patterns （**リテンション** - ユーザーの復帰パターン）

## When to Use （いつ使用するか）

- Tracking product usage events （製品使用イベントの追跡）
- Analyzing conversion funnels （コンバージョンファネルの分析）
- Measuring feature adoption （機能の導入を測定する）
- Retention analysis （保持率分析）
- User segmentation （ユーザーのセグメンテーション）

## Rate Limits （レート制限）

- Ingestion: No hard limit (batch recommended) （取り込み: ハードリミットなし (バッチ推奨)）
- Query API: Varies by plan （クエリAPI: プランによって異なります）

## Relevant Skills （関連するスキル）

- analytics-tracking （分析追跡）
- ab-test-setup （ab-テストのセットアップ）
- onboarding-cro （オンボーディングクロ）
