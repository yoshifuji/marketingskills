---
name: product-marketing-context
version: 1.0.0
description: "When the user wants to create or update their product marketing context document. Also use when the user mentions 'product context,' 'marketing context,' 'set up context,' 'positioning,' or wants to avoid repeating foundational information across marketing tasks. Creates `.claude/product-marketing-context.md` that other marketing skills reference." （日本語訳：「ユーザーが製品のマーケティング コンテキスト ドキュメントを作成または更新したい場合。ユーザーが『製品コンテキスト』、『マーケティング コンテキスト』、『コンテキストの設定』、『ポジショニング』について言及する場合、またはマーケティング タスク全体で基本的な情報の繰り返しを避けたい場合にも使用します。他のマーケティング スキルが参照する `.claude/product-marketing-context.md` を作成します。」）
---

# Product Marketing Context （日本語訳：製品マーケティングのコンテキスト）

You help users create and maintain a product marketing context document. This captures foundational positioning and messaging information that other marketing skills reference, so users don't repeat themselves. （日本語訳：ユーザーが製品マーケティング コンテキスト ドキュメントを作成および管理するのを支援します。これにより、他のマーケティング スキルが参照する基本的なポジショニングとメッセージング情報が取得されるため、ユーザーは同じことを繰り返すことがなくなります。）

The document is stored at `.claude/product-marketing-context.md`. （日本語訳：ドキュメントは `.claude/product-marketing-context.md` に保存されます。）

## Workflow （日本語訳：ワークフロー）

### Step 1: Check for Existing Context （日本語訳：ステップ 1: 既存のコンテキストを確認する）

First, check if `.claude/product-marketing-context.md` already exists. （日本語訳：まず、`.claude/product-marketing-context.md` がすでに存在するかどうかを確認します。）

**If it exists:** （日本語訳：**存在する場合:**）
- Read it and summarize what's captured （日本語訳：読んで内容を要約する）
- Ask which sections they want to update （日本語訳：どのセクションを更新したいかを尋ねる）
- Only gather info for those sections （日本語訳：それらのセクションの情報のみを収集する）

**If it doesn't exist, offer two options:** （日本語訳：**存在しない場合は、2 つのオプションを提供します。**）

1. **Auto-draft from codebase** (recommended): You'll study the repo—README, landing pages, marketing copy, package.json, etc.—and draft a V1 of the context document. The user then reviews, corrects, and fills gaps. This is faster than starting from scratch. （日本語訳：**コードベースからの自動ドラフト** (推奨): README、ランディング ページ、マーケティング コピー、package.json などのリポジトリを調べて、コンテキスト ドキュメントの V1 をドラフトします。その後、ユーザーはレビューし、修正し、ギャップを埋めます。これは、最初から始めるよりも高速です。）

2. **Start from scratch**: Walk through each section conversationally, gathering info one section at a time. （日本語訳：**最初から始める**: 各セクションを会話形式で説明し、一度に 1 セクションずつ情報を収集します。）

Most users prefer option 1. After presenting the draft, ask: "What needs correcting? What's missing?" （日本語訳：ほとんどのユーザーはオプション 1 を好みます。草案を提示した後、「何を修正する必要がありますか? 何が不足していますか?」と尋ねます。）

### Step 2: Gather Information （日本語訳：ステップ 2: 情報を収集する）

**If auto-drafting:** （日本語訳：**自動ドラフトの場合:**）
1. Read the codebase: README, landing pages, marketing copy, about pages, meta descriptions, package.json, any existing docs （日本語訳：コードベースを読む: README、ランディング ページ、マーケティング コピー、ページについて、メタ説明、package.json、既存のドキュメント）
2. Draft all sections based on what you find （日本語訳：見つけた内容に基づいてすべてのセクションの草案を作成する）
3. Present the draft and ask what needs correcting or is missing （日本語訳：草案を提示し、修正が必要な点や不足している点を尋ねます）
4. Iterate until the user is satisfied （日本語訳：ユーザーが満足するまで繰り返します）

**If starting from scratch:** （日本語訳：**最初から始める場合:**）
Walk through each section below conversationally, one at a time. Don't dump all questions at once. （日本語訳：以下の各セクションを一度に 1 つずつ会話形式で説明します。すべての質問を一度に捨てないでください。）

For each section: （日本語訳：各セクションについて:）
1. Briefly explain what you're capturing （日本語訳：何をキャプチャしているのかを簡単に説明します）
2. Ask relevant questions （日本語訳：関連する質問をする）
3. Confirm accuracy （日本語訳：精度の確認）
4. Move to the next （日本語訳：次へ移動）

**Important:** Push for verbatim customer language. Exact phrases are more valuable than polished descriptions. （日本語訳：**重要:** 顧客の言葉をそのまま伝えてください。洗練された説明よりも、正確なフレーズの方が価値があります。）

---

## Sections to Capture （日本語訳：キャプチャするセクション）

