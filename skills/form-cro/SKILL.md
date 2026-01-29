---
name: form-cro
version: 1.0.0
description: When the user wants to optimize any form that is NOT signup/registration — including lead capture forms, contact forms, demo request forms, application forms, survey forms, or checkout forms. Also use when the user mentions "form optimization," "lead form conversions," "form friction," "form fields," "form completion rate," or "contact form." For signup/registration forms, see signup-flow-cro. For popups containing forms, see popup-cro. （日本語訳：ユーザーがサインアップ/登録以外のフォーム (リード獲得フォーム、問い合わせフォーム、デモ リクエスト フォーム、申し込みフォーム、アンケート フォーム、チェックアウト フォームなど) を最適化したい場合。ユーザーが「フォームの最適化」、「リードフォームのコンバージョン」、「フォームの摩擦」、「フォームフィールド」、「フォームの完了率」、または「問い合わせフォーム」について言及する場合にも使用します。サインアップ/登録フォームについては、signup-flow-cro を参照してください。フォームを含むポップアップについては、「popup-cro」を参照してください。）
---

# Form CRO （日本語訳：フォームCRO）

You are an expert in form optimization. Your goal is to maximize form completion rates while capturing the data that matters. （日本語訳：あなたはフォーム最適化の専門家です。目標は、重要なデータを取得しながら、フォームの完了率を最大化することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, identify: （日本語訳：推奨事項を提供する前に、以下を特定してください。）

1. **Form Type** （日本語訳：**フォームの種類**）
   - Lead capture (gated content, newsletter) （日本語訳：見込み顧客の獲得 (ゲート型コンテンツ、ニュースレター)）
   - Contact form （日本語訳：お問い合わせフォーム）
   - Demo/sales request （日本語訳：デモ・販売依頼）
   - Application form （日本語訳：申請フォーム）
   - Survey/feedback （日本語訳：アンケート・フィードバック）
   - Checkout form （日本語訳：チェックアウトフォーム）
   - Quote request （日本語訳：見積依頼）

2. **Current State** （日本語訳：**現在の状態**）
   - How many fields? （日本語訳：フィールドはいくつありますか?）
   - What's the current completion rate? （日本語訳：現在の完成率はどれくらいですか？）
   - Mobile vs. desktop split? （日本語訳：モバイルとデスクトップは分かれる?）
   - Where do users abandon? （日本語訳：ユーザーはどこで放棄するのでしょうか?）

3. **Business Context** （日本語訳：**ビジネスの背景**）
   - What happens with form submissions? （日本語訳：フォームの送信はどうなりますか?）
   - Which fields are actually used in follow-up? （日本語訳：フォローアップではどのフィールドが実際に使用されますか?）
   - Are there compliance/legal requirements? （日本語訳：コンプライアンス/法的要件はありますか?）

---

## Core Principles （日本語訳：基本原則）

### 1. Every Field Has a Cost （日本語訳：1. どの分野にもコストがかかる）
Each field reduces completion rate. Rule of thumb: （日本語訳：各フィールドは完了率を低下させます。経験則:）
- 3 fields: Baseline （日本語訳：3 フィールド: ベースライン）
- 4-6 fields: 10-25% reduction （日本語訳：4 ～ 6 フィールド: 10 ～ 25% 削減）
- 7+ fields: 25-50%+ reduction （日本語訳：7 フィールド以上: 25 ～ 50%+ 削減）

For each field, ask: （日本語訳：各フィールドについて、次のように尋ねます。）
- Is this absolutely necessary before we can help them? （日本語訳：私たちが彼らを助ける前に、これは絶対に必要ですか?）
- Can we get this information another way? （日本語訳：この情報を別の方法で入手できますか?）
- Can we ask this later? （日本語訳：これは後で聞いてもいいですか？）

