# Event Library Reference （イベントライブラリリファレンス）

Comprehensive list of events to track by business type and context. （ビジネスの種類とコンテキストごとに追跡するイベントの包括的なリスト。）

## Marketing Site Events （マーケティングサイトのイベント）

### Navigation & Engagement （ナビゲーションとエンゲージメント）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| page_view（ページビュー） | Page loaded (enhanced)（ページが読み込まれました (拡張)） | page_title, page_location, content_group（page_title、page_location、content_group） |
| scroll_depth（スクロール深度） | User scrolled to threshold（ユーザーがしきい値までスクロールしました） | depth (25, 50, 75, 100)（深さ (25、50、75、100)） |
| outbound_link_clicked（outbound_link_clicked） | Click to external site（クリックすると外部サイトへ） | link_url, link_text（リンクURL、リンクテキスト） |
| internal_link_clicked（Internal_link_clicked） | Click within site（サイト内をクリック） | link_url, link_text, location（リンクURL、リンクテキスト、場所） |
| video_played（video_played） | Video started（ビデオが開始されました） | video_id, video_title, duration（video_id、video_title、再生時間） |
| video_completed（ビデオ_完了） | Video finished（ビデオが完成しました） | video_id, video_title, duration（video_id、video_title、再生時間） |

### CTA & Form Interactions （CTA とフォームのインタラクション）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| cta_clicked（cta_clicked） | Call to action clicked（行動喚起がクリックされました） | button_text, cta_location, page（button_text、cta_location、ページ） |
| form_started（フォーム_開始済み） | User began form（ユーザーがフォームを開始しました） | form_name, form_location（フォーム名、フォームの場所） |
| form_field_completed（フォームフィールド_完了） | Field filled（フィールドが入力されました） | form_name, field_name（フォーム名、フィールド名） |
| form_submitted（フォーム送信済み） | Form successfully sent（フォームは正常に送信されました） | form_name, form_location（フォーム名、フォームの場所） |
| form_error（フォームエラー） | Form validation failed（フォームの検証に失敗しました） | form_name, error_type（フォーム名、エラーの種類） |
| resource_downloaded（リソース_ダウンロード済み） | Asset downloaded（ダウンロードされたアセット） | resource_name, resource_type（リソース名、リソースタイプ） |

### Conversion Events （コンバージョンイベント）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| signup_started（サインアップ_開始済み） | Initiated signup（サインアップを開始しました） | source, page（ソース、ページ） |
| signup_completed（サインアップ_完了） | Finished signup（サインアップが完了しました） | method, plan, source（方法、計画、ソース） |
| demo_requested（デモ要求済み） | Demo form submitted（デモフォームが送信されました） | company_size, industry（会社規模、業種） |
| contact_submitted（連絡先_送信済み） | Contact form sent（お問い合わせフォームを送信しました） | inquiry_type（お問い合わせの種類） |
| newsletter_subscribed（ニュースレター_購読済み） | Email list signup（メールリストの登録） | source, list_name（ソース、リスト名） |
| trial_started（トライアル開始済み） | Free trial began（無料トライアルが始まりました） | plan, source（計画、ソース） |

---

## Product/App Events （製品/アプリのイベント）

### Onboarding （オンボーディング）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| signup_completed（サインアップ_完了） | Account created（アカウントが作成されました） | method, referral_source（メソッド、referral_source） |
| onboarding_started（オンボーディング_開始済み） | Began onboarding（オンボーディングを開始しました） | - |
| onboarding_step_completed（オンボーディング_ステップ_完了） | Step finished（ステップが完了しました） | step_number, step_name（ステップ番号、ステップ名） |
| onboarding_completed（オンボーディング_完了） | All steps done（すべての手順が完了しました） | steps_completed, time_to_complete（完了したステップ数、完了までの時間） |
| onboarding_skipped（オンボーディング_スキップされました） | User skipped onboarding（ユーザーがオンボーディングをスキップした） | step_skipped_at（step_skipped_at） |
| first_key_action_completed（first_key_action_completed） | Aha moment reached（ああ、その瞬間が来た） | action_type（アクションタイプ） |

### Core Usage （コアの使用法）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| session_started（セッション開始済み） | App session began（アプリセッションが開始されました） | session_number（セッション番号） |
| feature_used（使用されている機能） | Feature interaction（機能の相互作用） | feature_name, feature_category（機能名、機能カテゴリ） |
| action_completed（アクション_完了） | Core action done（主要なアクションが完了しました） | action_type, count（アクションタイプ、カウント） |
| content_created（コンテンツ作成済み） | User created content（ユーザーが作成したコンテンツ） | content_type（コンテンツタイプ） |
| content_edited（コンテンツ編集済み） | User modified content（ユーザーが変更したコンテンツ） | content_type（コンテンツタイプ） |
| content_deleted（コンテンツ_削除済み） | User removed content（ユーザーが削除したコンテンツ） | content_type（コンテンツタイプ） |
| search_performed（検索実行済み） | In-app search（アプリ内検索） | query, results_count（クエリ、結果数） |
| settings_changed（設定変更済み） | Settings modified（設定が変更されました） | setting_name, new_value（設定名、新しい値） |
| invite_sent（招待送信済み） | User invited others（ユーザーが他の人を招待しました） | invite_type, count（招待タイプ、数） |

