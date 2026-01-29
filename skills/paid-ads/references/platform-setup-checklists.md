# Platform Setup Checklists （プラットフォーム設定チェックリスト）

Complete setup checklists for major ad platforms. （主要な広告プラットフォームの設定チェックリストを完了します。）

## Google Ads Setup （Google 広告の設定）

### Account Foundation （アカウントの基盤）

- [ ] Google Ads account created and verified （[ ] Google 広告アカウントが作成および確認されました）
- [ ] Billing information added （[ ] 請求情報を追加しました）
- [ ] Time zone and currency set correctly （[ ] タイムゾーンと通貨が正しく設定されている）
- [ ] Account access granted to team members （[ ] チームメンバーに付与されたアカウントアクセス）

### Conversion Tracking （コンバージョントラッキング）

- [ ] Google tag installed on all pages （[ ] すべてのページに Google タグがインストールされています）
- [ ] Conversion actions created (purchase, lead, signup) （[ ] 作成されたコンバージョン アクション（購入、リード、サインアップ））
- [ ] Conversion values assigned (if applicable) （[ ] 割り当てられた変換値 (該当する場合)）
- [ ] Enhanced conversions enabled （[ ] 拡張変換が有効になりました）
- [ ] Test conversions firing correctly （[ ] 変換が正しく実行されるかテストする）
- [ ] Import conversions from GA4 (optional) （[ ] GA4 からコンバージョンをインポートする (オプション)）

### Analytics Integration （分析の統合）

- [ ] Google Analytics 4 linked （[ ] Google アナリティクス 4 がリンクされました）
- [ ] Auto-tagging enabled （[ ] 自動タグ付けが有効です）
- [ ] GA4 audiences available in Google Ads （[ ] Google 広告で利用できる GA4 オーディエンス）
- [ ] Cross-domain tracking set up (if multiple domains) （[ ] クロスドメイン追跡の設定 (複数ドメインの場合)）

### Audience Setup （視聴者の設定）

- [ ] Remarketing tag verified （[ ] リマーケティング タグが確認されました）
- [ ] Website visitor audiences created: （[ ] Web サイト訪問者が作成したオーディエンス:）
  - All visitors (180 days) （すべての訪問者 (180 日間)）
  - Key page visitors (pricing, demo, features) （主要なページ訪問者 (価格、デモ、機能)）
  - Converters (for exclusion) （コンバーター（除く））
- [ ] Customer match lists uploaded （[ ] 顧客一致リストがアップロードされました）
- [ ] Similar audiences enabled （[ ] 類似ユーザーが有効になっています）

### Campaign Readiness （キャンペーンの準備状況）

- [ ] Negative keyword lists created: （[ ] 作成された除外キーワード リスト:）
  - Universal negatives (free, jobs, careers, reviews, complaints) （普遍的なネガティブ (無料、仕事、キャリア、レビュー、苦情)）
  - Competitor negatives (if needed) （競合他社のネガ（必要な場合））
  - Irrelevant industry terms （無関係な業界用語）
- [ ] Location targeting set (include/exclude) （[ ] ターゲット地域セット (含む/除外)）
- [ ] Language targeting set （[ ] ターゲット言語セット）
- [ ] Ad schedule configured (if B2B, business hours) （[ ] 広告スケジュールが設定されています (B2B の場合は営業時間)）
- [ ] Device bid adjustments considered （[ ] デバイスの入札単価調整を検討中）

### Ad Extensions （広告表示オプション）

- [ ] Sitelinks (4-6 relevant pages) （[ ] サイトリンク (関連ページ 4 ～ 6)）
- [ ] Callouts (key benefits, offers) （[ ] コールアウト (主な特典、オファー)）
- [ ] Structured snippets (features, types, services) （[ ] 構造化スニペット (機能、タイプ、サービス)）
- [ ] Call extension (if phone leads valuable) （[ ] 電話内線番号（電話でのリードが貴重な場合））
- [ ] Lead form extension (if using) （[ ] リードフォーム拡張子 (使用している場合)）
- [ ] Price extensions (if applicable) （[ ] 価格表示オプション（該当する場合））
- [ ] Image extensions (where available) （[ ] 画像拡張子 (利用可能な場合)）

### Brand Protection （ブランド保護）

