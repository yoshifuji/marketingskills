# Google Tag Manager Implementation Reference （Google タグマネージャー実装リファレンス）

Detailed guide for implementing tracking via Google Tag Manager. （Google タグ マネージャーを介してトラッキングを実装するための詳細なガイド。）

## Container Structure （コンテナの構造）

### Tags （タグ）

Tags are code snippets that execute when triggered. （タグは、トリガーされたときに実行されるコード スニペットです。）

**Common tag types:** （**一般的なタグの種類:**）
- GA4 Configuration (base setup) （GA4 構成 (基本セットアップ)）
- GA4 Event (custom events) （GA4 イベント (カスタム イベント)）
- Google Ads Conversion （Google 広告のコンバージョン）
- Facebook Pixel （フェイスブックピクセル）
- LinkedIn Insight Tag （LinkedIn インサイト タグ）
- Custom HTML (for other pixels) （カスタム HTML (他のピクセル用)）

### Triggers （トリガー）

Triggers define when tags fire. （トリガーはタグがいつ起動されるかを定義します。）

**Built-in triggers:** （**組み込みトリガー:**）
- Page View: All Pages, DOM Ready, Window Loaded （ページビュー: すべてのページ、DOM 対応、ウィンドウロード済み）
- Click: All Elements, Just Links （クリック: すべての要素、リンクのみ）
- Form Submission （フォームの送信）
- Scroll Depth （スクロールの深さ）
- Timer （タイマー）
- Element Visibility （要素の可視性）

**Custom triggers:** （**カスタム トリガー:**）
- Custom Event (from dataLayer) （カスタム イベント (dataLayer から)）
- Trigger Groups (multiple conditions) （トリガーグループ（複数の条件））

### Variables （変数）

Variables capture dynamic values. （変数は動的な値を取得します。）

**Built-in (enable as needed):** （**組み込み (必要に応じて有効化):**）
- Click Text, Click URL, Click ID, Click Classes （「テキスト」をクリック、「URL」をクリック、「ID」をクリック、「クラス」をクリック）
- Page Path, Page URL, Page Hostname （ページパス、ページURL、ページホスト名）
- Referrer （参照元）
- Form Element, Form ID （フォーム要素、フォームID）

**User-defined:** （**ユーザー定義:**）
- Data Layer variables （データ層変数）
- JavaScript variables （JavaScript 変数）
- Lookup tables （ルックアップテーブル）
- RegEx tables （正規表現テーブル）
- Constants （定数）

---

## Naming Conventions （命名規則）

### Recommended Format （推奨フォーマット）

```
[Type] - [Description] - [Detail]

Tags:
GA4 - Event - Signup Completed
GA4 - Config - Base Configuration
FB - Pixel - Page View
HTML - LiveChat Widget

Triggers:
Click - CTA Button
Submit - Contact Form
View - Pricing Page
Custom - signup_completed

Variables:
DL - user_id
JS - Current Timestamp
LT - Campaign Source Map
```

---

## Data Layer Patterns （データ層パターン）

### Basic Structure （基本構造）

```javascript
// Initialize (in <head> before GTM)
window.dataLayer = window.dataLayer || [];

// Push event
dataLayer.push({
  'event': 'event_name',
  'property1': 'value1',
  'property2': 'value2'
});
```

### Page Load Data （ページロードデータ）

```javascript
// Set on page load (before GTM container)
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  'pageType': 'product',
  'contentGroup': 'products',
  'user': {
    'loggedIn': true,
    'userId': '12345',
    'userType': 'premium'
  }
});
```

### Form Submission （フォームの送信）

```javascript
document.querySelector('#contact-form').addEventListener('submit', function() {
  dataLayer.push({
    'event': 'form_submitted',
    'formName': 'contact',
    'formLocation': 'footer'
  });
});
```

### Button Click （ボタンクリック）

```javascript
document.querySelector('.cta-button').addEventListener('click', function() {
  dataLayer.push({
    'event': 'cta_clicked',
    'ctaText': this.innerText,
    'ctaLocation': 'hero'
  });
});
```

### E-commerce Events （Eコマースイベント）

```javascript
// Product view
dataLayer.push({ ecommerce: null }); // Clear previous
dataLayer.push({
  'event': 'view_item',
  'ecommerce': {
    'items': [{
      'item_id': 'SKU123',
      'item_name': 'Product Name',
      'price': 99.99,
      'item_category': 'Category',
      'quantity': 1
    }]
  }
});

// Add to cart
dataLayer.push({ ecommerce: null });
dataLayer.push({
  'event': 'add_to_cart',
  'ecommerce': {
    'items': [{
      'item_id': 'SKU123',
      'item_name': 'Product Name',
      'price': 99.99,
      'quantity': 1
    }]
  }
});

// Purchase
dataLayer.push({ ecommerce: null });
dataLayer.push({
  'event': 'purchase',
  'ecommerce': {
    'transaction_id': 'T12345',
    'value': 99.99,
    'currency': 'USD',
    'tax': 5.00,
    'shipping': 10.00,
    'items': [{
      'item_id': 'SKU123',
      'item_name': 'Product Name',
      'price': 99.99,
      'quantity': 1
    }]
  }
});
```

---

## Common Tag Configurations （一般的なタグ構成）

### GA4 Configuration Tag （GA4 構成タグ）

**Tag Type:** Google Analytics: GA4 Configuration （**タグ タイプ:** Google アナリティクス: GA4 構成）

**Settings:** （**設定：**）
- Measurement ID: G-XXXXXXXX （測定ID：G-XXXXXXXX）
- Send page view: Checked (for pageviews) （ページビューの送信: チェック済み (ページビューの場合)）
- User Properties: Add any user-level dimensions （ユーザー プロパティ: ユーザーレベルのディメンションを追加します。）

