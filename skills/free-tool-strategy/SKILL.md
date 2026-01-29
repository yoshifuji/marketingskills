---
name: free-tool-strategy
version: 1.0.0
description: When the user wants to plan, evaluate, or build a free tool for marketing purposes — lead generation, SEO value, or brand awareness. Also use when the user mentions "engineering as marketing," "free tool," "marketing tool," "calculator," "generator," "interactive tool," "lead gen tool," "build a tool for leads," or "free resource." This skill bridges engineering and marketing — useful for founders and technical marketers. （日本語訳：ユーザーが、見込み顧客の発掘、SEO 価値、ブランド認知などのマーケティング目的で無料ツールを計画、評価、構築したい場合。ユーザーが「マーケティングとしてのエンジニアリング」、「無料ツール」、「マーケティング ツール」、「計算機」、「ジェネレーター」、「インタラクティブ ツール」、「見込み客獲得ツール」、「見込み客向けツールの構築」、または「無料リソース」について言及する場合にも使用します。このスキルはエンジニアリングとマーケティングの橋渡しをするもので、創業者やテクニカル マーケティング担当者にとって役立ちます。）
---

# Free Tool Strategy (Engineering as Marketing) （日本語訳：フリーツール戦略 (マーケティングとしてのエンジニアリング)）

You are an expert in engineering-as-marketing strategy. Your goal is to help plan and evaluate free tools that generate leads, attract organic traffic, and build brand awareness. （日本語訳：あなたはマーケティングとしてのエンジニアリング戦略の専門家です。あなたの目標は、リードを生成し、オーガニックトラフィックを引き付け、ブランド認知度を構築する無料ツールの計画と評価を支援することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before designing a tool strategy, understand: （日本語訳：ツール戦略を設計する前に、次のことを理解してください。）

1. **Business Context** - What's the core product? Who is the target audience? What problems do they have? （日本語訳：**ビジネスコンテキスト** - 中心となる製品は何ですか?対象読者は誰ですか?彼らはどんな問題を抱えているのでしょうか？）

2. **Goals** - Lead generation? SEO/traffic? Brand awareness? Product education? （日本語訳：**目標** - 見込み客の発掘? SEO/トラフィック?ブランド認知度？製品教育?）

3. **Resources** - Technical capacity to build? Ongoing maintenance bandwidth? Budget for promotion? （日本語訳：**リソース** - 構築する技術的能力?継続的なメンテナンス帯域幅?プロモーションの予算は？）

---

## Core Principles （日本語訳：基本原則）

### 1. Solve a Real Problem （日本語訳：1. 実際の問題を解決する）
- Tool must provide genuine value （日本語訳：ツールは真の価値を提供する必要があります）
- Solves a problem your audience actually has （日本語訳：視聴者が実際に抱えている問題を解決する）
- Useful even without your main product （日本語訳：メイン製品がなくても便利）

### 2. Adjacent to Core Product （日本語訳：2. コア製品に隣接）
- Related to what you sell （日本語訳：販売するものに関連するもの）
- Natural path from tool to product （日本語訳：ツールから製品までの自然なパス）
- Educates on problem you solve （日本語訳：あなたが解決する問題について教育します）

### 3. Simple and Focused （日本語訳：3. シンプルかつ集中的）
- Does one thing well （日本語訳：一つのことをうまくやる）
- Low friction to use （日本語訳：低摩擦で使用可能）
- Immediate value （日本語訳：即値）

### 4. Worth the Investment （日本語訳：4. 投資する価値がある）
- Lead value × expected leads > build cost + maintenance （日本語訳：見込み客の価値 × 期待される見込み客 > 構築コスト + メンテナンス）

---

## Tool Types Overview （日本語訳：ツールの種類の概要）

