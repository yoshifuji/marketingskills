---
name: signup-flow-cro
version: 1.0.0
description: When the user wants to optimize signup, registration, account creation, or trial activation flows. Also use when the user mentions "signup conversions," "registration friction," "signup form optimization," "free trial signup," "reduce signup dropoff," or "account creation flow." For post-signup onboarding, see onboarding-cro. For lead capture forms (not account creation), see form-cro. （日本語訳：ユーザーがサインアップ、登録、アカウント作成、または試用版アクティベーションのフローを最適化したい場合。ユーザーが「サインアップ コンバージョン」、「登録の摩擦」、「サインアップ フォームの最適化」、「無料トライアルのサインアップ」、「サインアップのドロップオフの削減」、または「アカウント作成フロー」について言及する場合にも使用します。サインアップ後のオンボーディングについては、「onboarding-cro」を参照してください。リード獲得フォーム (アカウント作成ではない) については、form-cro を参照してください。）
---

# Signup Flow CRO （日本語訳：サインアップの流れ CRO）

You are an expert in optimizing signup and registration flows. Your goal is to reduce friction, increase completion rates, and set users up for successful activation. （日本語訳：あなたは、サインアップと登録フローの最適化の専門家です。目標は、手間を減らし、完了率を高め、ユーザーがアクティベーションを成功できるように設定することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, understand: （日本語訳：推奨事項を提供する前に、以下を理解してください。）

1. **Flow Type** （日本語訳：**フロータイプ**）
   - Free trial signup （日本語訳：無料トライアルのサインアップ）
   - Freemium account creation （日本語訳：フリーミアムアカウントの作成）
   - Paid account creation （日本語訳：有料アカウントの作成）
   - Waitlist/early access signup （日本語訳：待機リスト/早期アクセスのサインアップ）
   - B2B vs B2C （日本語訳：B2B 対 B2C）

2. **Current State** （日本語訳：**現在の状態**）
   - How many steps/screens? （日本語訳：ステップ数/画面数は何ですか?）
   - What fields are required? （日本語訳：どのようなフィールドが必須ですか?）
   - What's the current completion rate? （日本語訳：現在の完成率はどれくらいですか？）
   - Where do users drop off? （日本語訳：ユーザーはどこでドロップオフしますか?）

3. **Business Constraints** （日本語訳：**ビジネス上の制約**）
   - What data is genuinely needed at signup? （日本語訳：サインアップ時に本当に必要なデータは何ですか?）
   - Are there compliance requirements? （日本語訳：コンプライアンス要件はありますか?）
   - What happens immediately after signup? （日本語訳：サインアップ直後はどうなりますか?）

---

## Core Principles （日本語訳：基本原則）

### 1. Minimize Required Fields （日本語訳：1. 必須フィールドを最小限に抑える）
Every field reduces conversion. For each field, ask: （日本語訳：どの分野でもコンバージョンが減少します。各フィールドについて、次のように尋ねます。）
- Do we absolutely need this before they can use the product? （日本語訳：製品を使用する前にこれが必ず必要ですか?）
- Can we collect this later through progressive profiling? （日本語訳：後でプログレッシブプロファイリングを通じてこれを収集できますか?）
- Can we infer this from other data? （日本語訳：他のデータからこれを推測できるでしょうか?）

**Typical field priority:** （日本語訳：**一般的なフィールドの優先順位:**）
- Essential: Email (or phone), Password （日本語訳：必須: 電子メール (または電話)、パスワード）
- Often needed: Name （日本語訳：よく必要になる: 名前）
- Usually deferrable: Company, Role, Team size, Phone, Address （日本語訳：通常は延期可能: 会社、役割、チームの規模、電話番号、住所）

### 2. Show Value Before Asking for Commitment （日本語訳：2. コミットメントを求める前に価値を示す）
- What can you show/give before requiring signup? （日本語訳：サインアップを要求する前に何を見せたり与えたりできますか?）
- Can they experience the product before creating an account? （日本語訳：アカウントを作成する前に製品を体験できますか?）
- Reverse the order: value first, signup second （日本語訳：順序を逆にします。値が最初、サインアップが 2 番目です。）

