# Google Tag Manager Implementation Reference （日本語訳：Google タグマネージャー実装リファレンス）

Detailed guide for implementing tracking via Google Tag Manager. （日本語訳：Google タグ マネージャーを介してトラッキングを実装するための詳細なガイド。）

## Container Structure （日本語訳：コンテナの構造）

### Tags （日本語訳：タグ）

Tags are code snippets that execute when triggered. （日本語訳：タグは、トリガーされたときに実行されるコード スニペットです。）

**Common tag types:** （日本語訳：**一般的なタグの種類:**）
- GA4 Configuration (base setup) （日本語訳：GA4 構成 (基本セットアップ)）
- GA4 Event (custom events) （日本語訳：GA4 イベント (カスタム イベント)）
- Google Ads Conversion （日本語訳：Google 広告のコンバージョン）
- Facebook Pixel （日本語訳：フェイスブックピクセル）
- LinkedIn Insight Tag （日本語訳：LinkedIn インサイト タグ）
- Custom HTML (for other pixels) （日本語訳：カスタム HTML (他のピクセル用)）

### Triggers （日本語訳：トリガー）

Triggers define when tags fire. （日本語訳：トリガーはタグがいつ起動されるかを定義します。）

**Built-in triggers:** （日本語訳：**組み込みトリガー:**）
- Page View: All Pages, DOM Ready, Window Loaded （日本語訳：ページビュー: すべてのページ、DOM 対応、ウィンドウロード済み）
- Click: All Elements, Just Links （日本語訳：クリック: すべての要素、リンクのみ）
- Form Submission （日本語訳：フォームの送信）
- Scroll Depth （日本語訳：スクロールの深さ）
- Timer （日本語訳：タイマー）
- Element Visibility （日本語訳：要素の可視性）

**Custom triggers:** （日本語訳：**カスタム トリガー:**）
- Custom Event (from dataLayer) （日本語訳：カスタム イベント (dataLayer から)）
- Trigger Groups (multiple conditions) （日本語訳：トリガーグループ（複数の条件））

### Variables （日本語訳：変数）

Variables capture dynamic values. （日本語訳：変数は動的な値を取得します。）

**Built-in (enable as needed):** （日本語訳：**組み込み (必要に応じて有効化):**）
- Click Text, Click URL, Click ID, Click Classes （日本語訳：「テキスト」をクリック、「URL」をクリック、「ID」をクリック、「クラス」をクリック）
- Page Path, Page URL, Page Hostname （日本語訳：ページパス、ページURL、ページホスト名）
- Referrer （日本語訳：参照元）
- Form Element, Form ID （日本語訳：フォーム要素、フォームID）

**User-defined:** （日本語訳：**ユーザー定義:**）
- Data Layer variables （日本語訳：データ層変数）
- JavaScript variables （日本語訳：JavaScript 変数）
- Lookup tables （日本語訳：ルックアップテーブル）
- RegEx tables （日本語訳：正規表現テーブル）
- Constants （日本語訳：定数）

---

## Naming Conventions （日本語訳：命名規則）

### Recommended Format （日本語訳：推奨フォーマット）

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

## Data Layer Patterns （日本語訳：データ層パターン）

### Basic Structure （日本語訳：基本構造）

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

### Page Load Data （日本語訳：ページロードデータ）

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

### Form Submission （日本語訳：フォームの送信）

```javascript
document.querySelector('#contact-form').addEventListener('submit', function() {
  dataLayer.push({
    'event': 'form_submitted',
    'formName': 'contact',
    'formLocation': 'footer'
  });
});
```

### Button Click （日本語訳：ボタンクリック）

```javascript
document.querySelector('.cta-button').addEventListener('click', function() {
  dataLayer.push({
    'event': 'cta_clicked',
    'ctaText': this.innerText,
    'ctaLocation': 'hero'
  });
});
```

### E-commerce Events （日本語訳：Eコマースイベント）

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

## Common Tag Configurations （日本語訳：一般的なタグ構成）

### GA4 Configuration Tag （日本語訳：GA4 構成タグ）

**Tag Type:** Google Analytics: GA4 Configuration （日本語訳：**タグ タイプ:** Google アナリティクス: GA4 構成）

**Settings:** （日本語訳：**設定：**）
- Measurement ID: G-XXXXXXXX （日本語訳：測定ID：G-XXXXXXXX）
- Send page view: Checked (for pageviews) （日本語訳：ページビューの送信: チェック済み (ページビューの場合)）
- User Properties: Add any user-level dimensions （日本語訳：ユーザー プロパティ: ユーザーレベルのディメンションを追加します。）

**Trigger:** All Pages （日本語訳：**トリガー:** すべてのページ）

### GA4 Event Tag （日本語訳：GA4 イベントタグ）

**Tag Type:** Google Analytics: GA4 Event （日本語訳：**タグ タイプ:** Google アナリティクス: GA4 イベント）

**Settings:** （日本語訳：**設定：**）
- Configuration Tag: Select your config tag （日本語訳：構成タグ: 構成タグを選択します）
- Event Name: {{DL - event_name}} or hardcode （日本語訳：イベント名: {{DL -event_name}} またはハードコード）
- Event Parameters: Add parameters from dataLayer （日本語訳：イベントパラメータ: dataLayerからパラメータを追加）

