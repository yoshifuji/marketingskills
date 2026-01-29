# GA4 Implementation Reference （日本語訳：GA4 実装リファレンス）

Detailed implementation guide for Google Analytics 4. （日本語訳：Google Analytics 4 の詳細な実装ガイド。）

## Configuration （日本語訳：構成）

### Data Streams （日本語訳：データストリーム）

- One stream per platform (web, iOS, Android) （日本語訳：プラットフォームごとに 1 つのストリーム (Web、iOS、Android)）
- Enable enhanced measurement for automatic tracking （日本語訳：自動追跡のための拡張測定を有効にする）
- Configure data retention (2 months default, 14 months max) （日本語訳：データ保持の構成 (デフォルトは 2 か月、最大 14 か月)）
- Enable Google Signals (for cross-device, if consented) （日本語訳：Google シグナルを有効にする (同意されている場合、クロスデバイス用)）

### Enhanced Measurement Events (Automatic) （日本語訳：拡張測定イベント (自動)）

| Event（日本語訳：イベント） | Description（日本語訳：説明） | Configuration（日本語訳：構成） |
|-------|-------------|---------------|
| page_view（日本語訳：ページビュー） | Page loads（日本語訳：ページの読み込み） | Automatic（日本語訳：自動） |
| scroll（日本語訳：スクロール） | 90% scroll depth（日本語訳：スクロール深度 90%） | Toggle on/off（日本語訳：オン/オフを切り替えます） |
| outbound_click（日本語訳：outbound_click） | Click to external domain（日本語訳：クリックして外部ドメインへ） | Automatic（日本語訳：自動） |
| site_search（日本語訳：サイト検索） | Search query used（日本語訳：使用された検索クエリ） | Configure parameter（日本語訳：パラメータの設定） |
| video_engagement（日本語訳：ビデオエンゲージメント） | YouTube video plays（日本語訳：YouTube ビデオの再生） | Toggle on/off（日本語訳：オン/オフを切り替えます） |
| file_download（日本語訳：ファイル_ダウンロード） | PDF, docs, etc.（日本語訳：PDF、ドキュメントなど） | Configurable extensions（日本語訳：構成可能な拡張機能） |

### Recommended Events （日本語訳：おすすめイベント）

Use Google's predefined events when possible for enhanced reporting: （日本語訳：レポートを強化するには、可能な場合は Google の事前定義イベントを使用します。）

**All properties:** （日本語訳：**すべてのプロパティ:**）
- login, sign_up （日本語訳：ログイン、サインアップ）
- share （日本語訳：共有）
- search （日本語訳：検索）

**E-commerce:** （日本語訳：**電子商取引:**）
- view_item, view_item_list （日本語訳：view_item、view_item_list）
- add_to_cart, remove_from_cart （日本語訳：カートに追加、カートから削除）
- begin_checkout （日本語訳：チェックアウトの開始）
- add_payment_info （日本語訳：add_payment_info）
- purchase, refund （日本語訳：購入、返金）

**Games:** （日本語訳：**ゲーム:**）
- level_up, unlock_achievement （日本語訳：レベルアップ、アンロックアチーブメント）
- post_score, spend_virtual_currency （日本語訳：post_score、spend_virtual_currency）

Reference: https://support.google.com/analytics/answer/9267735 （日本語訳：参照: https://support.google.com/analytics/answer/9267735）

---

## Custom Events （日本語訳：カスタムイベント）

### gtag.js Implementation （日本語訳：gtag.jsの実装）

```javascript
// Basic event
gtag('event', 'signup_completed', {
  'method': 'email',
  'plan': 'free'
});

// Event with value
gtag('event', 'purchase', {
  'transaction_id': 'T12345',
  'value': 99.99,
  'currency': 'USD',
  'items': [{
    'item_id': 'SKU123',
    'item_name': 'Product Name',
    'price': 99.99
  }]
});

// User properties
gtag('set', 'user_properties', {
  'user_type': 'premium',
  'plan_name': 'pro'
});

// User ID (for logged-in users)
gtag('config', 'GA_MEASUREMENT_ID', {
  'user_id': 'USER_ID'
});
```

### Google Tag Manager (dataLayer) （日本語訳：Google タグマネージャー (dataLayer)）

```javascript
// Custom event
dataLayer.push({
  'event': 'signup_completed',
  'method': 'email',
  'plan': 'free'
});

// Set user properties
dataLayer.push({
  'user_id': '12345',
  'user_type': 'premium'
});

// E-commerce purchase
dataLayer.push({
  'event': 'purchase',
  'ecommerce': {
    'transaction_id': 'T12345',
    'value': 99.99,
    'currency': 'USD',
    'items': [{
      'item_id': 'SKU123',
      'item_name': 'Product Name',
      'price': 99.99,
      'quantity': 1
    }]
  }
});

// Clear ecommerce before sending (best practice)
dataLayer.push({ ecommerce: null });
dataLayer.push({
  'event': 'view_item',
  'ecommerce': {
    // ...
  }
});
```