- [ ] Brand campaign running (protect branded terms) （[ ] ブランド キャンペーン実施中 (ブランド規約を保護)）
- [ ] Competitor campaigns considered （[ ] 競合キャンペーンを検討中）
- [ ] Brand terms in negative lists for non-brand campaigns （[ ] 非ブランド キャンペーンのネガティブ リスト内のブランド用語）

---

## Meta Ads Setup （メタ広告の設定）

### Business Manager Foundation （ビジネスマネージャー財団）

- [ ] Business Manager created （[ ] ビジネスマネージャーが作成されました）
- [ ] Business verified (if running certain ad types) （[ ] ビジネスの確認済み（特定の広告タイプを掲載している場合））
- [ ] Ad account created within Business Manager （[ ] Business Manager 内で広告アカウントが作成されました）
- [ ] Payment method added （[ ] お支払い方法を追加しました）
- [ ] Team access configured with proper roles （[ ] 適切な役割で構成されたチーム アクセス）

### Pixel & Tracking （ピクセルとトラッキング）

- [ ] Meta Pixel installed on all pages （[ ] すべてのページにメタ ピクセルがインストールされています）
- [ ] Standard events configured: （[ ] 設定された標準イベント:）
  - PageView (automatic) （ページビュー (自動)）
  - ViewContent (product/feature pages) （ViewContent (製品/特集ページ)）
  - Lead (form submissions) （リード (フォーム送信)）
  - Purchase (conversions) （購入（コンバージョン））
  - AddToCart (if e-commerce) （カートに追加 (電子商取引の場合)）
  - InitiateCheckout (if e-commerce) （InitiateCheckout (電子商取引の場合)）
- [ ] Conversions API (CAPI) set up for server-side tracking （[ ] サーバー側トラッキング用に設定された Conversions API (CAPI)）
- [ ] Event Match Quality score > 6 （[ ] イベント マッチの品質スコア > 6）
- [ ] Test events in Events Manager （[ ] イベント マネージャーでイベントをテストする）

### Domain & Aggregated Events （ドメインおよび集約イベント）

- [ ] Domain verified in Business Manager （[ ] Business Manager でドメインが確認されました）
- [ ] Aggregated Event Measurement configured （[ ] 集約イベント測定が設定されました）
- [ ] Top 8 events prioritized in order of importance （[ ] 上位 8 件のイベントを重要度順に並べたもの）
- [ ] Web events prioritized for iOS 14+ tracking （[ ] iOS 14 以降の追跡で優先される Web イベント）

### Audience Setup （視聴者の設定）

- [ ] Custom audiences created: （[ ] 作成されたカスタム オーディエンス:）
  - Website visitors (all, 30/60/90/180 days) （Web サイト訪問者 (すべて、30/60/90/180 日)）
  - Key page visitors （主要なページ訪問者）
  - Video viewers (25%, 50%, 75%, 95%) （動画視聴者 (25%、50%、75%、95%)）
  - Page/Instagram engagers （ページ/Instagram エンゲージメント）
  - Customer list uploaded （顧客リストをアップロードしました）
- [ ] Lookalike audiences created (1%, 1-3%) （[ ] 類似オーディエンスが作成されました (1%、1～3%)）
- [ ] Saved audiences for common targeting （[ ] 共通ターゲティング用に保存されたオーディエンス）

### Catalog (E-commerce) （カタログ（電子商取引））

- [ ] Product catalog connected （[ ] 製品カタログが接続されました）
- [ ] Product feed updating correctly （[ ] 商品フィードが正しく更新されています）
- [ ] Catalog sales campaigns enabled （[ ] カタログ販売キャンペーンが有効になりました）
- [ ] Dynamic product ads configured （[ ] 動的商品広告が設定されました）

### Creative Assets （クリエイティブアセット）

- [ ] Images in correct sizes: （[ ] 正しいサイズの画像:）
  - Feed: 1080x1080 (1:1) （フィード: 1080x1080 (1:1)）
  - Stories/Reels: 1080x1920 (9:16) （ストーリー/リール: 1080x1920 (9:16)）
  - Landscape: 1200x628 (1.91:1) （風景: 1200x628 (1.91:1)）
- [ ] Videos in correct formats （[ ] 正しい形式のビデオ）
- [ ] Ad copy variations ready （[ ] 広告コピーのバリエーションが準備完了）
- [ ] UTM parameters in all destination URLs （すべての宛先 URL の [ ] UTM パラメータ）

### Compliance （コンプライアンス）