### 1. Product Overview （日本語訳：1. 製品概要）
- One-line description （日本語訳：一行説明）
- What it does (2-3 sentences) （日本語訳：何をするのか (2​​ ～ 3 文)）
- Product category (what "shelf" you sit on—how customers search for you) （日本語訳：製品カテゴリ (あなたがどの「棚」に座っているか - 顧客がどのようにあなたを検索しているか)）
- Product type (SaaS, marketplace, e-commerce, service, etc.) （日本語訳：製品タイプ (SaaS、マーケットプレイス、電子商取引、サービスなど)）
- Business model and pricing （日本語訳：ビジネスモデルと価格設定）

### 2. Target Audience （日本語訳：2. 対象者）
- Target company type (industry, size, stage) （日本語訳：対象企業の種類（業種、規模、ステージ））
- Target decision-makers (roles, departments) （日本語訳：対象となる意思決定者（役割、部門））
- Primary use case (the main problem you solve) （日本語訳：主な使用例 (解決する主な問題)）
- Jobs to be done (2-3 things customers "hire" you for) （日本語訳：やるべき仕事 (顧客があなたを「雇う」ための 2 ～ 3 つのこと)）
- Specific use cases or scenarios （日本語訳：特定の使用例またはシナリオ）

### 3. Personas (B2B only) （日本語訳：3. ペルソナ (B2B のみ)）
If multiple stakeholders are involved in buying, capture for each: （日本語訳：複数の関係者が購入に関与している場合は、それぞれについて以下をキャプチャします。）
- User, Champion, Decision Maker, Financial Buyer, Technical Influencer （日本語訳：ユーザー、チャンピオン、意思決定者、金融バイヤー、テクニカルインフルエンサー）
- What each cares about, their challenge, and the value you promise them （日本語訳：それぞれが重視していること、課題、そして約束する価値）

### 4. Problems & Pain Points （日本語訳：4. 問題と問題点）
- Core challenge customers face before finding you （日本語訳：顧客が貴社を見つける前に直面する主な課題）
- Why current solutions fall short （日本語訳：現在のソリューションが不十分な理由）
- What it costs them (time, money, opportunities) （日本語訳：かかるもの (時間、お金、機会)）
- Emotional tension (stress, fear, doubt) （日本語訳：感情的な緊張（ストレス、恐怖、疑い））

### 5. Competitive Landscape （日本語訳：5. 競争環境）
- **Direct competitors**: Same solution, same problem (e.g., Calendly vs SavvyCal) （日本語訳：**直接の競合他社**: 同じソリューション、同じ問題 (例: Calendly と SavvyCal)）
- **Secondary competitors**: Different solution, same problem (e.g., Calendly vs Superhuman scheduling) （日本語訳：**第 2 の競合他社**: 異なるソリューション、同じ問題 (例: Calendly と Superhuman のスケジュール設定)）
- **Indirect competitors**: Conflicting approach (e.g., Calendly vs personal assistant) （日本語訳：**間接的な競合他社**: 相反するアプローチ (例: Calendly 対パーソナル アシスタント)）
- How each falls short for customers （日本語訳：それぞれが顧客にとってどのように不足しているか）

### 6. Differentiation （日本語訳：6. 差別化）
- Key differentiators (capabilities alternatives lack) （日本語訳：主な差別化要因 (代替品に欠けている機能)）
- How you solve it differently （日本語訳：別の解決方法）
- Why that's better (benefits) （日本語訳：その方が良い理由（メリット））
- Why customers choose you over alternatives （日本語訳：顧客が他の選択肢よりも貴社を選ぶ理由）

### 7. Objections & Anti-Personas （日本語訳：7. 反対意見とアンチペルソナ）
- Top 3 objections heard in sales and how to address them （日本語訳：営業でよく聞かれる反対意見トップ 3 とその対処方法）
- Who is NOT a good fit (anti-persona) （日本語訳：合わない人（アンチペルソナ））

### 8. Switching Dynamics （日本語訳：8. スイッチングダイナミクス）
The JTBD Four Forces: （日本語訳：JTBD の 4 つの力:）
- **Push**: What frustrations drive them away from current solution （日本語訳：**プッシュ**: 現在のソリューションから遠ざける原因となっているフラストレーションは何か）
- **Pull**: What attracts them to you （日本語訳：**魅力**: 何があなたを惹きつけるのか）
- **Habit**: What keeps them stuck with current approach （日本語訳：**習慣**: 現在のアプローチに固執している原因）
- **Anxiety**: What worries them about switching （日本語訳：**不安**: 切り替える際に心配していること）

### 9. Customer Language （日本語訳：9. 顧客の言語）
- How customers describe the problem (verbatim) （日本語訳：顧客が問題を説明する方法 (逐語的に)）
- How they describe your solution (verbatim) （日本語訳：ソリューションをどのように説明するか (逐語的に)）
- Words/phrases to use （日本語訳：使用する単語/フレーズ）
- Words/phrases to avoid （日本語訳：避けるべき言葉/フレーズ）
- Glossary of product-specific terms （日本語訳：製品固有の用語集）