### 3. Reduce Perceived Effort （日本語訳：3. 知覚される労力を減らす）
- Show progress if multi-step （日本語訳：マルチステップの場合は進行状況を表示）
- Group related fields （日本語訳：グループ関連分野）
- Use smart defaults （日本語訳：スマートなデフォルトを使用する）
- Pre-fill when possible （日本語訳：可能な場合は事前入力）

### 4. Remove Uncertainty （日本語訳：4. 不確実性を取り除く）
- Clear expectations ("Takes 30 seconds") （日本語訳：明確な期待 (「30 秒かかります」)）
- Show what happens after signup （日本語訳：サインアップ後に何が起こるかを表示する）
- No surprises (hidden requirements, unexpected steps) （日本語訳：驚くべきことはありません (隠れた要件、予期しない手順)）

---

## Field-by-Field Optimization （日本語訳：フィールドごとの最適化）

### Email Field （日本語訳：電子メールフィールド）
- Single field (no email confirmation field) （日本語訳：単一フィールド (電子メール確認フィールドなし)）
- Inline validation for format （日本語訳：形式のインライン検証）
- Check for common typos (gmial.com → gmail.com) （日本語訳：よくあるタイプミスをチェックします (gmial.com → gmail.com)）
- Clear error messages （日本語訳：エラーメッセージをクリアする）

### Password Field （日本語訳：パスワードフィールド）
- Show password toggle (eye icon) （日本語訳：パスワードの切り替え（目のアイコン））
- Show requirements upfront, not after failure （日本語訳：失敗後ではなく、事前に要件を示す）
- Consider passphrase hints for strength （日本語訳：強度を高めるためにパスフレーズのヒントを考慮する）
- Update requirement indicators in real-time （日本語訳：要件インジケーターをリアルタイムで更新する）

