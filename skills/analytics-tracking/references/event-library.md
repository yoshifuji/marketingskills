# Event Library Reference （日本語訳：イベントライブラリリファレンス）

Comprehensive list of events to track by business type and context. （日本語訳：ビジネスの種類とコンテキストごとに追跡するイベントの包括的なリスト。）

## Marketing Site Events （日本語訳：マーケティングサイトのイベント）

### Navigation & Engagement （日本語訳：ナビゲーションとエンゲージメント）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| page_view（日本語訳：ページビュー） | Page loaded (enhanced)（日本語訳：ページが読み込まれました (拡張)） | page_title, page_location, content_group（日本語訳：page_title、page_location、content_group） |
| scroll_depth（日本語訳：スクロール深度） | User scrolled to threshold（日本語訳：ユーザーがしきい値までスクロールしました） | depth (25, 50, 75, 100)（日本語訳：深さ (25、50、75、100)） |
| outbound_link_clicked（日本語訳：outbound_link_clicked） | Click to external site（日本語訳：クリックすると外部サイトへ） | link_url, link_text（日本語訳：リンクURL、リンクテキスト） |
| internal_link_clicked（日本語訳：Internal_link_clicked） | Click within site（日本語訳：サイト内をクリック） | link_url, link_text, location（日本語訳：リンクURL、リンクテキスト、場所） |
| video_played（日本語訳：video_played） | Video started（日本語訳：ビデオが開始されました） | video_id, video_title, duration（日本語訳：video_id、video_title、再生時間） |
| video_completed（日本語訳：ビデオ_完了） | Video finished（日本語訳：ビデオが完成しました） | video_id, video_title, duration（日本語訳：video_id、video_title、再生時間） |

### CTA & Form Interactions （日本語訳：CTA とフォームのインタラクション）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| cta_clicked（日本語訳：cta_clicked） | Call to action clicked（日本語訳：行動喚起がクリックされました） | button_text, cta_location, page（日本語訳：button_text、cta_location、ページ） |
| form_started（日本語訳：フォーム_開始済み） | User began form（日本語訳：ユーザーがフォームを開始しました） | form_name, form_location（日本語訳：フォーム名、フォームの場所） |
| form_field_completed（日本語訳：フォームフィールド_完了） | Field filled（日本語訳：フィールドが入力されました） | form_name, field_name（日本語訳：フォーム名、フィールド名） |
| form_submitted（日本語訳：フォーム送信済み） | Form successfully sent（日本語訳：フォームは正常に送信されました） | form_name, form_location（日本語訳：フォーム名、フォームの場所） |
| form_error（日本語訳：フォームエラー） | Form validation failed（日本語訳：フォームの検証に失敗しました） | form_name, error_type（日本語訳：フォーム名、エラーの種類） |
| resource_downloaded（日本語訳：リソース_ダウンロード済み） | Asset downloaded（日本語訳：ダウンロードされたアセット） | resource_name, resource_type（日本語訳：リソース名、リソースタイプ） |

### Conversion Events （日本語訳：コンバージョンイベント）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| signup_started（日本語訳：サインアップ_開始済み） | Initiated signup（日本語訳：サインアップを開始しました） | source, page（日本語訳：ソース、ページ） |
| signup_completed（日本語訳：サインアップ_完了） | Finished signup（日本語訳：サインアップが完了しました） | method, plan, source（日本語訳：方法、計画、ソース） |
| demo_requested（日本語訳：デモ要求済み） | Demo form submitted（日本語訳：デモフォームが送信されました） | company_size, industry（日本語訳：会社規模、業種） |
| contact_submitted（日本語訳：連絡先_送信済み） | Contact form sent（日本語訳：お問い合わせフォームを送信しました） | inquiry_type（日本語訳：お問い合わせの種類） |
| newsletter_subscribed（日本語訳：ニュースレター_購読済み） | Email list signup（日本語訳：メールリストの登録） | source, list_name（日本語訳：ソース、リスト名） |
| trial_started（日本語訳：トライアル開始済み） | Free trial began（日本語訳：無料トライアルが始まりました） | plan, source（日本語訳：計画、ソース） |

