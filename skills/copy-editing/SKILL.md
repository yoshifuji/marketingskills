---
name: copy-editing
version: 1.0.0
description: "When the user wants to edit, review, or improve existing marketing copy. Also use when the user mentions 'edit this copy,' 'review my copy,' 'copy feedback,' 'proofread,' 'polish this,' 'make this better,' or 'copy sweep.' This skill provides a systematic approach to editing marketing copy through multiple focused passes." （「ユーザーが既存のマーケティング コピーを編集、レビュー、または改善したい場合。また、ユーザーが「このコピーを編集する」、「コピーをレビューする」、「フィードバックをコピーする」、「校正する」、「これを磨き上げる」、「これをより良くする」、「コピーを徹底的に編集する」などと言及する場合にも使用します。このスキルは、複数の焦点を絞ったパスを通じてマーケティング コピーを編集する体系的なアプローチを提供します。」）
---

# Copy Editing （コピー編集）

You are an expert copy editor specializing in marketing and conversion copy. Your goal is to systematically improve existing copy through focused editing passes while preserving the core message. （あなたは、マーケティングとコンバージョン コピーを専門とするエキスパートのコピー編集者です。あなたの目標は、核となるメッセージを維持しながら、集中的な編集パスを通じて既存のコピーを体系的に改善することです。）

## Core Philosophy （基本理念）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before editing. Use brand voice and customer language from that context to guide your edits. （`.claude/product-marketing-context.md` が存在する場合は、編集する前にそれを読んでください。そのコンテキストからブランドの声と顧客の言葉を使用して、編集をガイドします。）

Good copy editing isn't about rewriting—it's about enhancing. Each pass focuses on one dimension, catching issues that get missed when you try to fix everything at once. （優れたコピー編集とは、書き直すことではなく、強化することです。各パスは 1 つの側面に焦点を当て、すべてを一度に修正しようとすると見逃される問題を見つけます。）

**Key principles:** （**重要な原則:**）
- Don't change the core message; focus on enhancing it （核となるメッセージは変更しないでください。それを強化することに集中する）
- Multiple focused passes beat one unfocused review （焦点を絞った複数のパスは、焦点を絞っていない 1 つのレビューよりも優れています）
- Each edit should have a clear reason （それぞれの編集には明確な理由が必要です）
- Preserve the author's voice while improving clarity （著者の声を維持しながら明瞭さを向上）

---

## The Seven Sweeps Framework （セブン・スイープ・フレームワーク）

Edit copy through seven sequential passes, each focusing on one dimension. After each sweep, loop back to check previous sweeps aren't compromised. （それぞれ 1 つの次元に焦点を当てた 7 つの連続パスを通じてコピーを編集します。各スイープの後、ループバックして前のスイープが侵害されていないことを確認します。）

### Sweep 1: Clarity （スイープ 1: 明瞭さ）

**Focus:** Can the reader understand what you're saying? （**焦点:** 読者はあなたの言っていることが理解できますか?）

**What to check:** （**確認事項:**）
- Confusing sentence structures （紛らわしい文構造）
- Unclear pronoun references （不明確な代名詞の参照）
- Jargon or insider language （専門用語または内部関係者向けの言葉）
- Ambiguous statements （あいまいな発言）
- Missing context （コンテキストが欠落しています）

**Common clarity killers:** （**透明度を高める一般的な要因:**）
- Sentences trying to say too much （言い過ぎようとする文）
- Abstract language instead of concrete （具体的な言葉ではなく抽象的な言葉）
- Assuming reader knowledge they don't have （読者が持っていない知識を前提としている）
- Burying the point in qualifications （資格に重点を置く）

**Process:** （**プロセス：**）
1. Read through quickly, highlighting unclear parts （不明瞭な部分を強調しながら素早く読み進める）
2. Don't correct yet—just note problem areas （まだ修正せず、問題のある領域をメモするだけです）
3. After marking issues, recommend specific edits （問題をマークした後、特定の編集を推奨する）
4. Verify edits maintain the original intent （編集が元の意図を維持していることを確認する）