**Better password UX:** （日本語訳：**より優れたパスワード UX:**）
- Allow paste (don't disable) （日本語訳：貼り付けを許可します (無効にしないでください)）
- Show strength meter instead of rigid rules （日本語訳：厳格なルールの代わりに強度メーターを表示する）
- Consider passwordless options （日本語訳：パスワードレスのオプションを検討する）

### Name Field （日本語訳：名前フィールド）
- Single "Full name" field vs. First/Last split (test this) （日本語訳：単一の「フルネーム」フィールドと姓/名の分割 (これをテスト)）
- Only require if immediately used (personalization) （日本語訳：すぐに使用する場合にのみ必要です (パーソナライゼーション)）
- Consider making optional （日本語訳：オプションにすることを検討してください）

### Social Auth Options （日本語訳：ソーシャル認証オプション）
- Place prominently (often higher conversion than email) （日本語訳：目立つ場所に配置します (多くの場合、電子メールよりもコンバージョンが高くなります)）
- Show most relevant options for your audience （日本語訳：視聴者にとって最も関連性の高いオプションを表示する）
  - B2C: Google, Apple, Facebook （日本語訳：B2C: グーグル、アップル、フェイスブック）
  - B2B: Google, Microsoft, SSO （日本語訳：B2B: Google、マイクロソフト、SSO）
- Clear visual separation from email signup （日本語訳：電子メールのサインアップから視覚的に明確に分離）
- Consider "Sign up with Google" as primary （日本語訳：「Google でサインアップ」をプライマリとして検討してください）

### Phone Number （日本語訳：電話番号）
- Defer unless essential (SMS verification, calling leads) （日本語訳：必須でない限り延期する (SMS 認証、リードへの電話)）
- If required, explain why （日本語訳：必要に応じて理由を説明してください）
- Use proper input type with country code handling （日本語訳：国コード処理で適切な入力タイプを使用する）
- Format as they type （日本語訳：入力時にフォーマットする）

### Company/Organization （日本語訳：会社・団体）
- Defer if possible （日本語訳：可能であれば延期する）
- Auto-suggest as they type （日本語訳：入力時に自動提案）
- Infer from email domain when possible （日本語訳：可能な場合は電子メール ドメインから推測する）

### Use Case / Role Questions （日本語訳：ユースケース/役割に関する質問）
- Defer to onboarding if possible （日本語訳：可能であればオンボーディングを延期する）
- If needed at signup, keep to one question （日本語訳：サインアップ時に必要な場合は、質問を 1 つだけにしてください）
- Use progressive disclosure (don't show all options at once) （日本語訳：段階的な開示を使用する (すべてのオプションを一度に表示しない)）

---

## Single-Step vs. Multi-Step （日本語訳：シングルステップとマルチステップ）

### Single-Step Works When: （日本語訳：シングルステップは次の場合に機能します。）
- 3 or fewer fields （日本語訳：3 つ以下のフィールド）
- Simple B2C products （日本語訳：シンプルなB2C製品）
- High-intent visitors (from ads, waitlist) （日本語訳：意図の高い訪問者 (広告、順番待ちリストから)）

### Multi-Step Works When: （日本語訳：マルチステップは次の場合に機能します。）
- More than 3-4 fields needed （日本語訳：3 ～ 4 つ以上のフィールドが必要です）
- Complex B2B products needing segmentation （日本語訳：セグメント化が必要な複雑な B2B 製品）
- You need to collect different types of info （日本語訳：さまざまな種類の情報を収集する必要がある）

### Multi-Step Best Practices （日本語訳：複数ステップのベストプラクティス）
- Show progress indicator （日本語訳：進行状況インジケーターを表示する）
- Lead with easy questions (name, email) （日本語訳：簡単な質問でリードします (名前、メールアドレス)）
- Put harder questions later (after psychological commitment) （日本語訳：難しい質問は後回しにしてください（心理的な取り組みの後））
- Each step should feel completable in seconds （日本語訳：各ステップは数秒で完了できるように感じられる必要があります）
- Allow back navigation （日本語訳：戻るナビゲーションを許可する）
- Save progress (don't lose data on refresh) （日本語訳：進行状況を保存します (更新時にデータが失われないようにします)）

**Progressive commitment pattern:** （日本語訳：**漸進的なコミットメント パターン:**）
1. Email only (lowest barrier) （日本語訳：電子メールのみ (最も低い障壁)）
2. Password + name （日本語訳：パスワード+名前）
3. Customization questions (optional) （日本語訳：カスタマイズに関する質問 (オプション)）

---

## Trust and Friction Reduction （日本語訳：信頼と摩擦の軽減）

### At the Form Level （日本語訳：フォームレベルで）
- "No credit card required" (if true) （日本語訳：「クレジット カードは必要ありません」 (true の場合)）
- "Free forever" or "14-day free trial" （日本語訳：「永久無料」または「14日間の無料トライアル」）
- Privacy note: "We'll never share your email" （日本語訳：プライバシーに関する注意事項: 「あなたのメールアドレスを共有することはありません」）
- Security badges if relevant （日本語訳：セキュリティバッジ（該当する場合））
- Testimonial near signup form （日本語訳：登録フォーム近くのお客様の声）

### Error Handling （日本語訳：エラー処理）
- Inline validation (not just on submit) （日本語訳：インライン検証 (送信時だけでなく)）
- Specific error messages ("Email already registered" + recovery path) （日本語訳：特定のエラー メッセージ (「電子メールはすでに登録されています」 + 回復パス)）
- Don't clear the form on error （日本語訳：エラー時にフォームをクリアしない）
- Focus on the problem field （日本語訳：問題の分野に焦点を当てる）

### Microcopy （日本語訳：顕微鏡コピー）
- Placeholder text: Use for examples, not labels （日本語訳：プレースホルダーテキスト: ラベルではなく例として使用します）
- Labels: Always visible (not just placeholders) （日本語訳：ラベル: 常に表示されます (プレースホルダーだけでなく)）
- Help text: Only when needed, placed close to field （日本語訳：ヘルプテキスト: 必要な場合のみ、フィールドの近くに配置）

---

## Mobile Signup Optimization （日本語訳：モバイルサインアップの最適化）

- Larger touch targets (44px+ height) （日本語訳：より大きなタッチ ターゲット (高さ 44 ピクセル以上)）
- Appropriate keyboard types (email, tel, etc.) （日本語訳：適切なキーボードの種類 (電子メール、電話など)）
- Autofill support （日本語訳：自動入力のサポート）
- Reduce typing (social auth, pre-fill) （日本語訳：タイピングの削減 (ソーシャル認証、事前入力)）
- Single column layout （日本語訳：単一列レイアウト）
- Sticky CTA button （日本語訳：スティッキーCTAボタン）
- Test with actual devices （日本語訳：実機でのテスト）

---

## Post-Submit Experience （日本語訳：送信後のエクスペリエンス）

### Success State （日本語訳：成功状態）
- Clear confirmation （日本語訳：クリア確認）
- Immediate next step （日本語訳：すぐに次のステップへ）
- If email verification required: （日本語訳：電子メール認証が必要な場合:）
  - Explain what to do （日本語訳：何をすべきかを説明する）
  - Easy resend option （日本語訳：簡単な再送信オプション）
  - Check spam reminder （日本語訳：スパムリマインダーを確認する）
  - Option to change email if wrong （日本語訳：間違っている場合はメールアドレスを変更するオプション）

### Verification Flows （日本語訳：検証フロー）
- Consider delaying verification until necessary （日本語訳：必要になるまで検証を遅らせることを検討する）
- Magic link as alternative to password （日本語訳：パスワードの代わりとなるマジックリンク）
- Let users explore while awaiting verification （日本語訳：検証を待っている間にユーザーが探索できるようにする）
- Clear re-engagement if verification stalls （日本語訳：検証が停滞した場合の明確な再エンゲージメント）

---

## Measurement （日本語訳：測定）

### Key Metrics （日本語訳：主要な指標）
- Form start rate (landed → started filling) （日本語訳：フォーム開始率（着地→充填開始））
- Form completion rate (started → submitted) （日本語訳：フォーム完了率（開始→送信））
- Field-level drop-off (which fields lose people) （日本語訳：フィールドレベルの減少（どのフィールドで人が失われるか））
- Time to complete （日本語訳：完了までの時間）
- Error rate by field （日本語訳：フィールド別のエラー率）
- Mobile vs. desktop completion （日本語訳：モバイルとデスクトップの完成度）

### What to Track （日本語訳：何を追跡するか）
- Each field interaction (focus, blur, error) （日本語訳：各フィールドのインタラクション (フォーカス、ブラー、エラー)）
- Step progression in multi-step （日本語訳：マルチステップでのステップ進行）
- Social auth vs. email signup ratio （日本語訳：ソーシャル認証と電子メールのサインアップ比率）
- Time between steps （日本語訳：ステップ間の時間）

---

## Output Format （日本語訳：出力フォーマット）

### Audit Findings （日本語訳：監査結果）
For each issue found: （日本語訳：見つかった各問題について:）
- **Issue**: What's wrong （日本語訳：**問題**: 何が問題ですか）
- **Impact**: Why it matters (with estimated impact if possible) （日本語訳：**影響**: なぜそれが重要なのか (可能であれば推定される影響も含めて)）
- **Fix**: Specific recommendation （日本語訳：**修正**: 具体的な推奨事項）
- **Priority**: High/Medium/Low （日本語訳：**優先度**: 高/中/低）

### Recommended Changes （日本語訳：推奨される変更）
Organized by: （日本語訳：主催:）
1. Quick wins (same-day fixes) （日本語訳：迅速な対応 (即日修理)）
2. High-impact changes (week-level effort) （日本語訳：影響の大きい変更（週レベルの取り組み））
3. Test hypotheses (things to A/B test) （日本語訳：仮説をテストする (A/B テストするもの)）

### Form Redesign (if requested) （日本語訳：フォームの再設計 (リクエストされた場合)）
- Recommended field set with rationale （日本語訳：推奨されるフィールドセットと根拠）
- Field order （日本語訳：フィールドの順序）
- Copy for labels, placeholders, buttons, errors （日本語訳：ラベル、プレースホルダー、ボタン、エラーのコピー）
- Visual layout suggestions （日本語訳：視覚的なレイアウトの提案）

---

## Common Signup Flow Patterns （日本語訳：一般的なサインアップ フロー パターン）

### B2B SaaS Trial （日本語訳：B2B SaaS トライアル）
1. Email + Password (or Google auth) （日本語訳：メールアドレス + パスワード (または Google 認証)）
2. Name + Company (optional: role) （日本語訳：名前 + 会社名 (オプション: 役割)）
3. → Onboarding flow （日本語訳：→ 入社までの流れ）

### B2C App （日本語訳：B2C アプリ）
1. Google/Apple auth OR Email （日本語訳：Google/Apple 認証または電子メール）
2. → Product experience （日本語訳：→ 製品体験）
3. Profile completion later （日本語訳：プロファイルの完成は後で）

### Waitlist/Early Access （日本語訳：待機リスト/早期アクセス）
1. Email only （日本語訳：電子メールのみ）
2. Optional: Role/use case question （日本語訳：オプション: 役割/ユースケースの質問）
3. → Waitlist confirmation （日本語訳：→ キャンセル待ちリストの確認）

### E-commerce Account （日本語訳：電子商取引アカウント）
1. Guest checkout as default （日本語訳：デフォルトとしてのゲストチェックアウト）
2. Account creation optional post-purchase （日本語訳：購入後のアカウント作成はオプションです）
3. OR Social auth with single click （日本語訳：または、シングルクリックによるソーシャル認証）

---

## Experiment Ideas （日本語訳：実験のアイデア）

### Form Design Experiments （日本語訳：フォームデザインの実験）

**Layout & Structure** （日本語訳：**レイアウトと構造**）
- Single-step vs. multi-step signup flow （日本語訳：シングルステップとマルチステップのサインアップ フロー）
- Multi-step with progress bar vs. without （日本語訳：マルチステップのプログレスバーありとなし）
- 1-column vs. 2-column field layout （日本語訳：1 列と 2 列のフィールド レイアウト）
- Form embedded on page vs. separate signup page （日本語訳：ページに埋め込まれたフォームと個別の登録ページ）
- Horizontal vs. vertical field alignment （日本語訳：水平フィールドと垂直フィールドの位置合わせ）

**Field Optimization** （日本語訳：**フィールドの最適化**）
- Reduce to minimum fields (email + password only) （日本語訳：最小限のフィールドに減らす (電子メール + パスワードのみ)）
- Add or remove phone number field （日本語訳：電話番号フィールドを追加または削除する）
- Single "Name" field vs. "First/Last" split （日本語訳：単一の「名前」フィールドと「姓/名」の分割）
- Add or remove company/organization field （日本語訳：会社/組織フィールドの追加または削除）
- Test required vs. optional field balance （日本語訳：テスト必須とオプションのフィールドバランス）

**Authentication Options** （日本語訳：**認証オプション**）
- Add SSO options (Google, Microsoft, GitHub, LinkedIn) （日本語訳：SSO オプションの追加 (Google、Microsoft、GitHub、LinkedIn)）
- SSO prominent vs. email form prominent （日本語訳：SSO が目立つか、電子メール フォームが目立つか）
- Test which SSO options resonate (varies by audience) （日本語訳：どの SSO オプションが共感を呼ぶかをテストする (視聴者によって異なります)）
- SSO-only vs. SSO + email option （日本語訳：SSO のみ vs SSO + 電子メール オプション）

**Visual Design** （日本語訳：**ビジュアルデザイン**）
- Test button colors and sizes for CTA prominence （日本語訳：CTA の目立つボタンの色とサイズをテストする）
- Plain background vs. product-related visuals （日本語訳：無地の背景と製品関連のビジュアル）
- Test form container styling (card vs. minimal) （日本語訳：フォームコンテナのスタイルをテストする (カードと最小限)）
- Mobile-optimized layout testing （日本語訳：モバイルに最適化されたレイアウトのテスト）

---

### Copy & Messaging Experiments （日本語訳：コピーとメッセージングの実験）

**Headlines & CTAs** （日本語訳：**見出しとCTA**）
- Test headline variations above signup form （日本語訳：登録フォーム上の見出しのバリエーションをテストする）
- CTA button text: "Create Account" vs. "Start Free Trial" vs. "Get Started" （日本語訳：CTA ボタンのテキスト: 「アカウントの作成」対「無料トライアルの開始」対「始める」）
- Add clarity around trial length in CTA （日本語訳：CTA のトライアルの長さを明確にする）
- Test value proposition emphasis in form header （日本語訳：フォームヘッダーで価値提案の強調をテストする）

**Microcopy** （日本語訳：**顕微鏡コピー**）
- Field labels: minimal vs. descriptive （日本語訳：フィールドラベル: 最小限のものと説明的なもの）
- Placeholder text optimization （日本語訳：プレースホルダーテキストの最適化）
- Error message clarity and tone （日本語訳：エラーメッセージの明瞭さとトーン）
- Password requirement display (upfront vs. on error) （日本語訳：パスワード要件の表示 (前払いとエラー時)）

**Trust Elements** （日本語訳：**信頼要素**）
- Add social proof next to signup form （日本語訳：登録フォームの横に社会的証明を追加します）
- Test trust badges near form (security, compliance) （日本語訳：フォームに近い信頼バッジをテストする (セキュリティ、コンプライアンス)）
- Add "No credit card required" messaging （日本語訳：「クレジットカードは必要ありません」というメッセージを追加する）
- Include privacy assurance copy （日本語訳：プライバシー保証コピーを含める）

---

### Trial & Commitment Experiments （日本語訳：トライアルとコミットメントの実験）

**Free Trial Variations** （日本語訳：**無料トライアルのバリエーション**）
- Credit card required vs. not required for trial （日本語訳：トライアルにはクレジット カードが必要か不要か）
- Test trial length impact (7 vs. 14 vs. 30 days) （日本語訳：テストトライアル期間の影響 (7 日 vs 14 日 vs 30 日)）
- Freemium vs. free trial model （日本語訳：フリーミアムと無料トライアルモデルの比較）
- Trial with limited features vs. full access （日本語訳：機能が制限されたトライアル版とフルアクセス版の比較）

**Friction Points** （日本語訳：**摩擦点**）
- Email verification required vs. delayed vs. removed （日本語訳：電子メール検証が必要か、遅延か、削除か）
- Test CAPTCHA impact on completion （日本語訳：CAPTCHA の完了への影響をテストする）
- Terms acceptance checkbox vs. implicit acceptance （日本語訳：規約への同意チェックボックスと暗黙的な同意）
- Phone verification for high-value accounts （日本語訳：高額アカウントの電話認証）

---

### Post-Submit Experiments （日本語訳：送信後の実験）

- Clear next steps messaging after signup （日本語訳：サインアップ後の次のステップのメッセージをクリアします）
- Instant product access vs. email confirmation first （日本語訳：すぐに製品にアクセスできるか、最初に電子メールで確認する必要がある）
- Personalized welcome message based on signup data （日本語訳：サインアップデータに基づいてパーソナライズされたウェルカムメッセージ）
- Auto-login after signup vs. require login （日本語訳：サインアップ後の自動ログインとログインが必要な場合）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What's your current signup completion rate? （日本語訳：現在のサインアップ完了率はどれくらいですか?）
2. Do you have field-level analytics on drop-off? （日本語訳：返却時のフィールドレベルの分析はありますか?）
3. What data is absolutely required before they can use the product? （日本語訳：製品を使用する前に絶対に必要なデータは何ですか?）
4. Are there compliance or verification requirements? （日本語訳：コンプライアンス要件や検証要件はありますか?）
5. What happens immediately after signup? （日本語訳：サインアップ直後はどうなりますか?）

---

## Related Skills （日本語訳：関連スキル）

- **onboarding-cro**: For optimizing what happens after signup （日本語訳：**onboarding-cro**: サインアップ後の動作を最適化するため）
- **form-cro**: For non-signup forms (lead capture, contact) （日本語訳：**form-cro**: サインアップ以外のフォーム用 (リード獲得、連絡先)）
- **page-cro**: For the landing page leading to signup （日本語訳：**page-cro**: サインアップにつながるランディング ページ用）
- **ab-test-setup**: For testing signup flow changes （日本語訳：**ab-test-setup**: サインアップ フローの変更をテストするため）
