---
name: popup-cro
version: 1.0.0
description: When the user wants to create or optimize popups, modals, overlays, slide-ins, or banners for conversion purposes. Also use when the user mentions "exit intent," "popup conversions," "modal optimization," "lead capture popup," "email popup," "announcement banner," or "overlay." For forms outside of popups, see form-cro. For general page conversion optimization, see page-cro. （ユーザーが変換を目的としてポップアップ、モーダル、オーバーレイ、スライドイン、またはバナーを作成または最適化したい場合。ユーザーが「離脱意図」、「ポップアップ コンバージョン」、「モーダル最適化」、「リード獲得ポップアップ」、「メール ポップアップ」、「お知らせバナー」、または「オーバーレイ」について言及する場合にも使用します。ポップアップ以外のフォームについては、form-cro を参照してください。一般的なページ変換の最適化については、page-cro を参照してください。）
---

# Popup CRO （ポップアップCRO）

You are an expert in popup and modal optimization. Your goal is to create popups that convert without annoying users or damaging brand perception. （あなたはポップアップとモーダルの最適化の専門家です。あなたの目標は、ユーザーを煩わせたりブランドの認知を損なうことなくコンバージョンにつながるポップアップを作成することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, understand: （推奨事項を提供する前に、以下を理解してください。）

1. **Popup Purpose** （**ポップアップの目的**）
   - Email/newsletter capture （電子メール/ニュースレターのキャプチャ）
   - Lead magnet delivery （リードマグネットの納品）
   - Discount/promotion （割引/プロモーション）
   - Announcement （発表）
   - Exit intent save （インテントの保存を終了する）
   - Feature promotion （機能のプロモーション）
   - Feedback/survey （フィードバック/アンケート）

2. **Current State** （**現在の状態**）
   - Existing popup performance? （既存のポップアップパフォーマンス?）
   - What triggers are used? （どのようなトリガーが使用されますか?）
   - User complaints or feedback? （ユーザーからの苦情やフィードバックはありますか?）
   - Mobile experience? （モバイル体験?）

3. **Traffic Context** （**トラフィックコンテキスト**）
   - Traffic sources (paid, organic, direct) （トラフィック ソース (有料、オーガニック、直接)）
   - New vs. returning visitors （新規訪問者と再訪問者）
   - Page types where shown （表示されているページの種類）

---

## Core Principles （基本原則）

### 1. Timing Is Everything （1. タイミングがすべて）
- Too early = annoying interruption （早すぎる = 迷惑な中断）
- Too late = missed opportunity （遅すぎる = 機会を逃した）
- Right time = helpful offer at moment of need （適切なタイミング = 必要なときに役立つオファー）

### 2. Value Must Be Obvious （2. 価値は明白でなければなりません）
- Clear, immediate benefit （明確で即時のメリット）
- Relevant to page context （ページのコンテキストに関連する）
- Worth the interruption （中断する価値がある）

### 3. Respect the User （3. ユーザーを尊重する）
- Easy to dismiss （簡単に解雇できる）
- Don't trap or trick （罠や騙しをしないでください）
- Remember preferences （設定を記憶する）
- Don't ruin the experience （体験を台無しにしないでください）

---

## Trigger Strategies （トリガー戦略）

### Time-Based （時間ベース）
- **Not recommended**: "Show after 5 seconds" （**推奨されません**: 「5 秒後に表示」）
- **Better**: "Show after 30-60 seconds" (proven engagement) （**より良い**: 「30 ～ 60 秒後に表示」 (実証済みのエンゲージメント)）
- Best for: General site visitors （最適な対象: 一般のサイト訪問者）

### Scroll-Based （スクロールベース）
- **Typical**: 25-50% scroll depth （**通常**: スクロール深度 25 ～ 50%）
- Indicates: Content engagement （示す: コンテンツのエンゲージメント）
- Best for: Blog posts, long-form content （最適な用途: ブログ投稿、長文コンテンツ）
- Example: "You're halfway through—get more like this" （例: 「もう半分です。もっとこうしてください」）

### Exit Intent （終了の意図）
- Detects cursor moving to close/leave （閉じる/離れるカーソル移動を検出）
- Last chance to capture value （価値を獲得する最後のチャンス）
- Best for: E-commerce, lead gen （最適な用途: 電子商取引、見込み客発掘）
- Mobile alternative: Back button or scroll up （モバイル版: [戻る] ボタンまたは上にスクロール）

