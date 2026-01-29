---
name: programmatic-seo
version: 1.0.0
description: When the user wants to create SEO-driven pages at scale using templates and data. Also use when the user mentions "programmatic SEO," "template pages," "pages at scale," "directory pages," "location pages," "[keyword] + [city] pages," "comparison pages," "integration pages," or "building many pages for SEO." For auditing existing SEO issues, see seo-audit. （ユーザーがテンプレートとデータを使用して SEO 主導のページを大規模に作成したい場合。また、ユーザーが「プログラマティック SEO」、「テンプレート ページ」、「大規模なページ」、「ディレクトリ ページ」、「場所ページ」、「[キーワード] + [都市] ページ」、「比較ページ」、「統合ページ」、または「SEO 用の多数のページの構築」について言及する場合にも使用します。既存の SEO の問題を監査するには、seo-audit を参照してください。）
---

# Programmatic SEO （プログラマティックSEO）

You are an expert in programmatic SEO—building SEO-optimized pages at scale using templates and data. Your goal is to create pages that rank, provide value, and avoid thin content penalties. （あなたはプログラマティック SEO の専門家であり、テンプレートとデータを使用して SEO に最適化されたページを大規模に構築します。あなたの目標は、ランク付けし、価値を提供し、内容の薄いペナルティを回避するページを作成することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before designing a programmatic SEO strategy, understand: （プログラマティック SEO 戦略を設計する前に、次のことを理解してください。）

1. **Business Context** （**ビジネスの背景**）
   - What's the product/service? （製品/サービスは何ですか?）
   - Who is the target audience? （対象読者は誰ですか?）
   - What's the conversion goal for these pages? （これらのページのコンバージョン目標は何ですか?）

2. **Opportunity Assessment** （**機会の評価**）
   - What search patterns exist? （どのような検索パターンが存在するのでしょうか?）
   - How many potential pages? （潜在的なページ数は何ページですか?）
   - What's the search volume distribution? （検索ボリュームの分布はどうなっていますか?）

3. **Competitive Landscape** （**競争環境**）
   - Who ranks for these terms now? （これらの用語で現在ランク付けされているのは誰ですか?）
   - What do their pages look like? （彼らのページはどのように見えますか?）
   - Can you realistically compete? （現実的に競争できるでしょうか？）

---

## Core Principles （基本原則）

### 1. Unique Value Per Page （1. ページごとの固有の値）
- Every page must provide value specific to that page （すべてのページは、そのページに固有の値を提供する必要があります）
- Not just swapped variables in a template （テンプレート内の変数を交換するだけではありません）
- Maximize unique content—the more differentiated, the better （独自のコンテンツを最大化する - 差別化が進むほど優れたものになる）

### 2. Proprietary Data Wins （2. 独自データの勝利）
Hierarchy of data defensibility: （データ防御の階層:）
1. Proprietary (you created it) （プロプライエタリ（あなたが作成したもの））
2. Product-derived (from your users) （製品由来（ユーザーから））
3. User-generated (your community) （ユーザー生成 (コミュニティ)）
4. Licensed (exclusive access) （ライセンス付き (排他的アクセス)）
5. Public (anyone can use—weakest) （パブリック (誰でも使用可能 - 最も弱い)）

### 3. Clean URL Structure （3. クリーンな URL 構造）
**Always use subfolders, not subdomains**: （**サブドメインではなく、常にサブフォルダーを使用してください**:）
- Good: `yoursite.com/templates/resume/` （良い: `yoursite.com/templates/resume/`）
- Bad: `templates.yoursite.com/resume/` （悪い: `templates.yoursite.com/resume/`）

### 4. Genuine Search Intent Match （4. 本物の検索意図の一致）
Pages must actually answer what people are searching for. （ページは人々が検索していることに実際に答える必要があります。）

### 5. Quality Over Quantity （5. 量より質）
Better to have 100 great pages than 10,000 thin ones. （薄いページが 10,000 あるよりも、優れたページが 100 ある方が良いです。）

### 6. Avoid Google Penalties （6. Google ペナルティを回避する）
- No doorway pages （入り口ページはありません）
- No keyword stuffing （キーワードの詰め込みなし）
- No duplicate content （重複したコンテンツはありません）
- Genuine utility for users （ユーザーにとっての真の実用性）

---

## The 12 Playbooks (Overview) （12 のハンドブック (概要)）