**Trigger:** Custom Event with event name match （日本語訳：**トリガー:** イベント名が一致するカスタム イベント）

### Facebook Pixel - Base （日本語訳：Facebook ピクセル - ベース）

**Tag Type:** Custom HTML （日本語訳：**タグの種類:** カスタム HTML）

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

**Trigger:** All Pages （日本語訳：**トリガー:** すべてのページ）

### Facebook Pixel - Event （日本語訳：Facebook ピクセル - イベント）

**Tag Type:** Custom HTML （日本語訳：**タグの種類:** カスタム HTML）

```html
<script>
  fbq('track', 'Lead', {
    content_name: '{{DL - form_name}}'
  });
</script>
```

**Trigger:** Custom Event - form_submitted （日本語訳：**トリガー:** カスタム イベント - form_submitted）

---

## Preview and Debug （日本語訳：プレビューとデバッグ）

### Preview Mode （日本語訳：プレビューモード）

1. Click "Preview" in GTM （日本語訳：GTMの「プレビュー」をクリックします）
2. Enter site URL （日本語訳：サイトのURLを入力してください）
3. GTM debug panel opens at bottom （日本語訳：GTM デバッグ パネルが下部に開きます）

**What to check:** （日本語訳：**確認事項:**）
- Tags fired on this event （日本語訳：このイベントで起動されたタグ）
- Tags not fired (and why) （日本語訳：タグが起動されない (およびその理由)）
- Variables and their values （日本語訳：変数とその値）
- Data layer contents （日本語訳：データ層の内容）

### Debug Tips （日本語訳：デバッグのヒント）

**Tag not firing:** （日本語訳：**タグが起動しない:**）
- Check trigger conditions （日本語訳：トリガー条件を確認する）
- Verify data layer push （日本語訳：データ層のプッシュを確認する）
- Check tag sequencing （日本語訳：タグのシーケンスを確認する）

**Wrong variable value:** （日本語訳：**変数値が間違っています:**）
- Check data layer structure （日本語訳：データ層構造を確認する）
- Verify variable path (nested objects) （日本語訳：変数パスの検証 (ネストされたオブジェクト)）
- Check timing (data may not exist yet) （日本語訳：タイミングを確認（データがまだ存在していない可能性があります））

**Multiple firings:** （日本語訳：**複数回の発射:**）
- Check trigger uniqueness （日本語訳：トリガーの一意性をチェックする）
- Look for duplicate tags （日本語訳：重複したタグを探す）
- Check tag firing options （日本語訳：タグ起動オプションを確認する）

---

## Workspaces and Versioning （日本語訳：ワークスペースとバージョン管理）

### Workspaces （日本語訳：ワークスペース）

Use workspaces for team collaboration: （日本語訳：チームコラボレーションにワークスペースを使用します。）
- Default workspace for production （日本語訳：実稼働用のデフォルトのワークスペース）
- Separate workspaces for large changes （日本語訳：大規模な変更には個別のワークスペースを使用する）
- Merge when ready （日本語訳：準備ができたらマージ）

### Version Management （日本語訳：バージョン管理）

**Best practices:** （日本語訳：**ベストプラクティス:**）
- Name every version descriptively （日本語訳：各バージョンにわかりやすい名前を付ける）
- Add notes explaining changes （日本語訳：変更点を説明するメモを追加する）
- Review changes before publish （日本語訳：公開する前に変更を確認する）
- Keep production version noted （日本語訳：製品バージョンをメモしておきます）

**Version notes example:** （日本語訳：**バージョンメモの例:**）
```
v15: Added purchase conversion tracking
- New tag: GA4 - Event - Purchase
- New trigger: Custom Event - purchase
- New variables: DL - transaction_id, DL - value
- Tested: Chrome, Safari, Mobile
```

---

## Consent Management （日本語訳：同意管理）

### Consent Mode Integration （日本語訳：同意モードの統合）

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

### GTM Consent Overview （日本語訳：GTM 同意の概要）

1. Enable Consent Overview in Admin （日本語訳：管理画面で同意概要を有効にする）
2. Configure consent for each tag （日本語訳：タグごとに同意を構成する）
3. Tags respect consent state automatically （日本語訳：タグは自動的に同意状態を尊重します）

---

## Advanced Patterns （日本語訳：高度なパターン）

### Tag Sequencing （日本語訳：タグのシーケンス）

**Setup tags to fire in order:** （日本語訳：**タグを順番に起動するように設定します:**）
Tag Configuration > Advanced Settings > Tag Sequencing （日本語訳：タグの設定 > 詳細設定 > タグの順序付け）

**Use cases:** （日本語訳：**使用例:**）
- Config tag before event tags （日本語訳：イベントタグの前の設定タグ）
- Pixel initialization before tracking （日本語訳：追跡前のピクセルの初期化）
- Cleanup after conversion （日本語訳：変換後のクリーンアップ）

### Exception Handling （日本語訳：例外処理）

**Trigger exceptions** - Prevent tag from firing: （日本語訳：**例外のトリガー** - タグの起動を防止します。）
- Exclude certain pages （日本語訳：特定のページを除外する）
- Exclude internal traffic （日本語訳：内部トラフィックを除外する）
- Exclude during testing （日本語訳：テスト中に除外する）

### Custom JavaScript Variables （日本語訳：カスタム JavaScript 変数）

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