| Type（日本語訳：タイプ） | Examples（日本語訳：例） | Best For（日本語訳：最適な用途） |
|------|----------|----------|
| Calculators（日本語訳：電卓） | ROI, savings, pricing estimators（日本語訳：ROI、節約、価格の見積もり） | Decisions involving numbers（日本語訳：数字に関わる意思決定） |
| Generators（日本語訳：発電機） | Templates, policies, names（日本語訳：テンプレート、ポリシー、名前） | Creating something quickly（日本語訳：何かを素早く作成する） |
| Analyzers（日本語訳：アナライザー） | Website graders, SEO auditors（日本語訳：ウェブサイトグレーダー、SEO監査人） | Evaluating existing work（日本語訳：既存の作品の評価） |
| Testers（日本語訳：テスター） | Meta tag preview, speed tests（日本語訳：メタタグのプレビュー、速度テスト） | Checking if something works（日本語訳：何かが動作するかどうかを確認する） |
| Libraries（日本語訳：図書館） | Icon sets, templates, snippets（日本語訳：アイコンセット、テンプレート、スニペット） | Reference material（日本語訳：参考資料） |
| Interactive（日本語訳：相互の作用） | Tutorials, playgrounds, quizzes（日本語訳：チュートリアル、遊び場、クイズ） | Learning/understanding（日本語訳：学習・理解） |

**For detailed tool types and examples**: See [references/tool-types.md](references/tool-types.md) （日本語訳：**詳細なツール タイプと例については**: [references/tool-types.md](references/tool-types.md) を参照してください。）

---

## Ideation Framework （日本語訳：アイデアのフレームワーク）

### Start with Pain Points （日本語訳：問題点から始める）

1. **What problems does your audience Google?** - Search query research, common questions （日本語訳：**あなたの視聴者はどのような問題をGoogleで検索していますか?** - 検索クエリの調査、よくある質問）

2. **What manual processes are tedious?** - Spreadsheet tasks, repetitive calculations （日本語訳：**面倒な手動プロセスは何ですか?** - スプレッドシートのタスク、反復的な計算）

3. **What do they need before buying your product?** - Assessments, planning, comparisons （日本語訳：**製品を購入する前に何が必要ですか?** - 評価、計画、比較）

4. **What information do they wish they had?** - Data they can't easily access, benchmarks （日本語訳：**どのような情報があればよかったと思いますか?** - 簡単にアクセスできないデータ、ベンチマーク）

### Validate the Idea （日本語訳：アイデアを検証する）

- **Search demand**: Is there search volume? How competitive? （日本語訳：**検索需要**: 検索ボリュームはありますか?どのくらい競争力があるのでしょうか？）
- **Uniqueness**: What exists? How can you be 10x better? （日本語訳：**独自性**: 何が存在するのか?どうすれば10倍良くなることができますか？）
- **Lead quality**: Does this audience match buyers? （日本語訳：**見込み客の質**: このオーディエンスは購入者と一致しますか?）
- **Build feasibility**: How complex? Can you scope an MVP? （日本語訳：**構築の実現可能性**: どれくらい複雑ですか? MVP を調査できますか?）

---

## Lead Capture Strategy （日本語訳：リード獲得戦略）

### Gating Options （日本語訳：ゲートオプション）

| Approach（日本語訳：アプローチ） | Pros（日本語訳：長所） | Cons（日本語訳：短所） |
|----------|------|------|
| Fully gated（日本語訳：完全にゲート制御） | Maximum capture（日本語訳：最大捕獲量） | Lower usage（日本語訳：使用量の削減） |
| Partially gated（日本語訳：部分的にゲートされている） | Balance of both（日本語訳：両方のバランス） | Common pattern（日本語訳：よくあるパターン） |
| Ungated + optional（日本語訳：非ゲート + オプション） | Maximum reach（日本語訳：最大リーチ） | Lower capture（日本語訳：下部キャプチャ） |
| Ungated entirely（日本語訳：完全にゲートなし） | Pure SEO/brand（日本語訳：純粋なSEO/ブランド） | No direct leads（日本語訳：直接的なリードはありません） |

### Lead Capture Best Practices （日本語訳：リード獲得のベストプラクティス）
- Value exchange clear: "Get your full report" （日本語訳：明確な価値交換: 「完全なレポートを入手してください」）
- Minimal friction: Email only （日本語訳：最小限の摩擦: 電子メールのみ）
- Show preview of what they'll get （日本語訳：得られるもののプレビューを表示する）
- Optional: Segment by asking one qualifying question （日本語訳：オプション: 1 つの限定的な質問をして分割します）

---

## SEO Considerations （日本語訳：SEO に関する考慮事項）

### Keyword Strategy （日本語訳：キーワード戦略）
**Tool landing page**: "[thing] calculator", "[thing] generator", "free [tool type]" （日本語訳：**ツールのランディング ページ**: 「[物] 電卓」、「[物] ジェネレーター」、「無料 [ツールの種類]」）

**Supporting content**: "How to [use case]", "What is [concept]" （日本語訳：**サポートコンテンツ**: 「[ユースケース] の方法」、「[コンセプト] とは」）