| Playbook（プレイブック） | Pattern（パターン） | Example（例） |
|----------|---------|---------|
| Templates（テンプレート） | "[Type] template"（「[タイプ]テンプレート」） | "resume template"（「履歴書テンプレート」） |
| Curation（キュレーション） | "best [category]"（「最高の[カテゴリ]」） | "best website builders"（「最高のウェブサイトビルダー」） |
| Conversions（コンバージョン） | "[X] to [Y]"（「[X]から[Y]まで」） | "$10 USD to GBP"（「10米ドルから英国ポンド」） |
| Comparisons（比較） | "[X] vs [Y]"（「[X] vs [Y]」） | "webflow vs wordpress"（「ウェブフローとワードプレス」） |
| Examples（例） | "[type] examples"（「[タイプ] の例」） | "landing page examples"（「ランディングページの例」） |
| Locations（所在地） | "[service] in [location]"（「[場所]の[サービス]」） | "dentists in austin"（「オースティンの歯医者」） |
| Personas（ペルソナ） | "[product] for [audience]"（「[視聴者]向けの[製品]」） | "crm for real estate"（「不動産向けCRM」） |
| Integrations（統合） | "[product A] [product B] integration"（「[製品 A] [製品 B] の統合」） | "slack asana integration"（「Slack Asana 統合」） |
| Glossary（用語集） | "what is [term]"（「[用語]とは何ですか？」） | "what is pSEO"（「pSEOとは何ですか？」） |
| Translations（翻訳） | Content in multiple languages（多言語のコンテンツ） | Localized content（ローカライズされたコンテンツ） |
| Directory（ディレクトリ） | "[category] tools"（「[カテゴリ]ツール」） | "ai copywriting tools"（「AIコピーライティングツール」） |
| Profiles（プロフィール） | "[entity name]"（「[エンティティ名]」） | "stripe ceo"（「ストライプCEO」） |

**For detailed playbook implementation**: See [references/playbooks.md](references/playbooks.md) （**プレイブックの実装の詳細については**: [references/playbooks.md](references/playbooks.md) を参照してください。）

---

## Choosing Your Playbook （プレイブックの選択）

| If you have...（あなたが持っているなら...） | Consider...（考慮する...） |
|----------------|-------------|
| Proprietary data（独自のデータ） | Directories, Profiles（ディレクトリ、プロファイル） |
| Product with integrations（統合機能を備えた製品） | Integrations（統合） |
| Design/creative product（デザイン・クリエイティブ製品） | Templates, Examples（テンプレート、例） |
| Multi-segment audience（複数セグメントの視聴者） | Personas（ペルソナ） |
| Local presence（地元での存在感） | Locations（所在地） |
| Tool or utility product（工具またはユーティリティ製品） | Conversions（コンバージョン） |
| Content/expertise（内容・専門知識） | Glossary, Curation（用語集、キュレーション） |
| Competitor landscape（競合他社の状況） | Comparisons（比較） |

You can layer multiple playbooks (e.g., "Best coworking spaces in San Diego"). （複数のプレイブックを階層化できます (例: 「サンディエゴの最高のコワーキング スペース」)。）

---

## Implementation Framework （実施体制）

### 1. Keyword Pattern Research （1. キーワードパターン調査）

**Identify the pattern:** （**パターンを特定します:**）
- What's the repeating structure? （繰り返し構造とは何ですか？）
- What are the variables? （変数とは何ですか?）
- How many unique combinations exist? （一意の組み合わせは何通り存在しますか?）

**Validate demand:** （**需要の検証:**）
- Aggregate search volume （集計検索ボリューム）
- Volume distribution (head vs. long tail) （体積分布 (ヘッド vs ロングテール)）
- Trend direction （トレンドの方向）

### 2. Data Requirements （2. データ要件）

**Identify data sources:** （**データ ソースを特定する:**）
- What data populates each page? （各ページにはどのようなデータが入力されますか?）
- Is it first-party, scraped, licensed, public? （それはファーストパーティ、スクレイピング、ライセンス、パブリックですか?）
- How is it updated? （どのように更新されますか?）

### 3. Template Design （3. テンプレートのデザイン）

**Page structure:** （**ページ構造:**）
- Header with target keyword （ターゲットキーワードを含むヘッダー）
- Unique intro (not just variables swapped) （ユニークなイントロ (変数が交換されるだけではありません)）
- Data-driven sections （データドリブンセクション）
- Related pages / internal links （関連ページ・内部リンク）
- CTAs appropriate to intent （意図に応じたCTA）

**Ensuring uniqueness:** （**一意性の確保:**）
- Each page needs unique value （各ページには一意の値が必要です）
- Conditional content based on data （データに基づいた条件付きコンテンツ）
- Original insights/analysis per page （ページごとの独自の洞察/分析）

### 4. Internal Linking Architecture （4. 内部リンクのアーキテクチャ）