### Errors & Support （エラーとサポート）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| error_occurred（エラーが発生しました） | Error experienced（エラーが発生しました） | error_type, error_message, page（エラータイプ、エラーメッセージ、ページ） |
| help_opened（ヘルプ_開いた） | Help accessed（アクセスしたヘルプ） | help_type, page（ヘルプ_タイプ、ページ） |
| support_contacted（サポート連絡済み） | Support request made（サポートリクエストが行われました） | contact_method, issue_type（連絡方法、問題の種類） |
| feedback_submitted（フィードバック_送信済み） | User feedback given（ユーザーからのフィードバック） | feedback_type, rating（フィードバックの種類、評価） |

---

## Monetization Events （収益化イベント）

### Pricing & Checkout （価格設定とチェックアウト）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| pricing_viewed（価格設定_閲覧済み） | Pricing page seen（価格ページが表示されました） | source（ソース） |
| plan_selected（プラン_選択済み） | Plan chosen（選択したプラン） | plan_name, billing_cycle（プラン名、請求サイクル） |
| checkout_started（チェックアウト開始済み） | Began checkout（チェックアウトを開始しました） | plan, value（計画、価値観） |
| payment_info_entered（支払い情報が入力されました） | Payment submitted（支払いが完了しました） | payment_method（支払方法） |
| purchase_completed（購入_完了） | Purchase successful（購入が成功しました） | plan, value, currency, transaction_id（プラン、値、通貨、transaction_id） |
| purchase_failed（購入_失敗） | Purchase failed（購入に失敗しました） | error_reason, plan（エラーの理由、計画） |

### Subscription Management （サブスクリプション管理）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| trial_started（トライアル開始済み） | Trial began（裁判が始まりました） | plan, trial_length（プラン、トライアルの長さ） |
| trial_ended（トライアル終了） | Trial expired（トライアル期間が終了しました） | plan, converted (bool)（計画、変換済み (ブール値)） |
| subscription_upgraded（サブスクリプション_アップグレード済み） | Plan upgraded（プランがアップグレードされました） | from_plan, to_plan, value（from_plan、to_plan、値） |
| subscription_downgraded（サブスクリプション_ダウングレード） | Plan downgraded（プランがダウングレードされました） | from_plan, to_plan（from_plan、to_plan） |
| subscription_cancelled（サブスクリプション_キャンセル済み） | Cancelled（キャンセル） | plan, reason, tenure（計画、理由、在職期間） |
| subscription_renewed（サブスクリプション_更新済み） | Renewed（リニューアル） | plan, value（計画、価値観） |
| billing_updated（請求_更新済み） | Payment method changed（支払い方法が変更されました） | - |

---

## E-commerce Events （Eコマースイベント）

### Browsing （ブラウジング）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| product_viewed（製品_閲覧済み） | Product page viewed（製品ページを閲覧しました） | product_id, product_name, category, price（製品ID、製品名、カテゴリ、価格） |
| product_list_viewed（製品リスト_閲覧済み） | Category/list viewed（カテゴリ/閲覧リスト） | list_name, products[]（リスト名、製品[]） |
| product_searched（製品検索済み） | Search performed（実行された検索） | query, results_count（クエリ、結果数） |
| product_filtered（製品フィルタ済み） | Filters applied（適用されたフィルター） | filter_type, filter_value（フィルターの種類、フィルターの値） |
| product_sorted（製品_分類済み） | Sort applied（ソートが適用されました） | sort_by, sort_order（並べ替え、並べ替え順） |

### Cart （カート）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| product_added_to_cart（製品をカートに追加しました） | Item added（項目を追加しました） | product_id, product_name, price, quantity（製品ID、製品名、価格、数量） |
| product_removed_from_cart（カートから削除された製品） | Item removed（アイテムが削除されました） | product_id, product_name, price, quantity（製品ID、製品名、価格、数量） |
| cart_viewed（カート_閲覧済み） | Cart page viewed（カートページを閲覧しました） | cart_value, items_count（カートの値、商品数） |

### Checkout （チェックアウト）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| checkout_started（チェックアウト開始済み） | Checkout began（チェックアウトが始まりました） | cart_value, items_count（カートの値、商品数） |
| checkout_step_completed（チェックアウト_ステップ_完了） | Step finished（ステップが完了しました） | step_number, step_name（ステップ番号、ステップ名） |
| shipping_info_entered（Shipping_info_entered） | Address entered（入力された住所） | shipping_method（発送方法） |
| payment_info_entered（支払い情報が入力されました） | Payment entered（支払いが入力されました） | payment_method（支払方法） |
| coupon_applied（クーポン_適用済み） | Coupon used（使用したクーポン） | coupon_code, discount_value（クーポンコード、割引値） |
| purchase_completed（購入_完了） | Order placed（注文済み） | transaction_id, value, currency, items[]（トランザクションID、値、通貨、アイテム[]） |