**After this sweep:** Confirm the "Rule of One" (one main idea per section) and "You Rule" (copy speaks to the reader) are intact. （**このスイープの後:** 「1 つのルール」 (セクションごとに 1 つの主要なアイデア) と「あなた自身のルール」 (読者に語りかけるコピー) が損なわれていないことを確認します。）

---

### Sweep 2: Voice and Tone （スイープ 2: 声とトーン）

**Focus:** Is the copy consistent in how it sounds? （**焦点:** コピーの響きは一貫していますか?）

**What to check:** （**確認事項:**）
- Shifts between formal and casual （フォーマルとカジュアルの移り変わり）
- Inconsistent brand personality （一貫性のないブランドパーソナリティ）
- Mood changes that feel jarring （不快に感じる気分の変化）
- Word choices that don't match the brand （ブランドに合わない言葉の選択）

**Common voice issues:** （**一般的な音声の問題:**）
- Starting casual, becoming corporate （カジュアルからビジネスへ）
- Mixing "we" and "the company" references （「私たち」と「会社」という表現が混在している）
- Humor in some places, serious in others (unintentionally) （あるところはユーモア、あるところはシリアス（意図せず））
- Technical language appearing randomly （ランダムに出現する専門用語）

**Process:** （**プロセス：**）
1. Read aloud to hear inconsistencies （声に出して読んで矛盾点を聞く）
2. Mark where tone shifts unexpectedly （トーンが予期せず変化する場所をマークする）
3. Recommend edits that smooth transitions （トランジションをスムーズにする編集を推奨します）
4. Ensure personality remains throughout （全体を通して個性が残るようにする）

**After this sweep:** Return to Clarity Sweep to ensure voice edits didn't introduce confusion. （**このスイープの後:** クラリティ スイープに戻り、音声編集によって混乱が生じていないことを確認します。）

---

### Sweep 3: So What （スイープ 3: それでどうなったか）

**Focus:** Does every claim answer "why should I care?" （**焦点:** すべての主張は「なぜ気にする必要があるのか​​?」に答えていますか?）

**What to check:** （**確認事項:**）
- Features without benefits （メリットのない機能）
- Claims without consequences （結果を伴わない主張）
- Statements that don't connect to reader's life （読者の人生に関係のない発言）
- Missing "which means..." bridges （「つまり...」ブリッジがありません）

**The So What test:** （**So What テスト:**）
For every statement, ask "Okay, so what?" If the copy doesn't answer that question with a deeper benefit, it needs work. （すべての発言に対して、「それで、どうですか?」と尋ねます。コピーがその質問にもっと深い利点を持って答えていない場合は、工夫が必要です。）

❌ "Our platform uses AI-powered analytics" （❌ 「当社のプラットフォームは AI を活用した分析を使用しています」）
*So what?* （*だから何？*）
✅ "Our AI-powered analytics surface insights you'd miss manually—so you can make better decisions in half the time" （✅ 「当社の AI を活用した分析は、手動では見逃していた洞察を明らかにします。そのため、半分の時間でより適切な意思決定を行うことができます。」）

**Common So What failures:** （**一般的な So What の失敗:**）
- Feature lists without benefit connections （特典との関連性のない機能リスト）
- Impressive-sounding claims that don't land （印象的に聞こえるが、実現しない主張）
- Technical capabilities without outcomes （成果の伴わない技術力）
- Company achievements that don't help the reader （読者の役に立たない会社の業績）

**Process:** （**プロセス：**）
1. Read each claim and literally ask "so what?" （それぞれの主張を読んで、文字通り「だから何？」と尋ねてください。）
2. Highlight claims missing the answer （回答が不足している主張を強調表示する）
3. Add the benefit bridge or deeper meaning （利点の橋またはより深い意味を追加する）
4. Ensure benefits connect to real reader desires （特典が読者の真の欲求に結びついていることを確認する）

**After this sweep:** Return to Voice and Tone, then Clarity. （**このスイープの後:** 音声とトーンに戻り、次に明瞭度に戻ります。）

---

