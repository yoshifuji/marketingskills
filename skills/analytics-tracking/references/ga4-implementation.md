# GA4 Implementation Reference （GA4 実装リファレンス）

Detailed implementation guide for Google Analytics 4. （Google Analytics 4 の詳細な実装ガイド。）

## Configuration （構成）

### Data Streams （データストリーム）

- One stream per platform (web, iOS, Android) （プラットフォームごとに 1 つのストリーム (Web、iOS、Android)）
- Enable enhanced measurement for automatic tracking （自動追跡のための拡張測定を有効にする）
- Configure data retention (2 months default, 14 months max) （データ保持の構成 (デフォルトは 2 か月、最大 14 か月)）
- Enable Google Signals (for cross-device, if consented) （Google シグナルを有効にする (同意されている場合、クロスデバイス用)）

### Enhanced Measurement Events (Automatic) （拡張測定イベント (自動)）

| Event（イベント） | Description（説明） | Configuration（構成） |
|-------|-------------|---------------|
| page_view（ページビュー） | Page loads（ページの読み込み） | Automatic（自動） |
| scroll（スクロール） | 90% scroll depth（スクロール深度 90%） | Toggle on/off（オン/オフを切り替えます） |
| outbound_click（outbound_click） | Click to external domain（クリックして外部ドメインへ） | Automatic（自動） |
| site_search（サイト検索） | Search query used（使用された検索クエリ） | Configure parameter（パラメータの設定） |
| video_engagement（ビデオエンゲージメント） | YouTube video plays（YouTube ビデオの再生） | Toggle on/off（オン/オフを切り替えます） |
| file_download（ファイル_ダウンロード） | PDF, docs, etc.（PDF、ドキュメントなど） | Configurable extensions（構成可能な拡張機能） |

### Recommended Events （おすすめイベント）

Use Google's predefined events when possible for enhanced reporting: （レポートを強化するには、可能な場合は Google の事前定義イベントを使用します。）

**All properties:** （**すべてのプロパティ:**）
- login, sign_up （ログイン、サインアップ）
- share （共有）
- search （検索）

**E-commerce:** （**電子商取引:**）
- view_item, view_item_list （view_item、view_item_list）
- add_to_cart, remove_from_cart （カートに追加、カートから削除）
- begin_checkout （チェックアウトの開始）
- add_payment_info （add_payment_info）
- purchase, refund （購入、返金）

**Games:** （**ゲーム:**）
- level_up, unlock_achievement （レベルアップ、アンロックアチーブメント）
- post_score, spend_virtual_currency （post_score、spend_virtual_currency）

Reference: https://support.google.com/analytics/answer/9267735 （参照: https://support.google.com/analytics/answer/9267735）

---

## Custom Events （カスタムイベント）

### gtag.js Implementation （gtag.jsの実装）

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

### Google Tag Manager (dataLayer) （Google タグマネージャー (dataLayer)）

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

## Conversions Setup （変換の設定）

### Creating Conversions （コンバージョンの作成）

1. **Collect the event** - Ensure event is firing in GA4 （**イベントを収集** - GA4 でイベントが発生していることを確認します）
2. **Mark as conversion** - Admin > Events > Mark as conversion （**コンバージョンとしてマーク** - [管理] > [イベント] > [コンバージョンとしてマーク]）
3. **Set counting method**: （**カウント方法を設定**:）
   - Once per session (leads, signups) （セッションごとに 1 回 (リード、サインアップ)）
   - Every event (purchases) （イベントごと（購入時））
4. **Import to Google Ads** - For conversion-optimized bidding （**Google 広告にインポート** - コンバージョン最適化入札の場合）

### Conversion Values （コンバージョン値）

```javascript
// Event with conversion value
gtag('event', 'purchase', {
  'value': 99.99,
  'currency': 'USD'
});
```

Or set default value in GA4 Admin when marking conversion. （または、コンバージョンをマークするときに GA4 Admin でデフォルト値を設定します。）

---

## Custom Dimensions and Metrics （カスタムのディメンションと指標）

### When to Use （いつ使用するか）

**Custom dimensions:** （**カスタム寸法:**）
- Properties you want to segment/filter by （セグメント化/フィルタリングするプロパティ）
- User attributes (plan type, industry) （ユーザー属性（プランタイプ、業種））
- Content attributes (author, category) （コンテンツの属性 (作成者、カテゴリ)）

**Custom metrics:** （Error 500 (Server Error)!!1500.That’s an error.There was an error. Please try again later.That’s all we know.）
- Numeric values to aggregate （集計する数値）
- Scores, counts, durations （スコア、カウント、継続時間）

### Setup Steps （Error 500 (Server Error)!!1500.That’s an error.There was an error. Please try again later.That’s all we know.）

1. Admin > Data display > Custom definitions （管理 > データ表示 > カスタム定義）
2. Create dimension or metric （ディメンションまたは指標を作成する）
3. Choose scope: （範囲を選択してください:）
   - **Event**: Per event (content_type) （**イベント**: イベントごと (content_type)）
   - **User**: Per user (account_type) （**ユーザー**: ユーザーごと (account_type)）
   - **Item**: Per product (product_category) （**アイテム**: 製品ごと (product_category)）