---

## Conversions Setup （日本語訳：変換の設定）

### Creating Conversions （日本語訳：コンバージョンの作成）

1. **Collect the event** - Ensure event is firing in GA4 （日本語訳：**イベントを収集** - GA4 でイベントが発生していることを確認します）
2. **Mark as conversion** - Admin > Events > Mark as conversion （日本語訳：**コンバージョンとしてマーク** - [管理] > [イベント] > [コンバージョンとしてマーク]）
3. **Set counting method**: （日本語訳：**カウント方法を設定**:）
   - Once per session (leads, signups) （日本語訳：セッションごとに 1 回 (リード、サインアップ)）
   - Every event (purchases) （日本語訳：イベントごと（購入時））
4. **Import to Google Ads** - For conversion-optimized bidding （日本語訳：**Google 広告にインポート** - コンバージョン最適化入札の場合）

### Conversion Values （日本語訳：コンバージョン値）

```javascript
// Event with conversion value
gtag('event', 'purchase', {
  'value': 99.99,
  'currency': 'USD'
});
```

Or set default value in GA4 Admin when marking conversion. （日本語訳：または、コンバージョンをマークするときに GA4 Admin でデフォルト値を設定します。）

---

## Custom Dimensions and Metrics （日本語訳：カスタムのディメンションと指標）

### When to Use （日本語訳：いつ使用するか）

**Custom dimensions:** （日本語訳：**カスタム寸法:**）
- Properties you want to segment/filter by （日本語訳：セグメント化/フィルタリングするプロパティ）
- User attributes (plan type, industry) （日本語訳：ユーザー属性（プランタイプ、業種））
- Content attributes (author, category) （日本語訳：コンテンツの属性 (作成者、カテゴリ)）

**Custom metrics:** （日本語訳：Error 500 (Server Error)!!1500.That’s an error.There was an error. Please try again later.That’s all we know.）
- Numeric values to aggregate （日本語訳：集計する数値）
- Scores, counts, durations （日本語訳：スコア、カウント、継続時間）

### Setup Steps （日本語訳：Error 500 (Server Error)!!1500.That’s an error.There was an error. Please try again later.That’s all we know.）

1. Admin > Data display > Custom definitions （日本語訳：管理 > データ表示 > カスタム定義）
2. Create dimension or metric （日本語訳：ディメンションまたは指標を作成する）
3. Choose scope: （日本語訳：範囲を選択してください:）
   - **Event**: Per event (content_type) （日本語訳：**イベント**: イベントごと (content_type)）
   - **User**: Per user (account_type) （日本語訳：**ユーザー**: ユーザーごと (account_type)）
   - **Item**: Per product (product_category) （日本語訳：**アイテム**: 製品ごと (product_category)）
4. Enter parameter name (must match event parameter) （日本語訳：パラメータ名を入力してください (イベントパラメータと一致する必要があります)）

### Examples （日本語訳：例）

| Dimension（日本語訳：寸法） | Scope（日本語訳：範囲） | Parameter（日本語訳：パラメータ） | Description（日本語訳：説明） |
|-----------|-------|-----------|-------------|
| User Type（日本語訳：ユーザータイプ） | User（日本語訳：ユーザー） | user_type（日本語訳：ユーザータイプ） | Free, trial, paid（日本語訳：無料、トライアル、有料） |
| Content Author（日本語訳：コンテンツ作成者） | Event（日本語訳：イベント） | author（日本語訳：著者） | Blog post author（日本語訳：ブログ投稿の著者） |
| Product Category（日本語訳：製品カテゴリー） | Item（日本語訳：アイテム） | item_category（日本語訳：アイテムカテゴリー） | E-commerce category（日本語訳：Eコマースカテゴリー） |

---

## Audiences （日本語訳：観客）

### Creating Audiences （日本語訳：視聴者の作成）

Admin > Data display > Audiences （日本語訳：管理者 > データ表示 > オーディエンス）

**Use cases:** （日本語訳：**使用例:**）
- Remarketing audiences (export to Ads) （日本語訳：リマーケティング オーディエンス (広告へのエクスポート)）
- Segment analysis （日本語訳：セグメント分析）
- Trigger-based events （日本語訳：トリガーベースのイベント）

### Audience Examples （日本語訳：対象読者の例）

**High-intent visitors:** （日本語訳：**関心の高い訪問者:**）
- Viewed pricing page （日本語訳：料金ページを閲覧しました）
- Did not convert （日本語訳：変換されませんでした）
- In last 7 days （日本語訳：過去 7 日間に）