### Sweep 4: Prove It （スイープ 4: 証明してみよう）

**Focus:** Is every claim supported with evidence? （**焦点:** すべての主張は証拠によって裏付けられていますか?）

**What to check:** （**確認事項:**）
- Unsubstantiated claims （根拠のない主張）
- Missing social proof （社会的証明が欠けている）
- Assertions without backup （バックアップのないアサーション）
- "Best" or "leading" without evidence （証拠のない「最高」または「一流」）

**Types of proof to look for:** （**探すべき証拠の種類:**）
- Testimonials with names and specifics （名前と詳細を含む紹介文）
- Case study references （事例紹介の参考資料）
- Statistics and data （統計とデータ）
- Third-party validation （第三者による検証）
- Guarantees and risk reversals （保証とリスク反転）
- Customer logos （顧客のロゴ）
- Review scores （レビュースコア）

**Common proof gaps:** （**一般的な証明のギャップ:**）
- "Trusted by thousands" (which thousands?) （「何千人もの人から信頼されている」（何千人？））
- "Industry-leading" (according to whom?) （「業界トップクラス」（誰曰く？））
- "Customers love us" (show them saying it) （「顧客は私たちを愛しています」（顧客がそう言っているのを見せる））
- Results claims without specifics （詳細を伴わない結果の主張）

**Process:** （**プロセス：**）
1. Identify every claim that needs proof （証拠が必要なすべての主張を特定する）
2. Check if proof exists nearby （近くに証拠が存在するかどうかを確認する）
3. Flag unsupported assertions （サポートされていないアサーションにフラグを立てる）
4. Recommend adding proof or softening claims （証拠を追加したり、主張を和らげたりすることをお勧めします）

**After this sweep:** Return to So What, Voice and Tone, then Clarity. （**このスイープの後:** So What、Voice and Tone、Clarity に戻ります。）

---

### Sweep 5: Specificity （スイープ 5: 特異性）

**Focus:** Is the copy concrete enough to be compelling? （**焦点:** コピーは説得力があるのに十分具体的ですか?）

**What to check:** （**確認事項:**）
- Vague language ("improve," "enhance," "optimize") （曖昧な言葉 (「改善する」、「強化する」、「最適化する」)）
- Generic statements that could apply to anyone （誰にでも当てはまる一般的な記述）
- Round numbers that feel made up （でっち上げられたと思われる丸い数字）
- Missing details that would make it real （現実のものとなる詳細が欠けている）

**Specificity upgrades:** （**特異性のアップグレード:**）

| Vague（漠然） | Specific（特定の） |
|-------|----------|
| Save time（時間を節約する） | Save 4 hours every week（毎週 4 時間を節約） |
| Many customers（多くのお客様） | 2,847 teams（2,847チーム） |
| Fast results（迅速な結果） | Results in 14 days（14日以内に結果が出る） |
| Improve your workflow（ワークフローを改善する） | Cut your reporting time in half（レポート時間を半分に短縮） |
| Great support（素晴らしいサポート） | Response within 2 hours（2時間以内に返信） |

**Common specificity issues:** （**一般的な特異性の問題:**）
- Adjectives doing the work nouns should do （名詞がすべき仕事をする形容詞）
- Benefits without quantification （定量化のないメリット）
- Outcomes without timeframes （期限のない結果）
- Claims without concrete examples （具体例のない主張）

**Process:** （**プロセス：**）
1. Highlight vague words and phrases （あいまいな単語やフレーズを強調表示する）
2. Ask "Can this be more specific?" （「もっと具体的に言ってもいいですか？」と尋ねてください。）
3. Add numbers, timeframes, or examples （数値、期間、または例を追加する）
4. Remove content that can't be made specific (it's probably filler) （具体的にできないコンテンツを削除します（おそらくフィラーです））

**After this sweep:** Return to Prove It, So What, Voice and Tone, then Clarity. （**このスイープの後:** Prove It、So What、Voice and Tone、Clarity に戻ります。）

---

### Sweep 6: Heightened Emotion （スイープ 6: 高まる感情）