---

## Product/App Events （日本語訳：製品/アプリのイベント）

### Onboarding （日本語訳：オンボーディング）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| signup_completed（日本語訳：サインアップ_完了） | Account created（日本語訳：アカウントが作成されました） | method, referral_source（日本語訳：メソッド、referral_source） |
| onboarding_started（日本語訳：オンボーディング_開始済み） | Began onboarding（日本語訳：オンボーディングを開始しました） | - |
| onboarding_step_completed（日本語訳：オンボーディング_ステップ_完了） | Step finished（日本語訳：ステップが完了しました） | step_number, step_name（日本語訳：ステップ番号、ステップ名） |
| onboarding_completed（日本語訳：オンボーディング_完了） | All steps done（日本語訳：すべての手順が完了しました） | steps_completed, time_to_complete（日本語訳：完了したステップ数、完了までの時間） |
| onboarding_skipped（日本語訳：オンボーディング_スキップされました） | User skipped onboarding（日本語訳：ユーザーがオンボーディングをスキップした） | step_skipped_at（日本語訳：step_skipped_at） |
| first_key_action_completed（日本語訳：first_key_action_completed） | Aha moment reached（日本語訳：ああ、その瞬間が来た） | action_type（日本語訳：アクションタイプ） |

### Core Usage （日本語訳：コアの使用法）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| session_started（日本語訳：セッション開始済み） | App session began（日本語訳：アプリセッションが開始されました） | session_number（日本語訳：セッション番号） |
| feature_used（日本語訳：使用されている機能） | Feature interaction（日本語訳：機能の相互作用） | feature_name, feature_category（日本語訳：機能名、機能カテゴリ） |
| action_completed（日本語訳：アクション_完了） | Core action done（日本語訳：主要なアクションが完了しました） | action_type, count（日本語訳：アクションタイプ、カウント） |
| content_created（日本語訳：コンテンツ作成済み） | User created content（日本語訳：ユーザーが作成したコンテンツ） | content_type（日本語訳：コンテンツタイプ） |
| content_edited（日本語訳：コンテンツ編集済み） | User modified content（日本語訳：ユーザーが変更したコンテンツ） | content_type（日本語訳：コンテンツタイプ） |
| content_deleted（日本語訳：コンテンツ_削除済み） | User removed content（日本語訳：ユーザーが削除したコンテンツ） | content_type（日本語訳：コンテンツタイプ） |
| search_performed（日本語訳：検索実行済み） | In-app search（日本語訳：アプリ内検索） | query, results_count（日本語訳：クエリ、結果数） |
| settings_changed（日本語訳：設定変更済み） | Settings modified（日本語訳：設定が変更されました） | setting_name, new_value（日本語訳：設定名、新しい値） |
| invite_sent（日本語訳：招待送信済み） | User invited others（日本語訳：ユーザーが他の人を招待しました） | invite_type, count（日本語訳：招待タイプ、数） |

### Errors & Support （日本語訳：エラーとサポート）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| error_occurred（日本語訳：エラーが発生しました） | Error experienced（日本語訳：エラーが発生しました） | error_type, error_message, page（日本語訳：エラータイプ、エラーメッセージ、ページ） |
| help_opened（日本語訳：ヘルプ_開いた） | Help accessed（日本語訳：アクセスしたヘルプ） | help_type, page（日本語訳：ヘルプ_タイプ、ページ） |
| support_contacted（日本語訳：サポート連絡済み） | Support request made（日本語訳：サポートリクエストが行われました） | contact_method, issue_type（日本語訳：連絡方法、問題の種類） |
| feedback_submitted（日本語訳：フィードバック_送信済み） | User feedback given（日本語訳：ユーザーからのフィードバック） | feedback_type, rating（日本語訳：フィードバックの種類、評価） |