**Engaged users:** （日本語訳：**熱心なユーザー:**）
- 3+ sessions （日本語訳：3セッション以上）
- Or 5+ minutes total engagement （日本語訳：または合計 5 分以上のエンゲージメント）

**Purchasers:** （日本語訳：**購入者:**）
- Purchase event （日本語訳：購入イベント）
- For exclusion or lookalike （日本語訳：除外または類似のため）

---

## Debugging （日本語訳：デバッグ）

### DebugView （日本語訳：デバッグビュー）

Enable with: （日本語訳：以下で有効にします:）
- URL parameter: `?debug_mode=true` （日本語訳：URL パラメータ: `?debug_mode=true`）
- Chrome extension: GA Debugger （日本語訳：Chrome 拡張機能: GA デバッガー）
- gtag: `'debug_mode': true` in config （日本語訳：gtag: 構成内の `'debug_mode': true`）

View at: Reports > Configure > DebugView （日本語訳：表示場所: [レポート] > [構成] > [DebugView]）

### Real-Time Reports （日本語訳：リアルタイムレポート）

Check events within 30 minutes: （日本語訳：30 分以内のイベントを確認します。）
Reports > Real-time （日本語訳：レポート > リアルタイム）

### Common Issues （日本語訳：よくある問題）

**Events not appearing:** （日本語訳：**イベントが表示されない:**）
- Check DebugView first （日本語訳：まず DebugView を確認してください）
- Verify gtag/GTM firing （日本語訳：gtag/GTM の起動を確認する）
- Check filter exclusions （日本語訳：フィルターの除外を確認する）

**Parameter values missing:** （日本語訳：**パラメータ値が欠落しています:**）
- Custom dimension not created （日本語訳：カスタム ディメンションが作成されていません）
- Parameter name mismatch （日本語訳：パラメータ名が一致しません）
- Data still processing (24-48 hrs) （日本語訳：データはまだ処理中 (24 ～ 48 時間)）

**Conversions not recording:** （日本語訳：**コンバージョンが記録されない:**）
- Event not marked as conversion （日本語訳：イベントがコンバージョンとしてマークされていない）
- Event name doesn't match （日本語訳：イベント名が一致しません）
- Counting method (once vs. every) （日本語訳：カウント方法 (1 回 vs. 毎回)）

---

## Data Quality （日本語訳：データ品質）

### Filters （日本語訳：フィルター）

Admin > Data streams > [Stream] > Configure tag settings > Define internal traffic （日本語訳：管理 > データ ストリーム > [ストリーム] > タグ設定の構成 > 内部トラフィックの定義）

**Exclude:** （日本語訳：**除外するもの:**）
- Internal IP addresses （日本語訳：内部IPアドレス）
- Developer traffic （日本語訳：開発者のトラフィック）
- Testing environments （日本語訳：テスト環境）

### Cross-Domain Tracking （日本語訳：クロスドメイントラッキング）

For multiple domains sharing analytics: （日本語訳：複数のドメインで分析を共有する場合:）

1. Admin > Data streams > [Stream] > Configure tag settings （日本語訳：管理者 > データ ストリーム > [ストリーム] > タグ設定の構成）
2. Configure your domains （日本語訳：ドメインを構成する）
3. List all domains that should share sessions （日本語訳：セッションを共有する必要があるすべてのドメインをリストします。）

### Session Settings （日本語訳：セッション設定）

Admin > Data streams > [Stream] > Configure tag settings （日本語訳：管理者 > データ ストリーム > [ストリーム] > タグ設定の構成）

- Session timeout (default 30 min) （日本語訳：セッションタイムアウト (デフォルトは 30 分)）
- Engaged session duration (10 sec default) （日本語訳：関与したセッションの継続時間 (デフォルトは 10 秒)）

---

## Integration with Google Ads （日本語訳：Google 広告との統合）

### Linking （日本語訳：リンクする）

1. Admin > Product links > Google Ads links （日本語訳：管理者 > 商品リンク > Google 広告リンク）
2. Enable auto-tagging in Google Ads （日本語訳：Google 広告で自動タグ設定を有効にする）
3. Import conversions in Google Ads （日本語訳：Google 広告にコンバージョンをインポートする）

### Audience Export （日本語訳：オーディエンスのエクスポート）

Audiences created in GA4 can be used in Google Ads for: （日本語訳：GA4 で作成されたオーディエンスは、Google 広告で次の用途に使用できます。）
- Remarketing campaigns （日本語訳：リマーケティング キャンペーン）
- Customer match （日本語訳：カスタマーマッチ）
- Similar audiences （日本語訳：同様の視聴者）