4. Enter parameter name (must match event parameter) （パラメータ名を入力してください (イベントパラメータと一致する必要があります)）

### Examples （例）

| Dimension（寸法） | Scope（範囲） | Parameter（パラメータ） | Description（説明） |
|-----------|-------|-----------|-------------|
| User Type（ユーザータイプ） | User（ユーザー） | user_type（ユーザータイプ） | Free, trial, paid（無料、トライアル、有料） |
| Content Author（コンテンツ作成者） | Event（イベント） | author（著者） | Blog post author（ブログ投稿の著者） |
| Product Category（製品カテゴリー） | Item（アイテム） | item_category（アイテムカテゴリー） | E-commerce category（Eコマースカテゴリー） |

---

## Audiences （観客）

### Creating Audiences （視聴者の作成）

Admin > Data display > Audiences （管理者 > データ表示 > オーディエンス）

**Use cases:** （**使用例:**）
- Remarketing audiences (export to Ads) （リマーケティング オーディエンス (広告へのエクスポート)）
- Segment analysis （セグメント分析）
- Trigger-based events （トリガーベースのイベント）

### Audience Examples （対象読者の例）

**High-intent visitors:** （**関心の高い訪問者:**）
- Viewed pricing page （料金ページを閲覧しました）
- Did not convert （変換されませんでした）
- In last 7 days （過去 7 日間に）

**Engaged users:** （**熱心なユーザー:**）
- 3+ sessions （3セッション以上）
- Or 5+ minutes total engagement （または合計 5 分以上のエンゲージメント）

**Purchasers:** （**購入者:**）
- Purchase event （購入イベント）
- For exclusion or lookalike （除外または類似のため）

---

## Debugging （デバッグ）

### DebugView （デバッグビュー）

Enable with: （以下で有効にします:）
- URL parameter: `?debug_mode=true` （URL パラメータ: `?debug_mode=true`）
- Chrome extension: GA Debugger （Chrome 拡張機能: GA デバッガー）
- gtag: `'debug_mode': true` in config （gtag: 構成内の `'debug_mode': true`）

View at: Reports > Configure > DebugView （表示場所: [レポート] > [構成] > [DebugView]）

### Real-Time Reports （リアルタイムレポート）

Check events within 30 minutes: （30 分以内のイベントを確認します。）
Reports > Real-time （レポート > リアルタイム）

### Common Issues （よくある問題）

**Events not appearing:** （**イベントが表示されない:**）
- Check DebugView first （まず DebugView を確認してください）
- Verify gtag/GTM firing （gtag/GTM の起動を確認する）
- Check filter exclusions （フィルターの除外を確認する）

**Parameter values missing:** （**パラメータ値が欠落しています:**）
- Custom dimension not created （カスタム ディメンションが作成されていません）
- Parameter name mismatch （パラメータ名が一致しません）
- Data still processing (24-48 hrs) （データはまだ処理中 (24 ～ 48 時間)）

**Conversions not recording:** （**コンバージョンが記録されない:**）
- Event not marked as conversion （イベントがコンバージョンとしてマークされていない）
- Event name doesn't match （イベント名が一致しません）
- Counting method (once vs. every) （カウント方法 (1 回 vs. 毎回)）

---

## Data Quality （データ品質）

### Filters （フィルター）

Admin > Data streams > [Stream] > Configure tag settings > Define internal traffic （管理 > データ ストリーム > [ストリーム] > タグ設定の構成 > 内部トラフィックの定義）

**Exclude:** （**除外するもの:**）
- Internal IP addresses （内部IPアドレス）
- Developer traffic （開発者のトラフィック）
- Testing environments （テスト環境）

### Cross-Domain Tracking （クロスドメイントラッキング）

For multiple domains sharing analytics: （複数のドメインで分析を共有する場合:）

1. Admin > Data streams > [Stream] > Configure tag settings （管理者 > データ ストリーム > [ストリーム] > タグ設定の構成）
2. Configure your domains （ドメインを構成する）
3. List all domains that should share sessions （セッションを共有する必要があるすべてのドメインをリストします。）

### Session Settings （セッション設定）

Admin > Data streams > [Stream] > Configure tag settings （管理者 > データ ストリーム > [ストリーム] > タグ設定の構成）

- Session timeout (default 30 min) （セッションタイムアウト (デフォルトは 30 分)）
- Engaged session duration (10 sec default) （関与したセッションの継続時間 (デフォルトは 10 秒)）

---

## Integration with Google Ads （Google 広告との統合）

### Linking （リンクする）

1. Admin > Product links > Google Ads links （管理者 > 商品リンク > Google 広告リンク）
2. Enable auto-tagging in Google Ads （Google 広告で自動タグ設定を有効にする）
3. Import conversions in Google Ads （Google 広告にコンバージョンをインポートする）

### Audience Export （オーディエンスのエクスポート）

Audiences created in GA4 can be used in Google Ads for: （GA4 で作成されたオーディエンスは、Google 広告で次の用途に使用できます。）
- Remarketing campaigns （リマーケティング キャンペーン）
- Customer match （カスタマーマッチ）
- Similar audiences （同様の視聴者）