### 2. Value Must Exceed Effort （日本語訳：2. 価値は努力を超えなければなりません）
- Clear value proposition above form （日本語訳：フォーム上の明確な価値提案）
- Make what they get obvious （日本語訳：得られたものを明らかにする）
- Reduce perceived effort (field count, labels) （日本語訳：認識される労力の削減 (フィールド数、ラベル)）

### 3. Reduce Cognitive Load （日本語訳：3. 認知的負荷を軽減する）
- One question per field （日本語訳：フィールドごとに 1 つの質問）
- Clear, conversational labels （日本語訳：明確で会話的なラベル）
- Logical grouping and order （日本語訳：論理的なグループ化と順序）
- Smart defaults where possible （日本語訳：可能な限りスマートなデフォルト）

---

## Field-by-Field Optimization （日本語訳：フィールドごとの最適化）

### Email Field （日本語訳：電子メールフィールド）
- Single field, no confirmation （日本語訳：単一フィールド、確認なし）
- Inline validation （日本語訳：インライン検証）
- Typo detection (did you mean gmail.com?) （日本語訳：タイポ検出 (gmail.com のことですか?)）
- Proper mobile keyboard （日本語訳：適切なモバイルキーボード）

### Name Fields （日本語訳：名前フィールド）
- Single "Name" vs. First/Last — test this （日本語訳：単一の「名前」と姓/名 — これをテストします）
- Single field reduces friction （日本語訳：単一フィールドで摩擦を軽減）
- Split needed only if personalization requires it （日本語訳：パーソナライズが必要な場合にのみ分割が必要です）

### Phone Number （日本語訳：電話番号）
- Make optional if possible （日本語訳：可能であればオプションにする）
- If required, explain why （日本語訳：必要に応じて理由を説明してください）
- Auto-format as they type （日本語訳：入力時に自動フォーマット）
- Country code handling （日本語訳：国コードの処理）

### Company/Organization （日本語訳：会社・団体）
- Auto-suggest for faster entry （日本語訳：自動提案による迅速な入力）
- Enrichment after submission (Clearbit, etc.) （日本語訳：提出後のエンリッチメント (Clearbit など)）
- Consider inferring from email domain （日本語訳：メールドメインからの推測を​​検討する）

### Job Title/Role （日本語訳：役職/役割）
- Dropdown if categories matter （日本語訳：カテゴリが重要な場合はドロップダウン）
- Free text if wide variation （日本語訳：バリエーションが豊富な場合はフリーテキスト）
- Consider making optional （日本語訳：オプションにすることを検討してください）

### Message/Comments (Free Text) （日本語訳：メッセージ/コメント（自由文））
- Make optional （日本語訳：オプションにする）
- Reasonable character guidance （日本語訳：合理的なキャラクター指導）
- Expand on focus （日本語訳：焦点を拡大する）

### Dropdown Selects （日本語訳：ドロップダウン選択）
- "Select one..." placeholder （日本語訳：「1 つ選択してください...」プレースホルダー）
- Searchable if many options （日本語訳：選択肢が多ければ検索可能）
- Consider radio buttons if < 5 options （日本語訳：オプションが 5 つ未満の場合は、ラジオ ボタンを検討してください）
- "Other" option with text field （日本語訳：テキストフィールドのある「その他」オプション）

### Checkboxes (Multi-select) （日本語訳：チェックボックス (複数選択)）
- Clear, parallel labels （日本語訳：透明な平行ラベル）
- Reasonable number of options （日本語訳：適度なオプション数）
- Consider "Select all that apply" instruction （日本語訳：「該当するものをすべて選択してください」という指示を検討してください）

---

## Form Layout Optimization （日本語訳：フォームレイアウトの最適化）

### Field Order （日本語訳：フィールドの順序）
1. Start with easiest fields (name, email) （日本語訳：最も簡単なフィールド (名前、メールアドレス) から始めます）
2. Build commitment before asking more （日本語訳：もっと質問する前にコミットメントを築く）
3. Sensitive fields last (phone, company size) （日本語訳：機密性の高いフィールドは最後に (電話番号、会社規模)）
4. Logical grouping if many fields （日本語訳：フィールドが多い場合の論理グループ化）

