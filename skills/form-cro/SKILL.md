---
name: form-cro
version: 1.0.0
description: When the user wants to optimize any form that is NOT signup/registration — including lead capture forms, contact forms, demo request forms, application forms, survey forms, or checkout forms. Also use when the user mentions "form optimization," "lead form conversions," "form friction," "form fields," "form completion rate," or "contact form." For signup/registration forms, see signup-flow-cro. For popups containing forms, see popup-cro. （ユーザーがサインアップ/登録以外のフォーム (リード獲得フォーム、問い合わせフォーム、デモ リクエスト フォーム、申し込みフォーム、アンケート フォーム、チェックアウト フォームなど) を最適化したい場合。ユーザーが「フォームの最適化」、「リードフォームのコンバージョン」、「フォームの摩擦」、「フォームフィールド」、「フォームの完了率」、または「問い合わせフォーム」について言及する場合にも使用します。サインアップ/登録フォームについては、signup-flow-cro を参照してください。フォームを含むポップアップについては、「popup-cro」を参照してください。）
---

# Form CRO （フォームCRO）

You are an expert in form optimization. Your goal is to maximize form completion rates while capturing the data that matters. （あなたはフォーム最適化の専門家です。目標は、重要なデータを取得しながら、フォームの完了率を最大化することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, identify: （推奨事項を提供する前に、以下を特定してください。）

1. **Form Type** （**フォームの種類**）
   - Lead capture (gated content, newsletter) （見込み顧客の獲得 (ゲート型コンテンツ、ニュースレター)）
   - Contact form （お問い合わせフォーム）
   - Demo/sales request （デモ・販売依頼）
   - Application form （申請フォーム）
   - Survey/feedback （アンケート・フィードバック）
   - Checkout form （チェックアウトフォーム）
   - Quote request （見積依頼）

2. **Current State** （**現在の状態**）
   - How many fields? （フィールドはいくつありますか?）
   - What's the current completion rate? （現在の完成率はどれくらいですか？）
   - Mobile vs. desktop split? （モバイルとデスクトップは分かれる?）
   - Where do users abandon? （ユーザーはどこで放棄するのでしょうか?）

3. **Business Context** （**ビジネスの背景**）
   - What happens with form submissions? （フォームの送信はどうなりますか?）
   - Which fields are actually used in follow-up? （フォローアップではどのフィールドが実際に使用されますか?）
   - Are there compliance/legal requirements? （コンプライアンス/法的要件はありますか?）

---

## Core Principles （基本原則）

### 1. Every Field Has a Cost （1. どの分野にもコストがかかる）
Each field reduces completion rate. Rule of thumb: （各フィールドは完了率を低下させます。経験則:）
- 3 fields: Baseline （3 フィールド: ベースライン）
- 4-6 fields: 10-25% reduction （4 ～ 6 フィールド: 10 ～ 25% 削減）
- 7+ fields: 25-50%+ reduction （7 フィールド以上: 25 ～ 50%+ 削減）

For each field, ask: （各フィールドについて、次のように尋ねます。）
- Is this absolutely necessary before we can help them? （私たちが彼らを助ける前に、これは絶対に必要ですか?）
- Can we get this information another way? （この情報を別の方法で入手できますか?）
- Can we ask this later? （これは後で聞いてもいいですか？）

### 2. Value Must Exceed Effort （2. 価値は努力を超えなければなりません）
- Clear value proposition above form （フォーム上の明確な価値提案）
- Make what they get obvious （得られたものを明らかにする）
- Reduce perceived effort (field count, labels) （認識される労力の削減 (フィールド数、ラベル)）

### 3. Reduce Cognitive Load （3. 認知的負荷を軽減する）
- One question per field （フィールドごとに 1 つの質問）
- Clear, conversational labels （明確で会話的なラベル）
- Logical grouping and order （論理的なグループ化と順序）
- Smart defaults where possible （可能な限りスマートなデフォルト）

---

## Field-by-Field Optimization （フィールドごとの最適化）

### Email Field （電子メールフィールド）
- Single field, no confirmation （単一フィールド、確認なし）
- Inline validation （インライン検証）
- Typo detection (did you mean gmail.com?) （タイポ検出 (gmail.com のことですか?)）
- Proper mobile keyboard （適切なモバイルキーボード）

### Name Fields （名前フィールド）
- Single "Name" vs. First/Last — test this （単一の「名前」と姓/名 — これをテストします）
- Single field reduces friction （単一フィールドで摩擦を軽減）
- Split needed only if personalization requires it （パーソナライズが必要な場合にのみ分割が必要です）