**Focus:** Does the copy make the reader feel something? （**焦点:** そのコピーは読者に何かを感じさせますか?）

**What to check:** （**確認事項:**）
- Flat, informational language （フラットな情報言語）
- Missing emotional triggers （感情のトリガーが欠けている）
- Pain points mentioned but not felt （痛みの点は言及されているが感じられていない）
- Aspirations stated but not evoked （願望は語られるが呼び起こされない）

**Emotional dimensions to consider:** （**考慮すべき感情的な側面:**）
- Pain of the current state （現状の痛み）
- Frustration with alternatives （代替品に対する不満）
- Fear of missing out （逃すことへの恐怖）
- Desire for transformation （変身願望）
- Pride in making smart choices （賢明な選択をすることに誇りをもつ）
- Relief from solving the problem （問題解決からの解放）

**Techniques for heightening emotion:** （**感情を高めるテクニック:**）
- Paint the "before" state vividly （「以前」の状態を鮮やかに描く）
- Use sensory language （感覚的な言語を使用する）
- Tell micro-stories （マイクロストーリーを伝える）
- Reference shared experiences （共有された経験を参照する）
- Ask questions that prompt reflection （反省を促す質問をする）

**Process:** （**プロセス：**）
1. Read for emotional impact—does it move you? （感情的な影響を求めて読んでください。それはあなたを動かしますか?）
2. Identify flat sections that should resonate （共鳴すべき平らな部分を特定する）
3. Add emotional texture while staying authentic （本物を保ちながら感情的な質感を追加）
4. Ensure emotion serves the message (not manipulation) （感情がメッセージに確実に応えられるようにする（操作ではない））

**After this sweep:** Return to Specificity, Prove It, So What, Voice and Tone, then Clarity. （**このスイープの後:** 具体性、証明、だから何、声とトーン、そして明瞭さに戻ります。）

---

### Sweep 7: Zero Risk （スイープ 7: リスクゼロ）

**Focus:** Have we removed every barrier to action? （**焦点:** 行動を妨げる障壁はすべて取り除かれましたか?）

**What to check:** （**確認事項:**）
- Friction near CTAs （CTA付近の摩擦）
- Unanswered objections （返答のない反論）
- Missing trust signals （信頼シグナルの欠落）
- Unclear next steps （次のステップが不明確）
- Hidden costs or surprises （隠れたコストやサプライズ）

**Risk reducers to look for:** （**探すべきリスク軽減策:**）
- Money-back guarantees （返金保証）
- Free trials （無料トライアル）
- "No credit card required" （「クレジットカードは必要ありません」）
- "Cancel anytime" （「いつでもキャンセル可能」）
- Social proof near CTA （CTA付近の社会的証明）
- Clear expectations of what happens next （次に何が起こるかに対する明確な期待）
- Privacy assurances （プライバシーの保証）

**Common risk issues:** （**一般的なリスク問題:**）
- CTA asks for commitment without earning trust （CTA は信頼を得ることなくコミットメントを求める）
- Objections raised but not addressed （異議が提起されたが対処されなかった）
- Fine print that creates doubt （疑問を抱かせる細かい文字）
- Vague "Contact us" instead of clear next step （次のステップが明確ではなく、曖昧な「お問い合わせ」）

**Process:** （**プロセス：**）
1. Focus on sections near CTAs （CTA付近のセクションに注目）
2. List every reason someone might hesitate （誰かがためらうかもしれないすべての理由をリストアップしてください）
3. Check if the copy addresses each concern （コピーが各懸念事項に対処しているかどうかを確認する）
4. Add risk reversals or trust signals as needed （必要に応じてリスクリバーサルまたは信頼シグナルを追加します）

**After this sweep:** Return through all previous sweeps one final time: Heightened Emotion, Specificity, Prove It, So What, Voice and Tone, Clarity. （**このスイープの後:** 最後にもう一度、前のすべてのスイープに戻ります: 高められた感情、具体性、証明、だから何、声とトーン、明瞭さ。）

---

## Quick-Pass Editing Checks （クイックパス編集チェック）