---

## Monetization Events （日本語訳：収益化イベント）

### Pricing & Checkout （日本語訳：価格設定とチェックアウト）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| pricing_viewed（日本語訳：価格設定_閲覧済み） | Pricing page seen（日本語訳：価格ページが表示されました） | source（日本語訳：ソース） |
| plan_selected（日本語訳：プラン_選択済み） | Plan chosen（日本語訳：選択したプラン） | plan_name, billing_cycle（日本語訳：プラン名、請求サイクル） |
| checkout_started（日本語訳：チェックアウト開始済み） | Began checkout（日本語訳：チェックアウトを開始しました） | plan, value（日本語訳：計画、価値観） |
| payment_info_entered（日本語訳：支払い情報が入力されました） | Payment submitted（日本語訳：支払いが完了しました） | payment_method（日本語訳：支払方法） |
| purchase_completed（日本語訳：購入_完了） | Purchase successful（日本語訳：購入が成功しました） | plan, value, currency, transaction_id（日本語訳：プラン、値、通貨、transaction_id） |
| purchase_failed（日本語訳：購入_失敗） | Purchase failed（日本語訳：購入に失敗しました） | error_reason, plan（日本語訳：エラーの理由、計画） |

### Subscription Management （日本語訳：サブスクリプション管理）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| trial_started（日本語訳：トライアル開始済み） | Trial began（日本語訳：裁判が始まりました） | plan, trial_length（日本語訳：プラン、トライアルの長さ） |
| trial_ended（日本語訳：トライアル終了） | Trial expired（日本語訳：トライアル期間が終了しました） | plan, converted (bool)（日本語訳：計画、変換済み (ブール値)） |
| subscription_upgraded（日本語訳：サブスクリプション_アップグレード済み） | Plan upgraded（日本語訳：プランがアップグレードされました） | from_plan, to_plan, value（日本語訳：from_plan、to_plan、値） |
| subscription_downgraded（日本語訳：サブスクリプション_ダウングレード） | Plan downgraded（日本語訳：プランがダウングレードされました） | from_plan, to_plan（日本語訳：from_plan、to_plan） |
| subscription_cancelled（日本語訳：サブスクリプション_キャンセル済み） | Cancelled（日本語訳：キャンセル） | plan, reason, tenure（日本語訳：計画、理由、在職期間） |
| subscription_renewed（日本語訳：サブスクリプション_更新済み） | Renewed（日本語訳：リニューアル） | plan, value（日本語訳：計画、価値観） |
| billing_updated（日本語訳：請求_更新済み） | Payment method changed（日本語訳：支払い方法が変更されました） | - |

---

## E-commerce Events （日本語訳：Eコマースイベント）

### Browsing （日本語訳：ブラウジング）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| product_viewed（日本語訳：製品_閲覧済み） | Product page viewed（日本語訳：製品ページを閲覧しました） | product_id, product_name, category, price（日本語訳：製品ID、製品名、カテゴリ、価格） |
| product_list_viewed（日本語訳：製品リスト_閲覧済み） | Category/list viewed（日本語訳：カテゴリ/閲覧リスト） | list_name, products[]（日本語訳：リスト名、製品[]） |
| product_searched（日本語訳：製品検索済み） | Search performed（日本語訳：実行された検索） | query, results_count（日本語訳：クエリ、結果数） |
| product_filtered（日本語訳：製品フィルタ済み） | Filters applied（日本語訳：適用されたフィルター） | filter_type, filter_value（日本語訳：フィルターの種類、フィルターの値） |
| product_sorted（日本語訳：製品_分類済み） | Sort applied（日本語訳：ソートが適用されました） | sort_by, sort_order（日本語訳：並べ替え、並べ替え順） |