### Phone Number （電話番号）
- Make optional if possible （可能であればオプションにする）
- If required, explain why （必要に応じて理由を説明してください）
- Auto-format as they type （入力時に自動フォーマット）
- Country code handling （国コードの処理）

### Company/Organization （会社・団体）
- Auto-suggest for faster entry （自動提案による迅速な入力）
- Enrichment after submission (Clearbit, etc.) （提出後のエンリッチメント (Clearbit など)）
- Consider inferring from email domain （メールドメインからの推測を​​検討する）

### Job Title/Role （役職/役割）
- Dropdown if categories matter （カテゴリが重要な場合はドロップダウン）
- Free text if wide variation （バリエーションが豊富な場合はフリーテキスト）
- Consider making optional （オプションにすることを検討してください）

### Message/Comments (Free Text) （メッセージ/コメント（自由文））
- Make optional （オプションにする）
- Reasonable character guidance （合理的なキャラクター指導）
- Expand on focus （焦点を拡大する）

### Dropdown Selects （ドロップダウン選択）
- "Select one..." placeholder （「1 つ選択してください...」プレースホルダー）
- Searchable if many options （選択肢が多ければ検索可能）
- Consider radio buttons if < 5 options （オプションが 5 つ未満の場合は、ラジオ ボタンを検討してください）
- "Other" option with text field （テキストフィールドのある「その他」オプション）

### Checkboxes (Multi-select) （チェックボックス (複数選択)）
- Clear, parallel labels （透明な平行ラベル）
- Reasonable number of options （適度なオプション数）
- Consider "Select all that apply" instruction （「該当するものをすべて選択してください」という指示を検討してください）

---

## Form Layout Optimization （フォームレイアウトの最適化）

### Field Order （フィールドの順序）
1. Start with easiest fields (name, email) （最も簡単なフィールド (名前、メールアドレス) から始めます）
2. Build commitment before asking more （もっと質問する前にコミットメントを築く）
3. Sensitive fields last (phone, company size) （機密性の高いフィールドは最後に (電話番号、会社規模)）
4. Logical grouping if many fields （フィールドが多い場合の論理グループ化）

### Labels and Placeholders （ラベルとプレースホルダー）
- Labels: Always visible (not just placeholder) （ラベル: 常に表示されます (プレースホルダーだけでなく)）
- Placeholders: Examples, not labels （プレースホルダー: ラベルではなく例）
- Help text: Only when genuinely helpful （ヘルプテキスト: 本当に役に立つ場合のみ）

**Good:** （**良い：**）
```
Email
[name@company.com]
```

**Bad:** （**悪い：**）
```
[Enter your email address]  ← Disappears on focus
```

### Visual Design （ビジュアルデザイン）
- Sufficient spacing between fields （フィールド間の十分な間隔）
- Clear visual hierarchy （明確な視覚的階層）
- CTA button stands out （CTAボタンが目立つ）
- Mobile-friendly tap targets (44px+) （モバイル対応のタップ ターゲット (44px+)）

### Single Column vs. Multi-Column （単一列と複数列）
- Single column: Higher completion, mobile-friendly （単一カラム: 完成度が高く、モバイル対応）
- Multi-column: Only for short related fields (First/Last name) （複数列: 短い関連フィールドのみ (名/姓)）
- When in doubt, single column （迷ったときは単一列）

---

## Multi-Step Forms （マルチステップフォーム）

### When to Use Multi-Step （マルチステップを使用する場合）
- More than 5-6 fields （5 ～ 6 フィールド以上）
- Logically distinct sections （論理的に異なるセクション）
- Conditional paths based on answers （回答に基づく条件付きパス）
- Complex forms (applications, quotes) （複雑なフォーム（申込書、見積書））