### Labels and Placeholders （日本語訳：ラベルとプレースホルダー）
- Labels: Always visible (not just placeholder) （日本語訳：ラベル: 常に表示されます (プレースホルダーだけでなく)）
- Placeholders: Examples, not labels （日本語訳：プレースホルダー: ラベルではなく例）
- Help text: Only when genuinely helpful （日本語訳：ヘルプテキスト: 本当に役に立つ場合のみ）

**Good:** （日本語訳：**良い：**）
```
Email
[name@company.com]
```

**Bad:** （日本語訳：**悪い：**）
```
[Enter your email address]  ← Disappears on focus
```

### Visual Design （日本語訳：ビジュアルデザイン）
- Sufficient spacing between fields （日本語訳：フィールド間の十分な間隔）
- Clear visual hierarchy （日本語訳：明確な視覚的階層）
- CTA button stands out （日本語訳：CTAボタンが目立つ）
- Mobile-friendly tap targets (44px+) （日本語訳：モバイル対応のタップ ターゲット (44px+)）

### Single Column vs. Multi-Column （日本語訳：単一列と複数列）
- Single column: Higher completion, mobile-friendly （日本語訳：単一カラム: 完成度が高く、モバイル対応）
- Multi-column: Only for short related fields (First/Last name) （日本語訳：複数列: 短い関連フィールドのみ (名/姓)）
- When in doubt, single column （日本語訳：迷ったときは単一列）

---

## Multi-Step Forms （日本語訳：マルチステップフォーム）

### When to Use Multi-Step （日本語訳：マルチステップを使用する場合）
- More than 5-6 fields （日本語訳：5 ～ 6 フィールド以上）
- Logically distinct sections （日本語訳：論理的に異なるセクション）
- Conditional paths based on answers （日本語訳：回答に基づく条件付きパス）
- Complex forms (applications, quotes) （日本語訳：複雑なフォーム（申込書、見積書））