### 10. Brand Voice （日本語訳：10. ブランドボイス）
- Tone (professional, casual, playful, etc.) （日本語訳：トーン (プロフェッショナル、カジュアル、遊び心など)）
- Communication style (direct, conversational, technical) （日本語訳：コミュニケーション スタイル (直接的、会話的、技術的)）
- Brand personality (3-5 adjectives) （日本語訳：ブランドの個性 (3 ～ 5 個の形容詞)）

### 11. Proof Points （日本語訳：11. 証明ポイント）
- Key metrics or results to cite （日本語訳：引用する主要な指標または結果）
- Notable customers/logos （日本語訳：著名な顧客/ロゴ）
- Testimonial snippets （日本語訳：お客様の声の抜粋）
- Main value themes and supporting evidence （日本語訳：主な価値テーマと裏付けとなる証拠）

### 12. Goals （日本語訳：12. 目標）
- Primary business goal （日本語訳：主なビジネス目標）
- Key conversion action (what you want people to do) （日本語訳：主要なコンバージョン アクション（ユーザーに実行してもらいたいこと））
- Current metrics (if known) （日本語訳：現在のメトリクス (既知の場合)）

---

## Step 3: Create the Document （日本語訳：ステップ 3: ドキュメントを作成する）

After gathering information, create `.claude/product-marketing-context.md` with this structure: （日本語訳：情報を収集したら、次の構造で `.claude/product-marketing-context.md` を作成します。）

```markdown
# Product Marketing Context

*Last updated: [date]*

## Product Overview
**One-liner:**
**What it does:**
**Product category:**
**Product type:**
**Business model:**

## Target Audience
**Target companies:**
**Decision-makers:**
**Primary use case:**
**Jobs to be done:**
-
**Use cases:**
-

## Personas
| Persona | Cares about | Challenge | Value we promise |
|---------|-------------|-----------|------------------|
| | | | |

## Problems & Pain Points
**Core problem:**
**Why alternatives fall short:**
-
**What it costs them:**
**Emotional tension:**

## Competitive Landscape
**Direct:** [Competitor] — falls short because...
**Secondary:** [Approach] — falls short because...
**Indirect:** [Alternative] — falls short because...

## Differentiation
**Key differentiators:**
-
**How we do it differently:**
**Why that's better:**
**Why customers choose us:**

## Objections
| Objection | Response |
|-----------|----------|
| | |

**Anti-persona:**

## Switching Dynamics
**Push:**
**Pull:**
**Habit:**
**Anxiety:**

## Customer Language
**How they describe the problem:**
- "[verbatim]"
**How they describe us:**
- "[verbatim]"
**Words to use:**
**Words to avoid:**
**Glossary:**
| Term | Meaning |
|------|---------|
| | |

## Brand Voice
**Tone:**
**Style:**
**Personality:**

## Proof Points
**Metrics:**
**Customers:**
**Testimonials:**
> "[quote]" — [who]
**Value themes:**
| Theme | Proof |
|-------|-------|
| | |

## Goals
**Business goal:**
**Conversion action:**
**Current metrics:**
```

---

## Step 4: Confirm and Save （日本語訳：ステップ 4: 確認して保存する）

- Show the completed document （日本語訳：完成した書類を見せる）
- Ask if anything needs adjustment （日本語訳：調整が必要かどうか尋ねる）
- Save to `.claude/product-marketing-context.md` （日本語訳：`.claude/product-marketing-context.md` に保存）
- Tell them: "Other marketing skills will now use this context automatically. Run `/product-marketing-context` anytime to update it." （日本語訳：「他のマーケティング スキルはこのコンテキストを自動的に使用するようになりました。いつでも `/product-marketing-context` を実行して更新してください。」と伝えます。）

---

## Tips （日本語訳：ヒント）

- **Be specific**: Ask "What's the #1 frustration that brings them to you?" not "What problem do they solve?" （日本語訳：**具体的に**: 「彼らをあなたにもたらす最大の不満は何ですか?」と尋ねます。 「どのような問題を解決するのか？」ではありません。）
- **Capture exact words**: Customer language beats polished descriptions （日本語訳：**正確な単語をキャプチャ**: 顧客の言語は洗練された説明に勝ります）
- **Ask for examples**: "Can you give me an example?" unlocks better answers （日本語訳：**例を尋ねる**: 「例を挙げてもらえますか?」より良い答えを導き出す）
- **Validate as you go**: Summarize each section and confirm before moving on （日本語訳：**作業を進めながら検証**: 各セクションを要約し、次に進む前に確認してください。）
- **Skip what doesn't apply**: Not every product needs all sections (e.g., Personas for B2C) （日本語訳：**該当しないものはスキップしてください**: すべての製品にすべてのセクションが必要なわけではありません (例: B2C のペルソナ)）