### Cart （日本語訳：カート）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| product_added_to_cart（日本語訳：製品をカートに追加しました） | Item added（日本語訳：項目を追加しました） | product_id, product_name, price, quantity（日本語訳：製品ID、製品名、価格、数量） |
| product_removed_from_cart（日本語訳：カートから削除された製品） | Item removed（日本語訳：アイテムが削除されました） | product_id, product_name, price, quantity（日本語訳：製品ID、製品名、価格、数量） |
| cart_viewed（日本語訳：カート_閲覧済み） | Cart page viewed（日本語訳：カートページを閲覧しました） | cart_value, items_count（日本語訳：カートの値、商品数） |

### Checkout （日本語訳：チェックアウト）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| checkout_started（日本語訳：チェックアウト開始済み） | Checkout began（日本語訳：チェックアウトが始まりました） | cart_value, items_count（日本語訳：カートの値、商品数） |
| checkout_step_completed（日本語訳：チェックアウト_ステップ_完了） | Step finished（日本語訳：ステップが完了しました） | step_number, step_name（日本語訳：ステップ番号、ステップ名） |
| shipping_info_entered（日本語訳：Shipping_info_entered） | Address entered（日本語訳：入力された住所） | shipping_method（日本語訳：発送方法） |
| payment_info_entered（日本語訳：支払い情報が入力されました） | Payment entered（日本語訳：支払いが入力されました） | payment_method（日本語訳：支払方法） |
| coupon_applied（日本語訳：クーポン_適用済み） | Coupon used（日本語訳：使用したクーポン） | coupon_code, discount_value（日本語訳：クーポンコード、割引値） |
| purchase_completed（日本語訳：購入_完了） | Order placed（日本語訳：注文済み） | transaction_id, value, currency, items[]（日本語訳：トランザクションID、値、通貨、アイテム[]） |

### Post-Purchase （日本語訳：購入後）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| order_confirmed（日本語訳：注文_確認済み） | Confirmation viewed（日本語訳：確認が表示されました） | transaction_id（日本語訳：トランザクションID） |
| refund_requested（日本語訳：返金要求済み） | Refund initiated（日本語訳：払い戻しが開始されました） | transaction_id, reason（日本語訳：トランザクションID、理由） |
| refund_completed（日本語訳：返金_完了） | Refund processed（日本語訳：返金処理済み） | transaction_id, value（日本語訳：トランザクションID、値） |
| review_submitted（日本語訳：レビュー_送信済み） | Product reviewed（日本語訳：レビューされた製品） | product_id, rating（日本語訳：製品ID、評価） |

---

## B2B / SaaS Specific Events （日本語訳：B2B / SaaS 固有のイベント）

### Team & Collaboration （日本語訳：チームとコラボレーション）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| team_created（日本語訳：チーム作成） | New team/org made（日本語訳：新しいチーム/組織が作成されました） | team_size, plan（日本語訳：チームサイズ、計画） |
| team_member_invited（日本語訳：チームメンバー_招待済み） | Invite sent（日本語訳：招待状を送信しました） | role, invite_method（日本語訳：ロール、inviate_method） |
| team_member_joined（日本語訳：チームメンバー_参加者） | Member accepted（日本語訳：メンバーが承認されました） | role（日本語訳：役割） |
| team_member_removed（日本語訳：チームメンバー_削除済み） | Member removed（日本語訳：メンバーが削除されました） | role（日本語訳：役割） |
| role_changed（日本語訳：役割_変更されました） | Permissions updated（日本語訳：権限が更新されました） | user_id, old_role, new_role（日本語訳：ユーザー ID、古い役割、新しい役割） |

### Integration Events （日本語訳：統合イベント）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| integration_viewed（日本語訳：統合_閲覧済み） | Integration page seen（日本語訳：統合ページが表示されました） | integration_name（日本語訳：統合名） |
| integration_started（日本語訳：統合開始済み） | Setup began（日本語訳：セットアップが始まりました） | integration_name（日本語訳：統合名） |
| integration_connected（日本語訳：統合接続済み） | Successfully connected（日本語訳：正常に接続されました） | integration_name（日本語訳：統合名） |
| integration_disconnected（日本語訳：統合_切断） | Removed integration（日本語訳：削除された統合） | integration_name, reason（日本語訳：統合名、理由） |