**Trigger:** All Pages （**トリガー:** すべてのページ）

### GA4 Event Tag （GA4 イベントタグ）

**Tag Type:** Google Analytics: GA4 Event （**タグ タイプ:** Google アナリティクス: GA4 イベント）

**Settings:** （**設定：**）
- Configuration Tag: Select your config tag （構成タグ: 構成タグを選択します）
- Event Name: {{DL - event_name}} or hardcode （イベント名: {{DL -event_name}} またはハードコード）
- Event Parameters: Add parameters from dataLayer （イベントパラメータ: dataLayerからパラメータを追加）

**Trigger:** Custom Event with event name match （**トリガー:** イベント名が一致するカスタム イベント）

### Facebook Pixel - Base （Facebook ピクセル - ベース）

**Tag Type:** Custom HTML （**タグの種類:** カスタム HTML）

```html
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

**Trigger:** All Pages （**トリガー:** すべてのページ）

### Facebook Pixel - Event （Facebook ピクセル - イベント）

**Tag Type:** Custom HTML （**タグの種類:** カスタム HTML）

```html
<script>
  fbq('track', 'Lead', {
    content_name: '{{DL - form_name}}'
  });
</script>
```

**Trigger:** Custom Event - form_submitted （**トリガー:** カスタム イベント - form_submitted）

---

## Preview and Debug （プレビューとデバッグ）

### Preview Mode （プレビューモード）

1. Click "Preview" in GTM （GTMの「プレビュー」をクリックします）
2. Enter site URL （サイトのURLを入力してください）
3. GTM debug panel opens at bottom （GTM デバッグ パネルが下部に開きます）

**What to check:** （**確認事項:**）
- Tags fired on this event （このイベントで起動されたタグ）
- Tags not fired (and why) （タグが起動されない (およびその理由)）
- Variables and their values （変数とその値）
- Data layer contents （データ層の内容）

### Debug Tips （デバッグのヒント）

**Tag not firing:** （**タグが起動しない:**）
- Check trigger conditions （トリガー条件を確認する）
- Verify data layer push （データ層のプッシュを確認する）
- Check tag sequencing （タグのシーケンスを確認する）

**Wrong variable value:** （**変数値が間違っています:**）
- Check data layer structure （データ層構造を確認する）
- Verify variable path (nested objects) （変数パスの検証 (ネストされたオブジェクト)）
- Check timing (data may not exist yet) （タイミングを確認（データがまだ存在していない可能性があります））

**Multiple firings:** （**複数回の発射:**）
- Check trigger uniqueness （トリガーの一意性をチェックする）
- Look for duplicate tags （重複したタグを探す）
- Check tag firing options （タグ起動オプションを確認する）

---

## Workspaces and Versioning （ワークスペースとバージョン管理）

### Workspaces （ワークスペース）

Use workspaces for team collaboration: （チームコラボレーションにワークスペースを使用します。）
- Default workspace for production （実稼働用のデフォルトのワークスペース）
- Separate workspaces for large changes （大規模な変更には個別のワークスペースを使用する）
- Merge when ready （準備ができたらマージ）

### Version Management （バージョン管理）

**Best practices:** （**ベストプラクティス:**）
- Name every version descriptively （各バージョンにわかりやすい名前を付ける）
- Add notes explaining changes （変更点を説明するメモを追加する）
- Review changes before publish （公開する前に変更を確認する）
- Keep production version noted （製品バージョンをメモしておきます）

**Version notes example:** （**バージョンメモの例:**）
```
v15: Added purchase conversion tracking
- New tag: GA4 - Event - Purchase
- New trigger: Custom Event - purchase
- New variables: DL - transaction_id, DL - value
- Tested: Chrome, Safari, Mobile
```

---

## Consent Management （同意管理）

### Consent Mode Integration （同意モードの統合）

```javascript
// Default state (before consent)
gtag('consent', 'default', {
  'analytics_storage': 'denied',
  'ad_storage': 'denied'
});

// Update on consent
function grantConsent() {
  gtag('consent', 'update', {
    'analytics_storage': 'granted',
    'ad_storage': 'granted'
  });
}
```

### GTM Consent Overview （GTM 同意の概要）

1. Enable Consent Overview in Admin （管理画面で同意概要を有効にする）
2. Configure consent for each tag （タグごとに同意を構成する）
3. Tags respect consent state automatically （タグは自動的に同意状態を尊重します）

---

## Advanced Patterns （高度なパターン）

### Tag Sequencing （タグのシーケンス）

**Setup tags to fire in order:** （**タグを順番に起動するように設定します:**）
Tag Configuration > Advanced Settings > Tag Sequencing （タグの設定 > 詳細設定 > タグの順序付け）

**Use cases:** （**使用例:**）
- Config tag before event tags （イベントタグの前の設定タグ）
- Pixel initialization before tracking （追跡前のピクセルの初期化）
- Cleanup after conversion （変換後のクリーンアップ）

### Exception Handling （例外処理）

**Trigger exceptions** - Prevent tag from firing: （**例外のトリガー** - タグの起動を防止します。）
- Exclude certain pages （特定のページを除外する）
- Exclude internal traffic （内部トラフィックを除外する）
- Exclude during testing （テスト中に除外する）

### Custom JavaScript Variables （カスタム JavaScript 変数）

```javascript
// Get URL parameter
function() {
  var params = new URLSearchParams(window.location.search);
  return params.get('campaign') || '(not set)';
}

// Get cookie value
function() {
  var match = document.cookie.match('(^|;) ?user_id=([^;]*)(;|$)');
  return match ? match[2] : null;
}

// Get data from page
function() {
  var el = document.querySelector('.product-price');
  return el ? parseFloat(el.textContent.replace('$', '')) : 0;
}
```