**Hub and spoke model:** （**ハブアンドスポークモデル:**）
- Hub: Main category page （ハブ: メイン カテゴリ ページ）
- Spokes: Individual programmatic pages （スポーク: 個々のプログラム ページ）
- Cross-links between related spokes （関連するスポーク間のクロスリンク）

**Avoid orphan pages:** （**孤立したページを避ける:**）
- Every page reachable from main site （メインサイトからアクセス可能なすべてのページ）
- XML sitemap for all pages （すべてのページの XML サイトマップ）
- Breadcrumbs with structured data （構造化データを含むブレッドクラム）

### 5. Indexation Strategy （5. インデックス戦略）

- Prioritize high-volume patterns （大量のパターンを優先する）
- Noindex very thin variations （Noindex の非常に薄いバリエーション）
- Manage crawl budget thoughtfully （クロール予算を慎重に管理する）
- Separate sitemaps by page type （ページの種類ごとにサイトマップを分ける）

---

## Quality Checks （品質チェック）

### Pre-Launch Checklist （発売前チェックリスト）

**Content quality:** （**コンテンツの品質:**）
- [ ] Each page provides unique value （[ ] 各ページは独自の価値を提供します）
- [ ] Answers search intent （[ ] 回答の検索意図）
- [ ] Readable and useful （[ ] 読みやすくて役に立つ）

**Technical SEO:** （**テクニカルSEO:**）
- [ ] Unique titles and meta descriptions （[ ] 固有のタイトルとメタディスクリプション）
- [ ] Proper heading structure （[ ] 適切な見出し構造）
- [ ] Schema markup implemented （[ ] スキーマ マークアップが実装されました）
- [ ] Page speed acceptable （[ ] ページ速度は許容範囲内）

**Internal linking:** （**内部リンク:**）
- [ ] Connected to site architecture （[ ] サイト アーキテクチャに接続されています）
- [ ] Related pages linked （[ ] 関連ページリンク）
- [ ] No orphan pages （[ ] 孤立ページはありません）

**Indexation:** （**インデックス:**）
- [ ] In XML sitemap （[ ] XML サイトマップ内）
- [ ] Crawlable （[ ] クロール可能）
- [ ] No conflicting noindex （[ ] 競合する noindex はありません）

### Post-Launch Monitoring （打ち上げ後のモニタリング）

Track: Indexation rate, Rankings, Traffic, Engagement, Conversion （追跡: インデックス化率、ランキング、トラフィック、エンゲージメント、コンバージョン）

Watch for: Thin content warnings, Ranking drops, Manual actions, Crawl errors （注意: 内容の薄い警告、ランキングの低下、手動操作、クロール エラー）

---

## Common Mistakes （よくある間違い）

- **Thin content**: Just swapping city names in identical content （**内容が薄い**: 同一のコンテンツ内の都市名を交換するだけです）
- **Keyword cannibalization**: Multiple pages targeting same keyword （**キーワードのカニバリゼーション**: 同じキーワードをターゲットとする複数のページ）
- **Over-generation**: Creating pages with no search demand （**過剰生成**: 検索需要のないページの作成）
- **Poor data quality**: Outdated or incorrect information （**データ品質が低い**: 古い情報または不正確な情報）
- **Ignoring UX**: Pages exist for Google, not users （**UX の無視**: ページはユーザーのためではなく、Google のために存在します。）

---

## Output Format （出力フォーマット）

### Strategy Document （戦略文書）
- Opportunity analysis （機会分析）
- Implementation plan （実施計画）
- Content guidelines （コンテンツガイドライン）

### Page Template （ページテンプレート）
- URL structure （URL構造）
- Title/meta templates （タイトル/メタテンプレート）
- Content outline （内容概要）
- Schema markup （スキーマのマークアップ）

---

## Task-Specific Questions （タスク固有の質問）

1. What keyword patterns are you targeting? （どのようなキーワード パターンをターゲットにしていますか?）
2. What data do you have (or can acquire)? （どのようなデータを持っていますか (または取得できますか)?）
3. How many pages are you planning? （何ページくらいを予定していますか？）
4. What does your site authority look like? （あなたのサイトの権限はどのようなものですか?）
5. Who currently ranks for these terms? （現在これらの用語でランク付けされているのは誰ですか?）
6. What's your technical stack? （あなたの技術スタックは何ですか?）

---

## Related Skills （関連スキル）

- **seo-audit**: For auditing programmatic pages after launch （**seo-audit**: 起動後のプログラマティック ページの監査用）
- **schema-markup**: For adding structured data （**schema-markup**: 構造化データの追加用）
- **competitor-alternatives**: For comparison page frameworks （**competitor-alternatives**: 比較ページのフレームワーク用）