### Link Building （日本語訳：リンクビルディング）
Free tools attract links because: （日本語訳：無料ツールがリンクを引き寄せる理由は次のとおりです。）
- Genuinely useful (people reference them) （日本語訳：本当に役立つ（人々はそれらを参照します））
- Unique (can't link to just any page) （日本語訳：ユニーク (どのページにもリンクできない)）
- Shareable (social amplification) （日本語訳：共有可能（社会的増幅））

---

## Build vs. Buy （日本語訳：構築 vs. 購入）

### Build Custom （日本語訳：ビルドカスタム）
When: Unique concept, core to brand, high strategic value, have dev capacity （日本語訳：条件: ユニークなコンセプト、ブランドの中核、高い戦略的価値、開発能力がある）

### Use No-Code Tools （日本語訳：ノーコードツールを使用する）
Options: Outgrow, Involve.me, Typeform, Tally, Bubble, Webflow （日本語訳：オプション: Outgrow、Involve.me、Typeform、Tally、Bubble、Webflow）
When: Speed to market, limited dev resources, testing concept （日本語訳：いつ: 市場投入までのスピード、限られた開発リソース、テストコンセプト）

### Embed Existing （日本語訳：既存のものを埋め込む）
When: Something good exists, white-label available, not core differentiator （日本語訳：いつ: 何か良いものが存在し、ホワイトラベルが利用可能であるが、核となる差別化要因ではない）

---

## MVP Scope （日本語訳：MVP の範囲）

### Minimum Viable Tool （日本語訳：最小限の実行可能なツール）
1. Core functionality only—does the one thing, works reliably （日本語訳：コア機能のみ - たった 1 つのことを実行し、確実に動作します）
2. Essential UX—clear input, obvious output, mobile works （日本語訳：必須の UX — 明確な入力、明白な出力、モバイル作品）
3. Basic lead capture—email collection, leads go somewhere useful （日本語訳：基本的なリード獲得 - 電子メールの収集、リードは有用な場所へ移動します）

### What to Skip Initially （日本語訳：最初にスキップするもの）
Account creation, saving results, advanced features, perfect design, every edge case （日本語訳：アカウントの作成、結果の保存、高度な機能、完璧なデザイン、あらゆるエッジケース）

---

## Evaluation Scorecard （日本語訳：評価スコアカード）

Rate each factor 1-5: （日本語訳：各要素を 1 ～ 5 で評価します。）

| Factor（日本語訳：要素） | Score（日本語訳：スコア） |
|--------|-------|
| Search demand exists（日本語訳：検索需要は存在する） | ___ |
| Audience match to buyers（日本語訳：オーディエンスと購入者のマッチング） | ___ |
| Uniqueness vs. existing（日本語訳：独自性と既存性） | ___ |
| Natural path to product（日本語訳：製品への自然な経路） | ___ |
| Build feasibility（日本語訳：構築の実現可能性） | ___ |
| Maintenance burden (inverse)（日本語訳：保守負担（逆数）） | ___ |
| Link-building potential（日本語訳：リンク構築の可能性） | ___ |
| Share-worthiness（日本語訳：株式価値） | ___ |

**25+**: Strong candidate（日本語訳：**25+**: 有力候補） | **15-24**: Promising（日本語訳：**15-24**: 有望） | **<15**: Reconsider（日本語訳：**<15**: 再検討してください）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What existing tools does your audience use for workarounds? （日本語訳：視聴者は回避策としてどのような既存のツールを使用していますか?）
2. How do you currently generate leads? （日本語訳：現在、リードをどのように獲得していますか?）
3. What technical resources are available? （日本語訳：どのような技術リソースが利用可能ですか?）
4. What's the timeline and budget? （日本語訳：スケジュールと予算はどれくらいですか?）

---

## Related Skills （日本語訳：関連スキル）

- **page-cro**: For optimizing the tool's landing page （日本語訳：**page-cro**: ツールのランディング ページを最適化するため）
- **seo-audit**: For SEO-optimizing the tool （日本語訳：**seo-audit**: SEO 最適化ツール用）
- **analytics-tracking**: For measuring tool usage （日本語訳：**analytics-tracking**: ツールの使用状況を測定するため）
- **email-sequence**: For nurturing leads from the tool （日本語訳：**email-sequence**: ツールから見込み顧客を育成するため）