### Account Events （日本語訳：アカウントイベント）

| Event Name（日本語訳：イベント名） | Description（日本語訳：説明） | Properties（日本語訳：プロパティ） |
|------------|-------------|------------|
| account_created（日本語訳：アカウント_作成済み） | New account（日本語訳：新しいアカウント） | source, plan（日本語訳：ソース、計画） |
| account_upgraded（日本語訳：アカウント_アップグレード済み） | Plan upgrade（日本語訳：プランのアップグレード） | from_plan, to_plan（日本語訳：from_plan、to_plan） |
| account_churned（日本語訳：アカウント_チャーン） | Account closed（日本語訳：アカウントが閉鎖されました） | reason, tenure, mrr_lost（日本語訳：理由、在職期間、mrr_lost） |
| account_reactivated（日本語訳：アカウント_再アクティブ化されました） | Returned customer（日本語訳：返品されたお客様） | previous_tenure, new_plan（日本語訳：以前の在職期間、新しい計画） |

---

## Event Properties (Parameters) （日本語訳：イベントのプロパティ (パラメータ)）

### Standard Properties to Include （日本語訳：含める標準プロパティ）

**User Context:** （日本語訳：**ユーザーコンテキスト:**）
```
user_id: "12345"
user_type: "free" | "trial" | "paid"
account_id: "acct_123"
plan_type: "starter" | "pro" | "enterprise"
```

**Session Context:** （日本語訳：**セッションコンテキスト:**）
```
session_id: "sess_abc"
session_number: 5
page: "/pricing"
referrer: "https://google.com"
```

**Campaign Context:** （日本語訳：**キャンペーンの内容:**）
```
source: "google"
medium: "cpc"
campaign: "spring_sale"
content: "hero_cta"
```

**Product Context (E-commerce):** （日本語訳：**製品コンテキスト (電子商取引):**）
```
product_id: "SKU123"
product_name: "Product Name"
category: "Category"
price: 99.99
quantity: 1
currency: "USD"
```

**Timing:** （日本語訳：**タイミング：**）
```
timestamp: "2024-01-15T10:30:00Z"
time_on_page: 45
session_duration: 300
```

---

## Funnel Event Sequences （日本語訳：ファネルイベントシーケンス）

### Signup Funnel （日本語訳：サインアップファネル）
1. signup_started （日本語訳：サインアップ_開始済み）
2. signup_step_completed (email) （日本語訳：サインアップ_ステップ_完了 (メール)）
3. signup_step_completed (password) （日本語訳：Signup_step_completed (パスワード)）
4. signup_completed （日本語訳：サインアップ_完了）
5. onboarding_started （日本語訳：オンボーディング_開始済み）

### Purchase Funnel （日本語訳：購入ファネル）
1. pricing_viewed （日本語訳：価格設定_閲覧済み）
2. plan_selected （日本語訳：プラン_選択済み）
3. checkout_started （日本語訳：チェックアウト開始済み）
4. payment_info_entered （日本語訳：支払い情報が入力されました）
5. purchase_completed （日本語訳：購入_完了）

### E-commerce Funnel （日本語訳：Eコマースファネル）
1. product_viewed （日本語訳：製品_閲覧済み）
2. product_added_to_cart （日本語訳：製品をカートに追加しました）
3. cart_viewed （日本語訳：カート_閲覧済み）
4. checkout_started （日本語訳：チェックアウト開始済み）
5. shipping_info_entered （日本語訳：Shipping_info_entered）
6. payment_info_entered （日本語訳：支払い情報が入力されました）
7. purchase_completed （日本語訳：購入_完了）