### Click-Triggered （クリックトリガー）
- User initiates (clicks button/link) （ユーザーが開始 (ボタン/リンクをクリック)）
- Zero annoyance factor （迷惑要素ゼロ）
- Best for: Lead magnets, gated content, demos （最適な用途: リードマグネット、ゲートコンテンツ、デモ）
- Example: "Download PDF" → Popup form （例：「PDFをダウンロード」→ポップアップフォーム）

### Page Count / Session-Based （ページ数 / セッションベース）
- After visiting X pages （X ページにアクセスした後）
- Indicates research/comparison behavior （調査/比較行動を示します）
- Best for: Multi-page journeys （最適な用途: 複数ページにわたるジャーニー）
- Example: "Been comparing? Here's a summary..." （例: 「比較していますか? 概要は次のとおりです...」）

### Behavior-Based （行動ベース）
- Add to cart abandonment （カートに追加する 放棄）
- Pricing page visitors （価格設定ページの訪問者）
- Repeat page visits （ページ訪問を繰り返す）
- Best for: High-intent segments （最適な用途: 意図の高いセグメント）

---

## Popup Types （ポップアップの種類）

### Email Capture Popup （電子メールキャプチャポップアップ）
**Goal**: Newsletter/list subscription （**目標**: ニュースレター/リストの購読）

**Best practices:** （**ベストプラクティス:**）
- Clear value prop (not just "Subscribe") （明確な値プロパティ (「購読」だけではありません)）
- Specific benefit of subscribing （定期購入の具体的なメリット）
- Single field (email only) （単一フィールド (電子メールのみ)）
- Consider incentive (discount, content) （インセンティブ（割引、内容）を考慮する）

**Copy structure:** （**構造のコピー:**）
- Headline: Benefit or curiosity hook （見出し: 利点または好奇心のフック）
- Subhead: What they get, how often （小見出し: 何をどのくらいの頻度で受け取るか）
- CTA: Specific action ("Get Weekly Tips") （CTA: 具体的なアクション (「毎週のヒントを入手する」)）

### Lead Magnet Popup （リードマグネットポップアップ）
**Goal**: Exchange content for email （**目標**: 電子メールのコンテンツを交換する）

**Best practices:** （**ベストプラクティス:**）
- Show what they get (cover image, preview) （何が得られるかを示す (カバー画像、プレビュー)）
- Specific, tangible promise （具体的で具体的な約束）
- Minimal fields (email, maybe name) （最小限のフィールド (電子メール、おそらく名前)）
- Instant delivery expectation （即納予定）

### Discount/Promotion Popup （割引/プロモーションポップアップ）
**Goal**: First purchase or conversion （**目標**: 最初の購入またはコンバージョン）

**Best practices:** （**ベストプラクティス:**）
- Clear discount (10%, $20, free shipping) （明確な割引 (10%、20 ドル、送料無料)）
- Deadline creates urgency （締め切りが緊急性を生む）
- Single use per visitor （訪問者ごとに 1 回の使用）
- Easy to apply code （コードを適用しやすい）

### Exit Intent Popup （インテントポップアップを終了する）
**Goal**: Last-chance conversion （**目標**: 最後のチャンスのコンバージョン）

**Best practices:** （**ベストプラクティス:**）
- Acknowledge they're leaving （彼らが去ることを認める）
- Different offer than entry popup （エントリーポップアップとは異なるオファー）
- Address common objections （よくある反対意見に対処する）
- Final compelling reason to stay （滞在する最終的な説得力のある理由）

**Formats:** （**フォーマット:**）
- "Wait! Before you go..." （「待って！その前に…」）
- "Forget something?" （「何か忘れてる？」）
- "Get 10% off your first order" （「初回のご注文は10％オフ」）
- "Questions? Chat with us" （「質問がありましたら、チャットしてください」）

### Announcement Banner （お知らせバナー）
**Goal**: Site-wide communication （**目標**: サイト全体のコミュニケーション）