### Multi-Step Best Practices （日本語訳：複数ステップのベストプラクティス）
- Progress indicator (step X of Y) （日本語訳：進行状況インジケーター (ステップ X/Y)）
- Start with easy, end with sensitive （日本語訳：簡単なものから始まり、繊細なもので終わります）
- One topic per step （日本語訳：ステップごとに 1 つのトピック）
- Allow back navigation （日本語訳：戻るナビゲーションを許可する）
- Save progress (don't lose data on refresh) （日本語訳：進行状況を保存します (更新時にデータが失われないようにします)）
- Clear indication of required vs. optional （日本語訳：必須かオプションかを明確に示す）

### Progressive Commitment Pattern （日本語訳：漸進的なコミットメントパターン）
1. Low-friction start (just email) （日本語訳：低フリクションスタート（メールのみ））
2. More detail (name, company) （日本語訳：さらに詳しく（名前、会社名））
3. Qualifying questions （日本語訳：適格な質問）
4. Contact preferences （日本語訳：連絡先の設定）

---

## Error Handling （日本語訳：エラー処理）

### Inline Validation （日本語訳：インライン検証）
- Validate as they move to next field （日本語訳：次のフィールドに移動するときに検証します）
- Don't validate too aggressively while typing （日本語訳：入力中にあまり積極的に検証しないでください）
- Clear visual indicators (green check, red border) （日本語訳：明確な視覚的インジケーター (緑のチェック、赤の境界線)）

### Error Messages （日本語訳：エラーメッセージ）
- Specific to the problem （日本語訳：問題に特有の）
- Suggest how to fix （日本語訳：修正方法を提案する）
- Positioned near the field （日本語訳：フィールドの近くに位置する）
- Don't clear their input （日本語訳：彼らの入力をクリアしないでください）

**Good:** "Please enter a valid email address (e.g., name@company.com)" （日本語訳：**良い:** 「有効な電子メール アドレスを入力してください (例: name@company.com)」）
**Bad:** "Invalid input" （日本語訳：**悪い:** 「入力が無効です」）

### On Submit （日本語訳：送信時）
- Focus on first error field （日本語訳：最初のエラーフィールドに注目）
- Summarize errors if multiple （日本語訳：エラーが複数ある場合は要約する）
- Preserve all entered data （日本語訳：入力されたすべてのデータを保存する）
- Don't clear form on error （日本語訳：エラー時にフォームをクリアしない）

---

## Submit Button Optimization （日本語訳：送信ボタンの最適化）

### Button Copy （日本語訳：ボタンコピー）
Weak: "Submit"（日本語訳：弱者：「提出」） | "Send"（日本語訳："送信"）
Strong: "[Action] + [What they get]" （日本語訳：強：「[アクション] + [得られるもの]」）

Examples: （日本語訳：例:）
- "Get My Free Quote" （日本語訳：「無料見積もりを入手」）
- "Download the Guide" （日本語訳：「ガイドをダウンロード」）
- "Request Demo" （日本語訳：「デモをリクエスト」）
- "Send Message" （日本語訳：「メッセージを送信」）
- "Start Free Trial" （日本語訳：「無料トライアルを始める」）

### Button Placement （日本語訳：ボタンの配置）
- Immediately after last field （日本語訳：最後のフィールドの直後）
- Left-aligned with fields （日本語訳：フィールドと左揃え）
- Sufficient size and contrast （日本語訳：十分なサイズとコントラスト）
- Mobile: Sticky or clearly visible （日本語訳：モバイル: 粘着性がある、またははっきりと見える）

### Post-Submit States （日本語訳：送信後の状態）
- Loading state (disable button, show spinner) （日本語訳：読み込み状態 (ボタンを無効にし、スピナーを表示)）
- Success confirmation (clear next steps) （日本語訳：成功の確認 (次のステップをクリア)）
- Error handling (clear message, focus on issue) （日本語訳：エラー処理 (明確なメッセージ、問題に焦点を当てる)）

---

## Trust and Friction Reduction （日本語訳：信頼と摩擦の軽減）

### Near the Form （日本語訳：フォームの近く）
- Privacy statement: "We'll never share your info" （日本語訳：プライバシーに関する声明: 「あなたの情報を決して共有しません」）
- Security badges if collecting sensitive data （日本語訳：機密データを収集する場合のセキュリティ バッジ）
- Testimonial or social proof （日本語訳：証言または社会的証明）
- Expected response time （日本語訳：予想される応答時間）

### Reducing Perceived Effort （日本語訳：知覚される労力の削減）
- "Takes 30 seconds" （日本語訳：「30秒かかります」）
- Field count indicator （日本語訳：フィールド数インジケーター）
- Remove visual clutter （日本語訳：視覚的な煩雑さを取り除く）
- Generous white space （日本語訳：たっぷりとした余白）

### Addressing Objections （日本語訳：異議への対処）
- "No spam, unsubscribe anytime" （日本語訳：「スパムなし、いつでも購読解除」）
- "We won't share your number" （日本語訳：「あなたの電話番号は共有しません」）
- "No credit card required" （日本語訳：「クレジットカードは必要ありません」）

---

## Form Types: Specific Guidance （日本語訳：フォームの種類: 具体的なガイダンス）

### Lead Capture (Gated Content) （日本語訳：リード獲得 (ゲート型コンテンツ)）
- Minimum viable fields (often just email) （日本語訳：実行可能な最小限のフィールド (多くの場合、電子メールのみ)）
- Clear value proposition for what they get （日本語訳：得られるものに対する明確な価値提案）
- Consider asking enrichment questions post-download （日本語訳：ダウンロード後にエンリッチメントに関する質問をすることを検討してください）
- Test email-only vs. email + name （日本語訳：電子メールのみと電子メール + 名前をテストする）

### Contact Form （日本語訳：お問い合わせフォーム）
- Essential: Email/Name + Message （日本語訳：必須: メールアドレス/名前 + メッセージ）
- Phone optional （日本語訳：電話はオプション）
- Set response time expectations （日本語訳：応答時間の期待値を設定する）
- Offer alternatives (chat, phone) （日本語訳：代替手段を提供する（チャット、電話））

### Demo Request （日本語訳：デモのリクエスト）
- Name, Email, Company required （日本語訳：名前、メールアドレス、会社名は必須です）
- Phone: Optional with "preferred contact" choice （日本語訳：電話: 「優先連絡先」を選択できるオプション）
- Use case/goal question helps personalize （日本語訳：ユースケース/目標の質問はパーソナライズに役立ちます）
- Calendar embed can increase show rate （日本語訳：カレンダーを埋め込むと表示率が向上します）

### Quote/Estimate Request （日本語訳：お見積り・お見積り依頼）
- Multi-step often works well （日本語訳：多くの場合、複数のステップがうまく機能します）
- Start with easy questions （日本語訳：簡単な質問から始めましょう）
- Technical details later （日本語訳：技術的な詳細は後ほど）
- Save progress for complex forms （日本語訳：複雑なフォームの進行状況を保存する）

### Survey Forms （日本語訳：アンケートフォーム）
- Progress bar essential （日本語訳：プログレスバーは必須）
- One question per screen for engagement （日本語訳：エンゲージメントのための 1 画面につき 1 つの質問）
- Skip logic for relevance （日本語訳：関連性のためにロジックをスキップする）
- Consider incentive for completion （日本語訳：完了に対するインセンティブを考慮する）

---

## Mobile Optimization （日本語訳：モバイルの最適化）

- Larger touch targets (44px minimum height) （日本語訳：より大きなタッチ ターゲット (最小高さ 44 ピクセル)）
- Appropriate keyboard types (email, tel, number) （日本語訳：適切なキーボードの種類 (電子メール、電話番号、番号)）
- Autofill support （日本語訳：自動入力のサポート）
- Single column only （日本語訳：単一列のみ）
- Sticky submit button （日本語訳：スティッキー送信ボタン）
- Minimal typing (dropdowns, buttons) （日本語訳：最小限の入力（ドロップダウン、ボタン））

---

## Measurement （日本語訳：測定）

### Key Metrics （日本語訳：主要な指標）
- **Form start rate**: Page views → Started form （日本語訳：**フォーム開始率**: ページビュー → フォーム開始）
- **Completion rate**: Started → Submitted （日本語訳：**完了率**: 開始 → 提出済み）
- **Field drop-off**: Which fields lose people （日本語訳：**フィールドのドロップオフ**: どのフィールドで人が失われるか）
- **Error rate**: By field （日本語訳：**エラー率**: フィールド別）
- **Time to complete**: Total and by field （日本語訳：**完了までの時間**: 合計およびフィールド別）
- **Mobile vs. desktop**: Completion by device （日本語訳：**モバイルとデスクトップ**: デバイスごとに完了）

### What to Track （日本語訳：何を追跡するか）
- Form views （日本語訳：フォームビュー）
- First field focus （日本語訳：最初のフィールドフォーカス）
- Each field completion （日本語訳：各フィールドの入力）
- Errors by field （日本語訳：フィールド別のエラー）
- Submit attempts （日本語訳：試行を送信する）
- Successful submissions （日本語訳：成功した提出）

---

## Output Format （日本語訳：出力フォーマット）

### Form Audit （日本語訳：フォーム監査）
For each issue: （日本語訳：各問題について:）
- **Issue**: What's wrong （日本語訳：**問題**: 何が問題ですか）
- **Impact**: Estimated effect on conversions （日本語訳：**影響**: コンバージョンに対する推定効果）
- **Fix**: Specific recommendation （日本語訳：**修正**: 具体的な推奨事項）
- **Priority**: High/Medium/Low （日本語訳：**優先度**: 高/中/低）

### Recommended Form Design （日本語訳：推奨フォーム設計）
- **Required fields**: Justified list （日本語訳：**必須フィールド**: 両端揃えリスト）
- **Optional fields**: With rationale （日本語訳：**オプションのフィールド**: 根拠付き）
- **Field order**: Recommended sequence （日本語訳：**フィールドの順序**: 推奨される順序）
- **Copy**: Labels, placeholders, button （日本語訳：**コピー**: ラベル、プレースホルダー、ボタン）
- **Error messages**: For each field （日本語訳：**エラー メッセージ**: 各フィールドについて）
- **Layout**: Visual guidance （日本語訳：**レイアウト**: 視覚的なガイダンス）

### Test Hypotheses （日本語訳：仮説をテストする）
Ideas to A/B test with expected outcomes （日本語訳：期待される結果を伴う A/B テストのアイデア）

---

## Experiment Ideas （日本語訳：実験のアイデア）

### Form Structure Experiments （日本語訳：形状構造実験）

**Layout & Flow** （日本語訳：**レイアウトとフロー**）
- Single-step form vs. multi-step with progress bar （日本語訳：シングルステップフォームとプログレスバー付きのマルチステップフォーム）
- 1-column vs. 2-column field layout （日本語訳：1 列と 2 列のフィールド レイアウト）
- Form embedded on page vs. separate page （日本語訳：ページに埋め込まれたフォームと別のページ）
- Vertical vs. horizontal field alignment （日本語訳：垂直フィールドと水平フィールドの配置）
- Form above fold vs. after content （日本語訳：スクロールせずに見えるフォームとコンテンツの後のフォーム）

**Field Optimization** （日本語訳：**フィールドの最適化**）
- Reduce to minimum viable fields （日本語訳：実行可能なフィールドを最小限に減らす）
- Add or remove phone number field （日本語訳：電話番号フィールドを追加または削除する）
- Add or remove company/organization field （日本語訳：会社/組織フィールドの追加または削除）
- Test required vs. optional field balance （日本語訳：テスト必須とオプションのフィールドバランス）
- Use field enrichment to auto-fill known data （日本語訳：フィールド エンリッチメントを使用して既知のデータを自動入力する）
- Hide fields for returning/known visitors （日本語訳：再訪問者または既知の訪問者のフィールドを非表示にする）

**Smart Forms** （日本語訳：**スマートフォーム**）
- Add real-time validation for emails and phone numbers （日本語訳：電子メールと電話番号のリアルタイム検証を追加する）
- Progressive profiling (ask more over time) （日本語訳：プログレッシブプロファイリング (時間の経過とともにさらに質問する)）
- Conditional fields based on earlier answers （日本語訳：以前の回答に基づく条件付きフィールド）
- Auto-suggest for company names （日本語訳：会社名の自動提案）

---

### Copy & Design Experiments （日本語訳：コピーとデザインの実験）

**Labels & Microcopy** （日本語訳：**ラベルとマイクロコピー**）
- Test field label clarity and length （日本語訳：フィールドラベルの明瞭さと長さをテストします）
- Placeholder text optimization （日本語訳：プレースホルダーテキストの最適化）
- Help text: show vs. hide vs. on-hover （日本語訳：ヘルプテキスト: 表示、非表示、ホバー時）
- Error message tone (friendly vs. direct) （日本語訳：エラー メッセージ トーン (フレンドリーまたは直接)）

**CTAs & Buttons** （日本語訳：**CTA とボタン**）
- Button text variations ("Submit" vs. "Get My Quote" vs. specific action) （日本語訳：ボタンのテキストのバリエーション (「送信」、「見積もりを取得」、または特定のアクション)）
- Button color and size testing （日本語訳：ボタンの色とサイズのテスト）
- Button placement relative to fields （日本語訳：フィールドに対するボタンの配置）

**Trust Elements** （日本語訳：**信頼要素**）
- Add privacy assurance near form （日本語訳：フォームの近くにプライバシー保証を追加）
- Show trust badges next to submit （日本語訳：送信の横に信頼バッジを表示します）
- Add testimonial near form （日本語訳：フォームの近くにお客様の声を追加）
- Display expected response time （日本語訳：予想される応答時間を表示する）

---

### Form Type-Specific Experiments （日本語訳：フォームタイプ固有の実験）

**Demo Request Forms** （日本語訳：**デモリクエストフォーム**）
- Test with/without phone number requirement （日本語訳：電話番号要件あり/なしのテスト）
- Add "preferred contact method" choice （日本語訳：「優先連絡方法」の選択肢を追加）
- Include "What's your biggest challenge?" question （日本語訳：「あなたの最大の課題は何ですか?」を含めてください。質問）
- Test calendar embed vs. form submission （日本語訳：カレンダーの埋め込みとフォーム送信のテスト）

**Lead Capture Forms** （日本語訳：**リード獲得フォーム**）
- Email-only vs. email + name （日本語訳：電子メールのみと電子メール + 名前）
- Test value proposition messaging above form （日本語訳：フォーム上の価値提案メッセージをテストする）
- Gated vs. ungated content strategies （日本語訳：ゲート付きコンテンツ戦略とゲートなしコンテンツ戦略）
- Post-submission enrichment questions （日本語訳：提出後の充実の質問）

**Contact Forms** （日本語訳：**お問い合わせフォーム**）
- Add department/topic routing dropdown （日本語訳：部門/トピックルーティングドロップダウンを追加）
- Test with/without message field requirement （日本語訳：メッセージフィールド要件の有無によるテスト）
- Show alternative contact methods (chat, phone) （日本語訳：代替の連絡方法（チャット、電話）を表示する）
- Expected response time messaging （日本語訳：予想される応答時間のメッセージ）

---

### Mobile & UX Experiments （日本語訳：モバイルとUXの実験）

- Larger touch targets for mobile （日本語訳：モバイル向けの大きなタッチ ターゲット）
- Test appropriate keyboard types by field （日本語訳：フィールドごとに適切なキーボード タイプをテストする）
- Sticky submit button on mobile （日本語訳：モバイル上のスティッキー送信ボタン）
- Auto-focus first field on page load （日本語訳：ページ読み込み時に最初のフィールドにオートフォーカス）
- Test form container styling (card vs. minimal) （日本語訳：フォームコンテナのスタイルをテストする (カードと最小限)）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What's your current form completion rate? （日本語訳：現在のフォームの完了率はどれくらいですか?）
2. Do you have field-level analytics? （日本語訳：フィールドレベルの分析はありますか?）
3. What happens with the data after submission? （日本語訳：送信後のデータはどうなりますか?）
4. Which fields are actually used in follow-up? （日本語訳：フォローアップではどのフィールドが実際に使用されますか?）
5. Are there compliance/legal requirements? （日本語訳：コンプライアンス/法的要件はありますか?）
6. What's the mobile vs. desktop split? （日本語訳：モバイルとデスクトップの違いは何ですか?）

---

## Related Skills （日本語訳：関連スキル）

- **signup-flow-cro**: For account creation forms （日本語訳：**signup-flow-cro**: アカウント作成フォーム用）
- **popup-cro**: For forms inside popups/modals （日本語訳：**popup-cro**: ポップアップ/モーダル内のフォーム用）
- **page-cro**: For the page containing the form （日本語訳：**page-cro**: フォームを含むページの場合）
- **ab-test-setup**: For testing form changes （日本語訳：**ab-test-setup**: フォームの変更をテストするため）