- [ ] Special Ad Categories declared (if housing, credit, employment, politics) （[ ] 宣言された特別広告カテゴリ (住宅、信用、雇用、政治の場合)）
- [ ] Landing page complies with Meta policies （[ ] ランディング ページはメタ ポリシーに準拠しています）
- [ ] No prohibited content in ads （[ ] 広告に禁止されているコンテンツはありません）

---

## LinkedIn Ads Setup （LinkedIn 広告の設定）

### Campaign Manager Foundation （キャンペーン マネージャー財団）

- [ ] Campaign Manager account created （[ ] キャンペーン マネージャー アカウントが作成されました）
- [ ] Company Page connected （[ ] 会社ページが接続されました）
- [ ] Billing information added （[ ] 請求情報を追加しました）
- [ ] Team access configured （[ ] チームアクセスが設定されました）

### Insight Tag & Tracking （インサイトタグとトラッキング）

- [ ] LinkedIn Insight Tag installed on all pages （[ ] LinkedIn Insight タグがすべてのページにインストールされています）
- [ ] Tag verified and firing （[ ] タグが検証され、起動されました）
- [ ] Conversion tracking configured: （[ ] コンバージョン トラッキングが設定されています:）
  - URL-based conversions （URLベースのコンバージョン）
  - Event-specific conversions （イベント固有のコンバージョン）
- [ ] Conversion values set (if applicable) （[ ] 設定された変換値 (該当する場合)）

### Audience Setup （視聴者の設定）

- [ ] Matched Audiences created: （[ ] 一致するオーディエンスが作成されました:）
  - Website retargeting audiences （ウェブサイトのリターゲティングオーディエンス）
  - Company list uploaded (for ABM) （会社リストをアップロードしました（ABM用））
  - Contact list uploaded （連絡先リストがアップロードされました）
- [ ] Lookalike audiences created （[ ] 類似オーディエンスが作成されました）
- [ ] Saved audiences for common targeting （[ ] 共通ターゲティング用に保存されたオーディエンス）

### Lead Gen Forms (if using) （リード獲得フォーム (使用している場合)）

- [ ] Lead gen form templates created （[ ] 見込み顧客獲得フォーム テンプレートが作成されました）
- [ ] Form fields selected (minimize for conversion) （[ ] 選択されたフォームフィールド (変換のために最小化)）
- [ ] Privacy policy URL added （[ ] プライバシーポリシーのURLを追加しました）
- [ ] Thank you message configured （[ ] ありがとうメッセージが設定されました）
- [ ] CRM integration set up (or CSV export process) （[ ] CRM統合設定（またはCSVエクスポートプロセス））

### Document Ads (if using) （ドキュメント広告 (使用している場合)）

- [ ] Documents uploaded (PDF, PowerPoint) （[ ] アップロードされたドキュメント (PDF、PowerPoint)）
- [ ] Gating configured (full gate or preview) （[ ] ゲート設定済み (フルゲートまたはプレビュー)）
- [ ] Lead gen form connected （[ ] リード獲得フォームが接続されました）

### Creative Assets （クリエイティブアセット）

- [ ] Single image ads: 1200x627 (1.91:1) or 1080x1080 (1:1) （[ ] 単一イメージ広告: 1200x627 (1.91:1) または 1080x1080 (1:1)）
- [ ] Carousel images ready （[ ] カルーセル画像の準備ができました）
- [ ] Video specs met (if using) （[ ] ビデオ仕様を満たしている (使用している場合)）
- [ ] Ad copy within character limits: （[ ] 文字数制限内の広告コピー:）
  - Intro text: 600 max, 150 recommended （紹介テキスト: 最大 600、推奨 150）
  - Headline: 200 max, 70 recommended （見出し: 最大 200、推奨 70）

### Budget Considerations （予算に関する考慮事項）

- [ ] Budget realistic for LinkedIn CPCs ($8-15+ typical) （[ ] LinkedIn CPC にとって現実的な予算 (通常 8 ～ 15 ドル以上)）
- [ ] Audience size validated (50K+ recommended) （[ ] オーディエンス サイズが検証済み (50,000 以上を推奨)）
- [ ] Daily vs. lifetime budget decided （[ ] 1 日の予算と生涯の予算の決定）
- [ ] Bid strategy selected （[ ] 入札戦略が選択されました）

---

## Twitter/X Ads Setup （Twitter/X 広告の設定）