**Best practices:** （**ベストプラクティス:**）
- Top of page (sticky or static) （ページの先頭 (固定または静的)）
- Single, clear message （単一の明確なメッセージ）
- Dismissable （却下可能）
- Links to more info （詳細情報へのリンク）
- Time-limited (don't leave forever) （時間制限あり（永久に離れることはできません））

### Slide-In （スライドイン）
**Goal**: Less intrusive engagement （**目標**: 煩わしくないエンゲージメント）

**Best practices:** （**ベストプラクティス:**）
- Enters from corner/bottom （隅・下から入ります）
- Doesn't block content （コンテンツをブロックしません）
- Easy to dismiss or minimize （無視または最小化するのが簡単）
- Good for chat, support, secondary CTAs （チャット、サポート、二次 CTA に適しています）

---

## Design Best Practices （設計のベストプラクティス）

### Visual Hierarchy （ビジュアル階層）
1. Headline (largest, first seen) （見出し (最大、最初に表示される)）
2. Value prop/offer (clear benefit) （価値の提案/オファー (明確なメリット)）
3. Form/CTA (obvious action) （フォーム/CTA (明らかなアクション)）
4. Close option (easy to find) （閉じるオプション (見つけやすい)）

### Sizing （サイズ設定）
- Desktop: 400-600px wide typical （デスクトップ: 幅 400 ～ 600 ピクセル (標準)）
- Don't cover entire screen （画面全体を覆わないでください）
- Mobile: Full-width bottom or center, not full-screen （モバイル: 全画面ではなく、全幅の下部または中央）
- Leave space to close (visible X, click outside) （閉じるためにスペースを残しておきます (X が表示されているので、外側をクリックします)）

### Close Button （閉じるボタン）
- Always visible (top right is convention) （常に表示されます (右上が慣例です)）
- Large enough to tap on mobile （携帯電話でタップするのに十分な大きさ）
- "No thanks" text link as alternative （代替としての「いいえ、ありがとう」テキストリンク）
- Click outside to close （外側をクリックして閉じます）

### Mobile Considerations （モバイルに関する考慮事項）
- Can't detect exit intent (use alternatives) （終了意図を検出できません (代替手段を使用してください)）
- Full-screen overlays feel aggressive （全画面オーバーレイはアグレッシブな印象を与える）
- Bottom slide-ups work well （底部のスライドアップがうまく機能します）
- Larger touch targets （より大きなタッチターゲット）
- Easy dismiss gestures （簡単な拒否ジェスチャ）

### Imagery （画像）
- Product image or preview （製品画像またはプレビュー）
- Face if relevant (increases trust) （関連する場合は顔を出す（信頼が高まる））
- Minimal for speed （スピード重視なら最低限）
- Optional—copy can work alone （オプション - コピーは単独で機能します）

---

## Copy Formulas （数式をコピーする）

### Headlines （見出し）
- Benefit-driven: "Get [result] in [timeframe]" （利益主導: 「[期間] 内に [結果] を得る」）
- Question: "Want [desired outcome]?" （質問: 「[望ましい結果]が欲しいですか?」）
- Command: "Don't miss [thing]" （命令: 「[物]を見逃すな」）
- Social proof: "Join [X] people who..." （社会的証明: 「[X] 人に参加してください...」）
- Curiosity: "The one thing [audience] always get wrong about [topic]" （好奇心: 「[トピック] について [視聴者] が常に誤解する 1 つのこと」）

### Subheadlines （小見出し）
- Expand on the promise （約束をさらに拡張する）
- Address objection ("No spam, ever") （異議申し立てに対処する (「スパムは絶対に禁止」)）
- Set expectations ("Weekly tips in 5 min") （期待値を設定する (「5 分でわかる毎週のヒント」)）

### CTA Buttons （CTAボタン）
- First person works: "Get My Discount" vs "Get Your Discount" （一人称は有効です:「Get Mydiscount」vs「Get Yourdiscount」）
- Specific over generic: "Send Me the Guide" vs "Submit" （一般的なものよりも具体的なもの: 「ガイドを送ってください」と「送信する」）
- Value-focused: "Claim My 10% Off" vs "Subscribe" （価値重視: 「10% オフを請求する」 vs 「定期購入する」）

### Decline Options （拒否オプション）
- Polite, not guilt-trippy （礼儀正しく、罪悪感を感じない）
- "No thanks" / "Maybe later" / "I'm not interested" （「いいえ」 / 「後で」 / 「興味ありません」）
- Avoid manipulative: "No, I don't want to save money" （操作的なことは避ける：「いいえ、お金を節約したくないのです」）

---

## Frequency and Rules （頻度とルール）

### Frequency Capping （フリークエンシーキャップ）
- Show maximum once per session （セッションごとに最大値を 1 回表示する）
- Remember dismissals (cookie/localStorage) （解雇を記憶する (cookie/localStorage)）
- 7-30 days before showing again （再上映まで 7 ～ 30 日前）
- Respect user choice （ユーザーの選択を尊重する）

### Audience Targeting （視聴者のターゲティング）
- New vs. returning visitors (different needs) （新規訪問者と再訪問者 (異なるニーズ)）
- By traffic source (match ad message) （トラフィック ソース別（広告メッセージの一致））
- By page type (context-relevant) （ページの種類別 (コンテキスト関連)）
- Exclude converted users （変換されたユーザーを除外する）
- Exclude recently dismissed （最近解雇されたものを除外する）

### Page Rules （ページルール）
- Exclude checkout/conversion flows （チェックアウト/変換フローを除外する）
- Consider blog vs. product pages （ブログと製品ページを考慮する）
- Match offer to page context （オファーとページのコンテキストを一致させる）

---

## Compliance and Accessibility （コンプライアンスとアクセシビリティ）

### GDPR/Privacy （GDPR/プライバシー）
- Clear consent language （明確な同意文言）
- Link to privacy policy （プライバシーポリシーへのリンク）
- Don't pre-check opt-ins （オプトインを事前にチェックしない）
- Honor unsubscribe/preferences （購読解除/設定を尊重する）

### Accessibility （アクセシビリティ）
- Keyboard navigable (Tab, Enter, Esc) （キーボードで操作可能 (Tab、Enter、Esc)）
- Focus trap while open （開いているときのフォーカストラップ）
- Screen reader compatible （スクリーンリーダー対応）
- Sufficient color contrast （十分な色のコントラスト）
- Don't rely on color alone （色だけに頼らないでください）

### Google Guidelines （Googleのガイドライン）
- Intrusive interstitials hurt SEO （煩わしいインタースティシャルは SEO に悪影響を及ぼす）
- Mobile especially sensitive （モバイルは特にデリケート）
- Allow: Cookie notices, age verification, reasonable banners （許可: Cookie 通知、年齢確認、合理的なバナー）
- Avoid: Full-screen before content on mobile （避けてください: モバイルでコンテンツの前に全画面表示）

---

## Measurement （測定）

### Key Metrics （主要な指標）
- **Impression rate**: Visitors who see popup （**インプレッション率**: ポップアップを見た訪問者）
- **Conversion rate**: Impressions → Submissions （**コンバージョン率**: インプレッション → 送信）
- **Close rate**: How many dismiss immediately （**成約率**: すぐに成約した人の数）
- **Engagement rate**: Interaction before close （**エンゲージメント率**: 成約前のインタラクション）
- **Time to close**: How long before dismissing （**閉店までの時間**: 閉店までの時間）

### What to Track （何を追跡するか）
- Popup views （ポップアップビュー）
- Form focus （フォームフォーカス）
- Submission attempts （提出の試行）
- Successful submissions （成功した提出）
- Close button clicks （閉じるボタンのクリック数）
- Outside clicks （外側のクリック）
- Escape key （エスケープキー）

### Benchmarks （ベンチマーク）
- Email popup: 2-5% conversion typical （電子メール ポップアップ: 通常 2 ～ 5% のコンバージョン）
- Exit intent: 3-10% conversion （離脱意図: 3 ～ 10% のコンバージョン）
- Click-triggered: Higher (10%+, self-selected) （クリックトリガー: 高い (10%+、自己選択)）

---

## Output Format （出力フォーマット）

### Popup Design （ポップアップデザイン）
- **Type**: Email capture, lead magnet, etc. （**タイプ**: 電子メール キャプチャ、リード マグネットなど。）
- **Trigger**: When it appears （**トリガー**：出現時）
- **Targeting**: Who sees it （**ターゲティング**: 誰が見るか）
- **Frequency**: How often shown （**頻度**: 表示される頻度）
- **Copy**: Headline, subhead, CTA, decline （**コピー**: 見出し、小見出し、CTA、辞退）
- **Design notes**: Layout, imagery, mobile （**デザインノート**: レイアウト、画像、モバイル）

### Multiple Popup Strategy （複数のポップアップ戦略）
If recommending multiple popups: （複数のポップアップを推奨する場合:）
- Popup 1: [Purpose, trigger, audience] （ポップアップ 1: [目的、きっかけ、対象者]）
- Popup 2: [Purpose, trigger, audience] （ポップアップ 2: [目的、きっかけ、対象者]）
- Conflict rules: How they don't overlap （競合ルール: 重複しない方法）

### Test Hypotheses （仮説をテストする）
Ideas to A/B test with expected outcomes （期待される結果を伴う A/B テストのアイデア）

---

## Common Popup Strategies （一般的なポップアップ戦略）

### E-commerce （電子商取引）
1. Entry/scroll: First-purchase discount （エントリー/スクロール：初回購入割引）
2. Exit intent: Bigger discount or reminder （終了の意図: 大幅な割引またはリマインダー）
3. Cart abandonment: Complete your order （カートの放棄: 注文を完了します）

### B2B SaaS （B2B SaaS）
1. Click-triggered: Demo request, lead magnets （クリックトリガー: デモリクエスト、リードマグネット）
2. Scroll: Newsletter/blog subscription （スクロール: ニュースレター/ブログの購読）
3. Exit intent: Trial reminder or content offer （終了の目的: トライアルのリマインダーまたはコンテンツの提供）

### Content/Media （コンテンツ/メディア）
1. Scroll-based: Newsletter after engagement （スクロールベース: エンゲージメント後のニュースレター）
2. Page count: Subscribe after multiple visits （ページ数: 複数回アクセスした後に購読してください）
3. Exit intent: Don't miss future content （終了の意図: 今後のコンテンツをお見逃しなく）

### Lead Generation （リードジェネレーション）
1. Time-delayed: General list building （時間遅延: 一般的なリストの構築）
2. Click-triggered: Specific lead magnets （クリックトリガー: 特定のリードマグネット）
3. Exit intent: Final capture attempt （終了意図: 最後のキャプチャ試行）

---

## Experiment Ideas （実験のアイデア）

### Placement & Format Experiments （配置とフォーマットの実験）

**Banner Variations** （**バナーのバリエーション**）
- Top bar vs. banner below header （トップバーとヘッダー下のバナー）
- Sticky banner vs. static banner （粘着バナーと静的バナー）
- Full-width vs. contained banner （全幅バナーと含まれるバナー）
- Banner with countdown timer vs. without （カウントダウンタイマー付きのバナーとカウントダウンタイマーなしのバナー）

**Popup Formats** （**ポップアップ形式**）
- Center modal vs. slide-in from corner （センターモーダルとコーナーからのスライドイン）
- Full-screen overlay vs. smaller modal （全画面オーバーレイと小さなモーダルの比較）
- Bottom bar vs. corner popup （ボトムバーとコーナーポップアップの比較）
- Top announcements vs. bottom slideouts （上部のお知らせと下部のスライドアウト）

**Position Testing** （**ポジションテスト**）
- Test popup sizes on desktop and mobile （デスクトップとモバイルでポップアップ サイズをテストする）
- Left corner vs. right corner for slide-ins （スライドインの場合の左コーナーと右コーナー）
- Test visibility without blocking content （コンテンツをブロックせずに可視性をテストする）

---

### Trigger Experiments （トリガー実験）

**Timing Triggers** （**トリガーのタイミング**）
- Exit intent vs. 30-second delay vs. 50% scroll depth （終了意図 vs. 30 秒の遅延 vs. スクロール深さ 50%）
- Test optimal time delay (10s vs. 30s vs. 60s) （最適な遅延時間をテストする (10 秒 vs. 30 秒 vs. 60 秒)）
- Test scroll depth percentage (25% vs. 50% vs. 75%) （スクロールの深さのパーセンテージをテストします (25% 対 50% 対 75%)）
- Page count trigger (show after X pages viewed) （ページ数トリガー (X ページ閲覧後に表示)）

**Behavior Triggers** （**行動のトリガー**）
- Show based on user intent prediction （ユーザーの意図予測に基づいて表示する）
- Trigger based on specific page visits （特定のページの訪問に基づいてトリガー）
- Return visitor vs. new visitor targeting （再訪問者と新規訪問者のターゲティング）
- Show based on referral source （参照元に基づいて表示する）

**Click Triggers** （**クリックトリガー**）
- Click-triggered popups for lead magnets （リードマグネットのクリックトリガーポップアップ）
- Button-triggered vs. link-triggered modals （ボタントリガーモーダルとリンクトリガーモーダルの比較）
- Test in-content triggers vs. sidebar triggers （コンテンツ内トリガーとサイドバー トリガーをテストする）

---

### Messaging & Content Experiments （メッセージングとコンテンツの実験）

**Headlines & Copy** （**見出しとコピー**）
- Test attention-grabbing vs. informational headlines （注目を集める見出しと情報見出しをテストする）
- "Limited-time offer" vs. "New feature alert" messaging （「期間限定オファー」メッセージと「新機能アラート」メッセージ）
- Urgency-focused copy vs. value-focused copy （緊急性を重視したコピーと価値を重視したコピー）
- Test headline length and specificity （見出しの長さと具体性をテストする）

**CTAs** （**CTA**）
- CTA button text variations （CTA ボタンのテキストのバリエーション）
- Button color testing for contrast （ボタンの色のコントラストのテスト）
- Primary + secondary CTA vs. single CTA （プライマリ + セカンダリ CTA と単一 CTA の比較）
- Test decline text (friendly vs. neutral) （テスト拒否のテキスト (友好的または中立的)）

**Visual Content** （**ビジュアルコンテンツ**）
- Add countdown timers to create urgency （カウントダウンタイマーを追加して緊急性を高める）
- Test with/without images （画像あり/なしでテストする）
- Product preview vs. generic imagery （製品プレビューと一般的な画像の比較）
- Include social proof in popup （ポップアップに社会的証明を含める）

---

### Personalization Experiments （パーソナライゼーションの実験）

**Dynamic Content** （**動的コンテンツ**）
- Personalize popup based on visitor data （訪問者データに基づいてポップアップをパーソナライズする）
- Show industry-specific content （業界固有のコンテンツを表示する）
- Tailor content based on pages visited （訪問したページに基づいてコンテンツを調整する）
- Use progressive profiling (ask more over time) （プログレッシブプロファイリングを使用する (時間の経過とともにさらに質問する)）

**Audience Targeting** （**視聴者のターゲティング**）
- New vs. returning visitor messaging （新規訪問者と再訪問者のメッセージのやり取り）
- Segment by traffic source （トラフィックソースごとにセグメント化する）
- Target based on engagement level （エンゲージメントレベルに基づいた目標）
- Exclude already-converted visitors （すでにコンバージョンした訪問者を除外する）

---

### Frequency & Rules Experiments （頻度とルールの実験）

- Test frequency capping (once per session vs. once per week) （フリークエンシー キャップのテスト (セッションごとに 1 回、または週に 1 回)）
- Cool-down period after dismissal （解雇後のクールダウン期間）
- Test different dismiss behaviors （さまざまな拒否動作をテストする）
- Show escalating offers over multiple visits （複数の訪問にわたってエスカレートするオファーを表示する）

---

## Task-Specific Questions （タスク固有の質問）

1. What's the primary goal for this popup? （このポップアップの主な目的は何ですか?）
2. What's your current popup performance (if any)? （現在のポップアップのパフォーマンスはどのようなものですか (ある場合)。）
3. What traffic sources are you optimizing for? （どのようなトラフィック ソースを最適化していますか?）
4. What incentive can you offer? （どのようなインセンティブを提供できますか?）
5. Are there compliance requirements (GDPR, etc.)? （コンプライアンス要件（GDPRなど）はありますか?）
6. Mobile vs. desktop traffic split? （モバイルとデスクトップのトラフィックは分割されますか?）

---

## Related Skills （関連スキル）

- **form-cro**: For optimizing the form inside the popup （**form-cro**: ポップアップ内のフォームを最適化します。）
- **page-cro**: For the page context around popups （**page-cro**: ポップアップ周辺のページ コンテキスト用）
- **email-sequence**: For what happens after popup conversion （**email-sequence**: ポップアップ変換後の動作について）
- **ab-test-setup**: For testing popup variations （**ab-test-setup**: ポップアップのバリエーションをテストする場合）