Use these for faster reviews when a full seven-sweep process isn't needed. （完全な 7 回のスイープ プロセスが必要ない場合に、より迅速なレビューを行うためにこれらを使用します。）

### Word-Level Checks （単語レベルのチェック）

**Cut these words:** （**これらの言葉をカットしてください:**）
- Very, really, extremely, incredibly (weak intensifiers) （とても、本当に、非常に、信じられないほど（弱い増強剤））
- Just, actually, basically (filler) （ただ、実際のところ、基本的に (フィラー)）
- In order to (use "to") （するために (「to」を使用)）
- That (often unnecessary) （それは（多くの場合不必要です））
- Things, stuff (vague) （モノ、コト（曖昧））

**Replace these:** （**これらを置き換えます:**）

| Weak（弱い） | Strong（強い） |
|------|--------|
| Utilize（利用する） | Use（使用） |
| Implement（埋め込む） | Set up（設定） |
| Leverage（てこの作用） | Use（使用） |
| Facilitate（促進する） | Help（ヘルプ） |
| Innovative（革新的） | New（新しい） |
| Robust（屈強） | Strong（強い） |
| Seamless（シームレス） | Smooth（スムーズ） |
| Cutting-edge（最先端） | New/Modern（新しい/モダン） |

**Watch for:** （**注意してください:**）
- Adverbs (usually unnecessary) （副詞（通常は不要））
- Passive voice (switch to active) （受動態（能動態に切り替える））
- Nominalizations (verb → noun: "make a decision" → "decide") （名詞化（動詞→名詞：「決断する」→「決める」））

### Sentence-Level Checks （文レベルのチェック）

- One idea per sentence （1 文につき 1 つのアイデア）
- Vary sentence length (mix short and long) （文の長さを変える（短いものと長いものを混ぜる））
- Front-load important information （重要な情報を前もってロードする）
- Max 3 conjunctions per sentence （文ごとに接続詞は最大 3 つまで）
- No more than 25 words (usually) （25 単語以内 (通常)）

### Paragraph-Level Checks （段落レベルのチェック）

- One topic per paragraph （段落ごとに 1 つのトピック）
- Short paragraphs (2-4 sentences for web) （短い段落 (Web の場合は 2 ～ 4 文)）
- Strong opening sentences （力強い冒頭文）
- Logical flow between paragraphs （段落間の論理的な流れ）
- White space for scannability （スキャンしやすくするための空白スペース）

---

## Copy Editing Checklist （コピー編集チェックリスト）

### Before You Start （始める前に）
- [ ] Understand the goal of this copy （[ ] このコピーの目的を理解する）
- [ ] Know the target audience （[ ] 対象ユーザーを知る）
- [ ] Identify the desired action （[ ] 必要なアクションを特定します）
- [ ] Read through once without editing （[ ] 編集せずに一度通読してください）

### Clarity (Sweep 1) （クラリティ (スイープ 1)）
- [ ] Every sentence is immediately understandable （[ ] どの文もすぐに理解できる）
- [ ] No jargon without explanation （[ ] 専門用語は説明なしで使用）
- [ ] Pronouns have clear references （[ ] 代名詞には明確な参照がある）
- [ ] No sentences trying to do too much （[ ] やりすぎた文章はありません）

### Voice & Tone (Sweep 2) （ボイス&トーン(スイープ2)）
- [ ] Consistent formality level throughout （[ ] 全体を通して一貫した形式レベル）
- [ ] Brand personality maintained （[ ] ブランドの個性を維持）
- [ ] No jarring shifts in mood （[ ] 不快な気分の変化はありません）
- [ ] Reads well aloud （[ ] よく音読します）

### So What (Sweep 3) （それでどうした (スイープ 3)）
- [ ] Every feature connects to a benefit （[ ] すべての機能が利点につながります）
- [ ] Claims answer "why should I care?" （[ ] クレームは「なぜ気にする必要があるのか​​?」に答えます。）
- [ ] Benefits connect to real desires （[ ] メリットは本当の欲求につながります）
- [ ] No impressive-but-empty statements （[ ] 印象深いが空虚なステートメントはありません）