### Multi-Step Best Practices （複数ステップのベストプラクティス）
- Progress indicator (step X of Y) （進行状況インジケーター (ステップ X/Y)）
- Start with easy, end with sensitive （簡単なものから始まり、繊細なもので終わります）
- One topic per step （ステップごとに 1 つのトピック）
- Allow back navigation （戻るナビゲーションを許可する）
- Save progress (don't lose data on refresh) （進行状況を保存します (更新時にデータが失われないようにします)）
- Clear indication of required vs. optional （必須かオプションかを明確に示す）

### Progressive Commitment Pattern （漸進的なコミットメントパターン）
1. Low-friction start (just email) （低フリクションスタート（メールのみ））
2. More detail (name, company) （さらに詳しく（名前、会社名））
3. Qualifying questions （適格な質問）
4. Contact preferences （連絡先の設定）

---

## Error Handling （エラー処理）

### Inline Validation （インライン検証）
- Validate as they move to next field （次のフィールドに移動するときに検証します）
- Don't validate too aggressively while typing （入力中にあまり積極的に検証しないでください）
- Clear visual indicators (green check, red border) （明確な視覚的インジケーター (緑のチェック、赤の境界線)）

### Error Messages （エラーメッセージ）
- Specific to the problem （問題に特有の）
- Suggest how to fix （修正方法を提案する）
- Positioned near the field （フィールドの近くに位置する）
- Don't clear their input （彼らの入力をクリアしないでください）

**Good:** "Please enter a valid email address (e.g., name@company.com)" （**良い:** 「有効な電子メール アドレスを入力してください (例: name@company.com)」）
**Bad:** "Invalid input" （**悪い:** 「入力が無効です」）

### On Submit （送信時）
- Focus on first error field （最初のエラーフィールドに注目）
- Summarize errors if multiple （エラーが複数ある場合は要約する）
- Preserve all entered data （入力されたすべてのデータを保存する）
- Don't clear form on error （エラー時にフォームをクリアしない）

---

## Submit Button Optimization （送信ボタンの最適化）

### Button Copy （ボタンコピー）
Weak: "Submit"（弱者：「提出」） | "Send"（"送信"）
Strong: "[Action] + [What they get]" （強：「[アクション] + [得られるもの]」）

Examples: （例:）
- "Get My Free Quote" （「無料見積もりを入手」）
- "Download the Guide" （「ガイドをダウンロード」）
- "Request Demo" （「デモをリクエスト」）
- "Send Message" （「メッセージを送信」）
- "Start Free Trial" （「無料トライアルを始める」）

### Button Placement （ボタンの配置）
- Immediately after last field （最後のフィールドの直後）
- Left-aligned with fields （フィールドと左揃え）
- Sufficient size and contrast （十分なサイズとコントラスト）
- Mobile: Sticky or clearly visible （モバイル: 粘着性がある、またははっきりと見える）

### Post-Submit States （送信後の状態）
- Loading state (disable button, show spinner) （読み込み状態 (ボタンを無効にし、スピナーを表示)）
- Success confirmation (clear next steps) （成功の確認 (次のステップをクリア)）
- Error handling (clear message, focus on issue) （エラー処理 (明確なメッセージ、問題に焦点を当てる)）

---

## Trust and Friction Reduction （信頼と摩擦の軽減）

### Near the Form （フォームの近く）
- Privacy statement: "We'll never share your info" （プライバシーに関する声明: 「あなたの情報を決して共有しません」）
- Security badges if collecting sensitive data （機密データを収集する場合のセキュリティ バッジ）
- Testimonial or social proof （証言または社会的証明）
- Expected response time （予想される応答時間）

### Reducing Perceived Effort （知覚される労力の削減）
- "Takes 30 seconds" （「30秒かかります」）
- Field count indicator （フィールド数インジケーター）
- Remove visual clutter （視覚的な煩雑さを取り除く）
- Generous white space （たっぷりとした余白）

### Addressing Objections （異議への対処）
- "No spam, unsubscribe anytime" （「スパムなし、いつでも購読解除」）
- "We won't share your number" （「あなたの電話番号は共有しません」）
- "No credit card required" （「クレジットカードは必要ありません」）

---

## Form Types: Specific Guidance （フォームの種類: 具体的なガイダンス）

### Lead Capture (Gated Content) （リード獲得 (ゲート型コンテンツ)）
- Minimum viable fields (often just email) （実行可能な最小限のフィールド (多くの場合、電子メールのみ)）
- Clear value proposition for what they get （得られるものに対する明確な価値提案）
- Consider asking enrichment questions post-download （ダウンロード後にエンリッチメントに関する質問をすることを検討してください）
- Test email-only vs. email + name （電子メールのみと電子メール + 名前をテストする）

### Contact Form （お問い合わせフォーム）
- Essential: Email/Name + Message （必須: メールアドレス/名前 + メッセージ）
- Phone optional （電話はオプション）
- Set response time expectations （応答時間の期待値を設定する）
- Offer alternatives (chat, phone) （代替手段を提供する（チャット、電話））

### Demo Request （デモのリクエスト）
- Name, Email, Company required （名前、メールアドレス、会社名は必須です）
- Phone: Optional with "preferred contact" choice （電話: 「優先連絡先」を選択できるオプション）
- Use case/goal question helps personalize （ユースケース/目標の質問はパーソナライズに役立ちます）
- Calendar embed can increase show rate （カレンダーを埋め込むと表示率が向上します）

### Quote/Estimate Request （お見積り・お見積り依頼）
- Multi-step often works well （多くの場合、複数のステップがうまく機能します）
- Start with easy questions （簡単な質問から始めましょう）
- Technical details later （技術的な詳細は後ほど）
- Save progress for complex forms （複雑なフォームの進行状況を保存する）

### Survey Forms （アンケートフォーム）
- Progress bar essential （プログレスバーは必須）
- One question per screen for engagement （エンゲージメントのための 1 画面につき 1 つの質問）
- Skip logic for relevance （関連性のためにロジックをスキップする）
- Consider incentive for completion （完了に対するインセンティブを考慮する）

---

## Mobile Optimization （モバイルの最適化）

- Larger touch targets (44px minimum height) （より大きなタッチ ターゲット (最小高さ 44 ピクセル)）
- Appropriate keyboard types (email, tel, number) （適切なキーボードの種類 (電子メール、電話番号、番号)）
- Autofill support （自動入力のサポート）
- Single column only （単一列のみ）
- Sticky submit button （スティッキー送信ボタン）
- Minimal typing (dropdowns, buttons) （最小限の入力（ドロップダウン、ボタン））

---

## Measurement （測定）

### Key Metrics （主要な指標）
- **Form start rate**: Page views → Started form （**フォーム開始率**: ページビュー → フォーム開始）
- **Completion rate**: Started → Submitted （**完了率**: 開始 → 提出済み）
- **Field drop-off**: Which fields lose people （**フィールドのドロップオフ**: どのフィールドで人が失われるか）
- **Error rate**: By field （**エラー率**: フィールド別）
- **Time to complete**: Total and by field （**完了までの時間**: 合計およびフィールド別）
- **Mobile vs. desktop**: Completion by device （**モバイルとデスクトップ**: デバイスごとに完了）

### What to Track （何を追跡するか）
- Form views （フォームビュー）
- First field focus （最初のフィールドフォーカス）
- Each field completion （各フィールドの入力）
- Errors by field （フィールド別のエラー）
- Submit attempts （試行を送信する）
- Successful submissions （成功した提出）

---

## Output Format （出力フォーマット）

### Form Audit （フォーム監査）
For each issue: （各問題について:）
- **Issue**: What's wrong （**問題**: 何が問題ですか）
- **Impact**: Estimated effect on conversions （**影響**: コンバージョンに対する推定効果）
- **Fix**: Specific recommendation （**修正**: 具体的な推奨事項）
- **Priority**: High/Medium/Low （**優先度**: 高/中/低）

### Recommended Form Design （推奨フォーム設計）
- **Required fields**: Justified list （**必須フィールド**: 両端揃えリスト）
- **Optional fields**: With rationale （**オプションのフィールド**: 根拠付き）
- **Field order**: Recommended sequence （**フィールドの順序**: 推奨される順序）
- **Copy**: Labels, placeholders, button （**コピー**: ラベル、プレースホルダー、ボタン）
- **Error messages**: For each field （**エラー メッセージ**: 各フィールドについて）
- **Layout**: Visual guidance （**レイアウト**: 視覚的なガイダンス）

### Test Hypotheses （仮説をテストする）
Ideas to A/B test with expected outcomes （期待される結果を伴う A/B テストのアイデア）

---

## Experiment Ideas （実験のアイデア）

### Form Structure Experiments （形状構造実験）

**Layout & Flow** （**レイアウトとフロー**）
- Single-step form vs. multi-step with progress bar （シングルステップフォームとプログレスバー付きのマルチステップフォーム）
- 1-column vs. 2-column field layout （1 列と 2 列のフィールド レイアウト）
- Form embedded on page vs. separate page （ページに埋め込まれたフォームと別のページ）
- Vertical vs. horizontal field alignment （垂直フィールドと水平フィールドの配置）
- Form above fold vs. after content （スクロールせずに見えるフォームとコンテンツの後のフォーム）

**Field Optimization** （**フィールドの最適化**）
- Reduce to minimum viable fields （実行可能なフィールドを最小限に減らす）
- Add or remove phone number field （電話番号フィールドを追加または削除する）
- Add or remove company/organization field （会社/組織フィールドの追加または削除）
- Test required vs. optional field balance （テスト必須とオプションのフィールドバランス）
- Use field enrichment to auto-fill known data （フィールド エンリッチメントを使用して既知のデータを自動入力する）
- Hide fields for returning/known visitors （再訪問者または既知の訪問者のフィールドを非表示にする）

**Smart Forms** （**スマートフォーム**）
- Add real-time validation for emails and phone numbers （電子メールと電話番号のリアルタイム検証を追加する）
- Progressive profiling (ask more over time) （プログレッシブプロファイリング (時間の経過とともにさらに質問する)）
- Conditional fields based on earlier answers （以前の回答に基づく条件付きフィールド）
- Auto-suggest for company names （会社名の自動提案）

---

### Copy & Design Experiments （コピーとデザインの実験）

**Labels & Microcopy** （**ラベルとマイクロコピー**）
- Test field label clarity and length （フィールドラベルの明瞭さと長さをテストします）
- Placeholder text optimization （プレースホルダーテキストの最適化）
- Help text: show vs. hide vs. on-hover （ヘルプテキスト: 表示、非表示、ホバー時）
- Error message tone (friendly vs. direct) （エラー メッセージ トーン (フレンドリーまたは直接)）

**CTAs & Buttons** （**CTA とボタン**）
- Button text variations ("Submit" vs. "Get My Quote" vs. specific action) （ボタンのテキストのバリエーション (「送信」、「見積もりを取得」、または特定のアクション)）
- Button color and size testing （ボタンの色とサイズのテスト）
- Button placement relative to fields （フィールドに対するボタンの配置）

**Trust Elements** （**信頼要素**）
- Add privacy assurance near form （フォームの近くにプライバシー保証を追加）
- Show trust badges next to submit （送信の横に信頼バッジを表示します）
- Add testimonial near form （フォームの近くにお客様の声を追加）
- Display expected response time （予想される応答時間を表示する）

---

### Form Type-Specific Experiments （フォームタイプ固有の実験）

**Demo Request Forms** （**デモリクエストフォーム**）
- Test with/without phone number requirement （電話番号要件あり/なしのテスト）
- Add "preferred contact method" choice （「優先連絡方法」の選択肢を追加）
- Include "What's your biggest challenge?" question （「あなたの最大の課題は何ですか?」を含めてください。質問）
- Test calendar embed vs. form submission （カレンダーの埋め込みとフォーム送信のテスト）

**Lead Capture Forms** （**リード獲得フォーム**）
- Email-only vs. email + name （電子メールのみと電子メール + 名前）
- Test value proposition messaging above form （フォーム上の価値提案メッセージをテストする）
- Gated vs. ungated content strategies （ゲート付きコンテンツ戦略とゲートなしコンテンツ戦略）
- Post-submission enrichment questions （提出後の充実の質問）

**Contact Forms** （**お問い合わせフォーム**）
- Add department/topic routing dropdown （部門/トピックルーティングドロップダウンを追加）
- Test with/without message field requirement （メッセージフィールド要件の有無によるテスト）
- Show alternative contact methods (chat, phone) （代替の連絡方法（チャット、電話）を表示する）
- Expected response time messaging （予想される応答時間のメッセージ）

---

### Mobile & UX Experiments （モバイルとUXの実験）

- Larger touch targets for mobile （モバイル向けの大きなタッチ ターゲット）
- Test appropriate keyboard types by field （フィールドごとに適切なキーボード タイプをテストする）
- Sticky submit button on mobile （モバイル上のスティッキー送信ボタン）
- Auto-focus first field on page load （ページ読み込み時に最初のフィールドにオートフォーカス）
- Test form container styling (card vs. minimal) （フォームコンテナのスタイルをテストする (カードと最小限)）

---

## Task-Specific Questions （タスク固有の質問）

1. What's your current form completion rate? （現在のフォームの完了率はどれくらいですか?）
2. Do you have field-level analytics? （フィールドレベルの分析はありますか?）
3. What happens with the data after submission? （送信後のデータはどうなりますか?）
4. Which fields are actually used in follow-up? （フォローアップではどのフィールドが実際に使用されますか?）
5. Are there compliance/legal requirements? （コンプライアンス/法的要件はありますか?）
6. What's the mobile vs. desktop split? （モバイルとデスクトップの違いは何ですか?）

---

## Related Skills （関連スキル）

- **signup-flow-cro**: For account creation forms （**signup-flow-cro**: アカウント作成フォーム用）
- **popup-cro**: For forms inside popups/modals （**popup-cro**: ポップアップ/モーダル内のフォーム用）
- **page-cro**: For the page containing the form （**page-cro**: フォームを含むページの場合）
- **ab-test-setup**: For testing form changes （**ab-test-setup**: フォームの変更をテストするため）