### Post-Purchase （購入後）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| order_confirmed（注文_確認済み） | Confirmation viewed（確認が表示されました） | transaction_id（トランザクションID） |
| refund_requested（返金要求済み） | Refund initiated（払い戻しが開始されました） | transaction_id, reason（トランザクションID、理由） |
| refund_completed（返金_完了） | Refund processed（返金処理済み） | transaction_id, value（トランザクションID、値） |
| review_submitted（レビュー_送信済み） | Product reviewed（レビューされた製品） | product_id, rating（製品ID、評価） |

---

## B2B / SaaS Specific Events （B2B / SaaS 固有のイベント）

### Team & Collaboration （チームとコラボレーション）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| team_created（チーム作成） | New team/org made（新しいチーム/組織が作成されました） | team_size, plan（チームサイズ、計画） |
| team_member_invited（チームメンバー_招待済み） | Invite sent（招待状を送信しました） | role, invite_method（ロール、inviate_method） |
| team_member_joined（チームメンバー_参加者） | Member accepted（メンバーが承認されました） | role（役割） |
| team_member_removed（チームメンバー_削除済み） | Member removed（メンバーが削除されました） | role（役割） |
| role_changed（役割_変更されました） | Permissions updated（権限が更新されました） | user_id, old_role, new_role（ユーザー ID、古い役割、新しい役割） |

### Integration Events （統合イベント）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| integration_viewed（統合_閲覧済み） | Integration page seen（統合ページが表示されました） | integration_name（統合名） |
| integration_started（統合開始済み） | Setup began（セットアップが始まりました） | integration_name（統合名） |
| integration_connected（統合接続済み） | Successfully connected（正常に接続されました） | integration_name（統合名） |
| integration_disconnected（統合_切断） | Removed integration（削除された統合） | integration_name, reason（統合名、理由） |

### Account Events （アカウントイベント）

| Event Name（イベント名） | Description（説明） | Properties（プロパティ） |
|------------|-------------|------------|
| account_created（アカウント_作成済み） | New account（新しいアカウント） | source, plan（ソース、計画） |
| account_upgraded（アカウント_アップグレード済み） | Plan upgrade（プランのアップグレード） | from_plan, to_plan（from_plan、to_plan） |
| account_churned（アカウント_チャーン） | Account closed（アカウントが閉鎖されました） | reason, tenure, mrr_lost（理由、在職期間、mrr_lost） |
| account_reactivated（アカウント_再アクティブ化されました） | Returned customer（返品されたお客様） | previous_tenure, new_plan（以前の在職期間、新しい計画） |

---

## Event Properties (Parameters) （イベントのプロパティ (パラメータ)）

### Standard Properties to Include （含める標準プロパティ）

**User Context:** （**ユーザーコンテキスト:**）
```
user_id: "12345"
user_type: "free" | "trial" | "paid"
account_id: "acct_123"
plan_type: "starter" | "pro" | "enterprise"
```

**Session Context:** （**セッションコンテキスト:**）
```
session_id: "sess_abc"
session_number: 5
page: "/pricing"
referrer: "https://google.com"
```

**Campaign Context:** （**キャンペーンの内容:**）
```
source: "google"
medium: "cpc"
campaign: "spring_sale"
content: "hero_cta"
```

**Product Context (E-commerce):** （**製品コンテキスト (電子商取引):**）
```
product_id: "SKU123"
product_name: "Product Name"
category: "Category"
price: 99.99
quantity: 1
currency: "USD"
```

**Timing:** （**タイミング：**）
```
timestamp: "2024-01-15T10:30:00Z"
time_on_page: 45
session_duration: 300
```

---

## Funnel Event Sequences （ファネルイベントシーケンス）

### Signup Funnel （サインアップファネル）
1. signup_started （サインアップ_開始済み）
2. signup_step_completed (email) （サインアップ_ステップ_完了 (メール)）
3. signup_step_completed (password) （Signup_step_completed (パスワード)）
4. signup_completed （サインアップ_完了）
5. onboarding_started （オンボーディング_開始済み）

### Purchase Funnel （購入ファネル）
1. pricing_viewed （価格設定_閲覧済み）
2. plan_selected （プラン_選択済み）
3. checkout_started （チェックアウト開始済み）
4. payment_info_entered （支払い情報が入力されました）
5. purchase_completed （購入_完了）

### E-commerce Funnel （Eコマースファネル）
1. product_viewed （製品_閲覧済み）
2. product_added_to_cart （製品をカートに追加しました）
3. cart_viewed （カート_閲覧済み）
4. checkout_started （チェックアウト開始済み）
5. shipping_info_entered （Shipping_info_entered）
6. payment_info_entered （支払い情報が入力されました）
7. purchase_completed （購入_完了）