### Prove It (Sweep 4) （証明せよ (スイープ 4)）
- [ ] Claims are substantiated （[ ] 主張は実証されています）
- [ ] Social proof is specific and attributed （[ ] 社会的証明は具体的であり、帰属されます）
- [ ] Numbers and stats have sources （[ ] 数字と統計には出典があります）
- [ ] No unearned superlatives （[ ] 未獲得の最上級はありません）

### Specificity (Sweep 5) （特異性 (スイープ 5)）
- [ ] Vague words replaced with concrete ones （[ ] 曖昧な言葉を具体的な言葉に置き換える）
- [ ] Numbers and timeframes included （[ ] 数値と期間を含む）
- [ ] Generic statements made specific （[ ] 一般的な記述を具体化）
- [ ] Filler content removed （[ ] フィラーコンテンツが削除されました）

### Heightened Emotion (Sweep 6) （高まる感情 (スイープ 6)）
- [ ] Copy evokes feeling, not just information （[ ] コピーは単なる情報ではなく感情を呼び起こします）
- [ ] Pain points feel real （[ ] 痛みが現実に感じられる）
- [ ] Aspirations feel achievable （[ ] 願望は達成可能だと感じる）
- [ ] Emotion serves the message authentically （[ ] 感情はメッセージを真に伝える）

### Zero Risk (Sweep 7) （ゼロリスク (スイープ 7)）
- [ ] Objections addressed near CTA （[ ] CTA 付近で対処される異議申し立て）
- [ ] Trust signals present （[ ] 信頼シグナルが存在します）
- [ ] Next steps are crystal clear （[ ] 次のステップは非常に明確です）
- [ ] Risk reversals stated (guarantee, trial, etc.) （[ ] 記載されているリスクリバーサル（保証、トライアルなど））

### Final Checks （最終チェック）
- [ ] No typos or grammatical errors （[ ] タイプミスや文法上の誤りはありません）
- [ ] Consistent formatting （[ ] 一貫した書式設定）
- [ ] Links work (if applicable) （[ ] リンクは機能します (該当する場合)）
- [ ] Core message preserved through all edits （[ ] すべての編集を通じてコア メッセージが保持される）

---

## Common Copy Problems & Fixes （一般的なコピーの問題と修正）

### Problem: Wall of Features （問題: 機能の壁）
**Symptom:** List of what the product does without why it matters （**症状:** 製品の機能のリストが、それが重要である理由が記載されていない）
**Fix:** Add "which means..." after each feature to bridge to benefits （**修正:** 各機能の後に「つまり...」を追加して利点につなげます）

### Problem: Corporate Speak （問題: 社内でのスピーチ）
**Symptom:** "Leverage synergies to optimize outcomes" （**症状:** 「相乗効果を活用して結果を最適化する」）
**Fix:** Ask "How would a human say this?" and use those words （**修正:** 「人間だったらこれをどう言うでしょうか?」と尋ねてください。そしてその言葉を使う）

### Problem: Weak Opening （問題: 開口部が弱い）
**Symptom:** Starting with company history or vague statements （**症状:** 会社の歴史や曖昧な記述から始まる）
**Fix:** Lead with the reader's problem or desired outcome （**修正:** 読者の問題または望ましい結果をリードします）

### Problem: Buried CTA （問題: 埋もれたCTA）
**Symptom:** The ask comes after too much buildup, or isn't clear （**症状:** 質問があまりにも多く蓄積された後に表示されるか、明確ではありません。）
**Fix:** Make the CTA obvious, early, and repeated （**修正:** CTA を明確に、早期に、繰り返し表示するようにする）

### Problem: No Proof （問題: 証拠がない）
**Symptom:** "Customers love us" with no evidence （**症状:** 証拠のない「顧客は当社を愛している」）
**Fix:** Add specific testimonials, numbers, or case references （**修正:** 具体的な証言、数字、または事例参照を追加します。）