### Account Foundation （アカウントの基盤）

- [ ] Ads account created （[ ] 広告アカウントが作成されました）
- [ ] Payment method added （[ ] お支払い方法を追加しました）
- [ ] Account verified (if required) （[ ] アカウントが確認されました (必要な場合)）

### Tracking （トラッキング）

- [ ] Twitter Pixel installed （[ ] Twitter Pixel がインストールされました）
- [ ] Conversion events created （[ ] コンバージョン イベントが作成されました）
- [ ] Website tag verified （[ ] ウェブサイトのタグが確認されました）

### Audience Setup （視聴者の設定）

- [ ] Tailored audiences created: （[ ] カスタマイズされたオーディエンスが作成されました:）
  - Website visitors （ウェブサイト訪問者）
  - Customer lists （顧客リスト）
- [ ] Follower lookalikes identified （[ ] フォロワーのそっくりさんが特定されました）
- [ ] Interest and keyword targets researched （[ ] インタレストとキーワード ターゲットを調査しました）

### Creative （クリエイティブ）

- [ ] Tweet copy within 280 characters （[ ] ツイートコピー280文字以内）
- [ ] Images: 1200x675 (1.91:1) or 1200x1200 (1:1) （[ ] 画像：1200x675 (1.91:1) または 1200x1200 (1:1)）
- [ ] Video specs met (if using) （[ ] ビデオ仕様を満たしている (使用している場合)）
- [ ] Cards configured (website, app, etc.) （[ ] 設定されたカード (Web サイト、アプリなど)）

---

## TikTok Ads Setup （TikTok広告の設定）

### Account Foundation （アカウントの基盤）

- [ ] TikTok Ads Manager account created （[ ] TikTok 広告マネージャー アカウントが作成されました）
- [ ] Business verification completed （[ ] ビジネス認証が完了しました）
- [ ] Payment method added （[ ] お支払い方法を追加しました）

### Pixel & Tracking （ピクセルとトラッキング）

- [ ] TikTok Pixel installed （[ ] TikTok Pixel がインストールされました）
- [ ] Events configured (ViewContent, Purchase, etc.) （[ ] 設定されたイベント (ViewContent、Purchase など)）
- [ ] Events API set up (recommended) （[ ] イベント API のセットアップ (推奨)）

### Audience Setup （視聴者の設定）

- [ ] Custom audiences created （[ ] カスタム オーディエンスが作成されました）
- [ ] Lookalike audiences created （[ ] 類似オーディエンスが作成されました）
- [ ] Interest categories identified （[ ] インタレスト カテゴリが特定されました）

### Creative （クリエイティブ）

- [ ] Vertical video (9:16) ready （[ ] 縦型ビデオ (9:16) 準備完了）
- [ ] Native-feeling content (not too polished) （[ ] ネイティブ感のあるコンテンツ (洗練されすぎていない)）
- [ ] First 3 seconds are compelling hooks （[ ] 最初の 3 秒が魅力的なフックです）
- [ ] Captions added (most watch without sound) （[ ] キャプションを追加しました (ほとんどの視聴は音声なし)）
- [ ] Music/sounds selected (licensed if needed) （[ ] 選択した音楽/サウンド (必要に応じてライセンスを取得)）

---

## Universal Pre-Launch Checklist （ユニバーサル発売前チェックリスト）

Before launching any campaign: （キャンペーンを開始する前に:）

- [ ] Conversion tracking tested with real conversion （[ ] 実際のコンバージョンでテストされたコンバージョン トラッキング）
- [ ] Landing page loads fast (<3 sec) （[ ] ランディング ページの読み込みが速い (3 秒未満)）
- [ ] Landing page mobile-friendly （[ ] ランディング ページ モバイル対応）
- [ ] UTM parameters working （[ ] UTM パラメータが機能する）
- [ ] Budget set correctly (daily vs. lifetime) （[ ] 予算が正しく設定されている (1 日と生涯)）
- [ ] Start/end dates correct （[ ] 開始日/終了日が正しい）
- [ ] Targeting matches intended audience （[ ] ターゲティングが対象ユーザーと一致する）
- [ ] Ad creative approved （[ ] 広告クリエイティブが承認されました）
- [ ] Team notified of launch （[ ] チームに発売の通知）
- [ ] Reporting dashboard ready （[ ] レポート ダッシュボードの準備が完了しました）