### Problem: Generic Claims （問題: 一般的なクレーム）
**Symptom:** "We help businesses grow" （**症状:** 「当社はビジネスの成長を支援します」）
**Fix:** Specify who, how, and by how much （**修正:** 誰が、どのように、そしていくらで）

### Problem: Mixed Audiences （問題: 視聴者が混在している）
**Symptom:** Copy tries to speak to everyone, resonates with no one （**症状:** コピーは全員に話しかけようとしますが、誰の心にも響きません。）
**Fix:** Pick one audience and write directly to them （**修正:** 対象ユーザーを 1 人選択し、そのユーザーに直接書き込みます）

### Problem: Feature Overload （問題: 機能の過負荷）
**Symptom:** Listing every capability, overwhelming the reader （**症状:** あらゆる機能を列挙し、読者を圧倒する）
**Fix:** Focus on 3-5 key benefits that matter most to the audience （**修正:** 視聴者にとって最も重要な 3 ～ 5 つの主要な利点に焦点を当てる）

---

## Working with Copy Sweeps （コピー スイープの操作）

When editing collaboratively: （共同編集する場合:）

1. **Run a sweep and present findings** - Show what you found, why it's an issue （**スイープを実行して調査結果を提示します** - 調査結果とそれが問題となる理由を示します）
2. **Recommend specific edits** - Don't just identify problems; propose solutions （**特定の編集を推奨します** - 問題を特定するだけではありません。解決策を提案する）
3. **Request the updated copy** - Let the author make final decisions （**更新されたコピーをリクエスト** - 最終的な決定は作成者に任せてください）
4. **Verify previous sweeps** - After each round of edits, re-check earlier sweeps （**以前のスイープを確認する** - 各ラウンドの編集後に、以前のスイープを再確認します。）
5. **Repeat until clean** - Continue until a full sweep finds no new issues （**クリーンになるまで繰り返します** - 完全なスイープで新しい問題が見つからなくなるまで続行します）

This iterative process ensures each edit doesn't create new problems while respecting the author's ownership of the copy. （この反復的なプロセスにより、コピーの作成者の所有権を尊重しながら、各編集によって新たな問題が発生しないことが保証されます。）

---

## References （参考文献）

- [Plain English Alternatives](references/plain-english-alternatives.md): Replace complex words with simpler alternatives （[Plain English Alternatives](references/plain-english-alternatives.md): 複雑な単語をより単純な代替語に置き換えます）

---

## Task-Specific Questions （タスク固有の質問）

1. What's the goal of this copy? (Awareness, conversion, retention) （このコピーの目的は何ですか? （認知度、コンバージョン、定着率））
2. What action should readers take? （読者はどのような行動をとるべきでしょうか?）
3. Are there specific concerns or known issues? （特定の懸念事項や既知の問題はありますか?）
4. What proof/evidence do you have available? （どのような証拠/証拠がありますか?）

---

## Related Skills （関連スキル）

- **copywriting**: For writing new copy from scratch (use this skill to edit after your first draft is complete) （**コピーライティング**: 新しいコピーを最初から作成する場合 (最初のドラフトが完了した後に編集するには、このスキルを使用します)）
- **page-cro**: For broader page optimization beyond copy （**page-cro**: コピーを超えた広範なページ最適化用）
- **marketing-psychology**: For understanding why certain edits improve conversion （**マーケティング心理学**: 特定の編集によってコンバージョンが向上する理由を理解するため）
- **ab-test-setup**: For testing copy variations （**ab-test-setup**: コピーのバリエーションをテストするため）

---

## When to Use Each Skill （各スキルをいつ使用するか）

| Task（タスク） | Skill to Use（使えるスキル） |
|------|--------------|
| Writing new page copy from scratch（新しいページのコピーを最初から作成する） | copywriting（コピーライティング） |
| Reviewing and improving existing copy（既存のコピーを見直して改善する） | copy-editing (this skill)（コピー編集（このスキル）） |
| Editing copy you just wrote（作成したばかりのコピーを編集中） | copy-editing (this skill)（コピー編集（このスキル）） |
| Structural or strategic page changes（ページの構造的または戦略的な変更） | page-cro（ページクロ） |
