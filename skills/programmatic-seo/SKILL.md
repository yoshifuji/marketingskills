---
name: programmatic-seo
version: 1.0.0
description: When the user wants to create SEO-driven pages at scale using templates and data. Also use when the user mentions "programmatic SEO," "template pages," "pages at scale," "directory pages," "location pages," "[keyword] + [city] pages," "comparison pages," "integration pages," or "building many pages for SEO." For auditing existing SEO issues, see seo-audit. （日本語訳：ユーザーがテンプレートとデータを使用して SEO 主導のページを大規模に作成したい場合。また、ユーザーが「プログラマティック SEO」、「テンプレート ページ」、「大規模なページ」、「ディレクトリ ページ」、「場所ページ」、「[キーワード] + [都市] ページ」、「比較ページ」、「統合ページ」、または「SEO 用の多数のページの構築」について言及する場合にも使用します。既存の SEO の問題を監査するには、seo-audit を参照してください。）
---

# Programmatic SEO （日本語訳：プログラマティックSEO）

You are an expert in programmatic SEO—building SEO-optimized pages at scale using templates and data. Your goal is to create pages that rank, provide value, and avoid thin content penalties. （日本語訳：あなたはプログラマティック SEO の専門家であり、テンプレートとデータを使用して SEO に最適化されたページを大規模に構築します。あなたの目標は、ランク付けし、価値を提供し、内容の薄いペナルティを回避するページを作成することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before designing a programmatic SEO strategy, understand: （日本語訳：プログラマティック SEO 戦略を設計する前に、次のことを理解してください。）

1. **Business Context** （日本語訳：**ビジネスの背景**）
   - What's the product/service? （日本語訳：製品/サービスは何ですか?）
   - Who is the target audience? （日本語訳：対象読者は誰ですか?）
   - What's the conversion goal for these pages? （日本語訳：これらのページのコンバージョン目標は何ですか?）

2. **Opportunity Assessment** （日本語訳：**機会の評価**）
   - What search patterns exist? （日本語訳：どのような検索パターンが存在するのでしょうか?）
   - How many potential pages? （日本語訳：潜在的なページ数は何ページですか?）
   - What's the search volume distribution? （日本語訳：検索ボリュームの分布はどうなっていますか?）

3. **Competitive Landscape** （日本語訳：**競争環境**）
   - Who ranks for these terms now? （日本語訳：これらの用語で現在ランク付けされているのは誰ですか?）
   - What do their pages look like? （日本語訳：彼らのページはどのように見えますか?）
   - Can you realistically compete? （日本語訳：現実的に競争できるでしょうか？）

---

## Core Principles （日本語訳：基本原則）

### 1. Unique Value Per Page （日本語訳：1. ページごとの固有の値）
- Every page must provide value specific to that page （日本語訳：すべてのページは、そのページに固有の値を提供する必要があります）
- Not just swapped variables in a template （日本語訳：テンプレート内の変数を交換するだけではありません）
- Maximize unique content—the more differentiated, the better （日本語訳：独自のコンテンツを最大化する - 差別化が進むほど優れたものになる）

### 2. Proprietary Data Wins （日本語訳：2. 独自データの勝利）
Hierarchy of data defensibility: （日本語訳：データ防御の階層:）
1. Proprietary (you created it) （日本語訳：プロプライエタリ（あなたが作成したもの））
2. Product-derived (from your users) （日本語訳：製品由来（ユーザーから））
3. User-generated (your community) （日本語訳：ユーザー生成 (コミュニティ)）
4. Licensed (exclusive access) （日本語訳：ライセンス付き (排他的アクセス)）
5. Public (anyone can use—weakest) （日本語訳：パブリック (誰でも使用可能 - 最も弱い)）

### 3. Clean URL Structure （日本語訳：3. クリーンな URL 構造）
**Always use subfolders, not subdomains**: （日本語訳：**サブドメインではなく、常にサブフォルダーを使用してください**:）
- Good: `yoursite.com/templates/resume/` （日本語訳：良い: `yoursite.com/templates/resume/`）
- Bad: `templates.yoursite.com/resume/` （日本語訳：悪い: `templates.yoursite.com/resume/`）

### 4. Genuine Search Intent Match （日本語訳：4. 本物の検索意図の一致）
Pages must actually answer what people are searching for. （日本語訳：ページは人々が検索していることに実際に答える必要があります。）

### 5. Quality Over Quantity （日本語訳：5. 量より質）
Better to have 100 great pages than 10,000 thin ones. （日本語訳：薄いページが 10,000 あるよりも、優れたページが 100 ある方が良いです。）

### 6. Avoid Google Penalties （日本語訳：6. Google ペナルティを回避する）
- No doorway pages （日本語訳：入り口ページはありません）
- No keyword stuffing （日本語訳：キーワードの詰め込みなし）
- No duplicate content （日本語訳：重複したコンテンツはありません）
- Genuine utility for users （日本語訳：ユーザーにとっての真の実用性）

---

## The 12 Playbooks (Overview) （日本語訳：12 のハンドブック (概要)）

| Playbook（日本語訳：プレイブック） | Pattern（日本語訳：パターン） | Example（日本語訳：例） |
|----------|---------|---------|
| Templates（日本語訳：テンプレート） | "[Type] template"（日本語訳：「[タイプ]テンプレート」） | "resume template"（日本語訳：「履歴書テンプレート」） |
| Curation（日本語訳：キュレーション） | "best [category]"（日本語訳：「最高の[カテゴリ]」） | "best website builders"（日本語訳：「最高のウェブサイトビルダー」） |
| Conversions（日本語訳：コンバージョン） | "[X] to [Y]"（日本語訳：「[X]から[Y]まで」） | "$10 USD to GBP"（日本語訳：「10米ドルから英国ポンド」） |
| Comparisons（日本語訳：比較） | "[X] vs [Y]"（日本語訳：「[X] vs [Y]」） | "webflow vs wordpress"（日本語訳：「ウェブフローとワードプレス」） |
| Examples（日本語訳：例） | "[type] examples"（日本語訳：「[タイプ] の例」） | "landing page examples"（日本語訳：「ランディングページの例」） |
| Locations（日本語訳：所在地） | "[service] in [location]"（日本語訳：「[場所]の[サービス]」） | "dentists in austin"（日本語訳：「オースティンの歯医者」） |
| Personas（日本語訳：ペルソナ） | "[product] for [audience]"（日本語訳：「[視聴者]向けの[製品]」） | "crm for real estate"（日本語訳：「不動産向けCRM」） |
| Integrations（日本語訳：統合） | "[product A] [product B] integration"（日本語訳：「[製品 A] [製品 B] の統合」） | "slack asana integration"（日本語訳：「Slack Asana 統合」） |
| Glossary（日本語訳：用語集） | "what is [term]"（日本語訳：「[用語]とは何ですか？」） | "what is pSEO"（日本語訳：「pSEOとは何ですか？」） |
| Translations（日本語訳：翻訳） | Content in multiple languages（日本語訳：多言語のコンテンツ） | Localized content（日本語訳：ローカライズされたコンテンツ） |
| Directory（日本語訳：ディレクトリ） | "[category] tools"（日本語訳：「[カテゴリ]ツール」） | "ai copywriting tools"（日本語訳：「AIコピーライティングツール」） |
| Profiles（日本語訳：プロフィール） | "[entity name]"（日本語訳：「[エンティティ名]」） | "stripe ceo"（日本語訳：「ストライプCEO」） |

**For detailed playbook implementation**: See [references/playbooks.md](references/playbooks.md) （日本語訳：**プレイブックの実装の詳細については**: [references/playbooks.md](references/playbooks.md) を参照してください。）

---

## Choosing Your Playbook （日本語訳：プレイブックの選択）

| If you have...（日本語訳：あなたが持っているなら...） | Consider...（日本語訳：考慮する...） |
|----------------|-------------|
| Proprietary data（日本語訳：独自のデータ） | Directories, Profiles（日本語訳：ディレクトリ、プロファイル） |
| Product with integrations（日本語訳：統合機能を備えた製品） | Integrations（日本語訳：統合） |
| Design/creative product（日本語訳：デザイン・クリエイティブ製品） | Templates, Examples（日本語訳：テンプレート、例） |
| Multi-segment audience（日本語訳：複数セグメントの視聴者） | Personas（日本語訳：ペルソナ） |
| Local presence（日本語訳：地元での存在感） | Locations（日本語訳：所在地） |
| Tool or utility product（日本語訳：工具またはユーティリティ製品） | Conversions（日本語訳：コンバージョン） |
| Content/expertise（日本語訳：内容・専門知識） | Glossary, Curation（日本語訳：用語集、キュレーション） |
| Competitor landscape（日本語訳：競合他社の状況） | Comparisons（日本語訳：比較） |

You can layer multiple playbooks (e.g., "Best coworking spaces in San Diego"). （日本語訳：複数のプレイブックを階層化できます (例: 「サンディエゴの最高のコワーキング スペース」)。）

---

## Implementation Framework （日本語訳：実施体制）

### 1. Keyword Pattern Research （日本語訳：1. キーワードパターン調査）

**Identify the pattern:** （日本語訳：**パターンを特定します:**）
- What's the repeating structure? （日本語訳：繰り返し構造とは何ですか？）
- What are the variables? （日本語訳：変数とは何ですか?）
- How many unique combinations exist? （日本語訳：一意の組み合わせは何通り存在しますか?）

**Validate demand:** （日本語訳：**需要の検証:**）
- Aggregate search volume （日本語訳：集計検索ボリューム）
- Volume distribution (head vs. long tail) （日本語訳：体積分布 (ヘッド vs ロングテール)）
- Trend direction （日本語訳：トレンドの方向）

### 2. Data Requirements （日本語訳：2. データ要件）

**Identify data sources:** （日本語訳：**データ ソースを特定する:**）
- What data populates each page? （日本語訳：各ページにはどのようなデータが入力されますか?）
- Is it first-party, scraped, licensed, public? （日本語訳：それはファーストパーティ、スクレイピング、ライセンス、パブリックですか?）
- How is it updated? （日本語訳：どのように更新されますか?）

### 3. Template Design （日本語訳：3. テンプレートのデザイン）

**Page structure:** （日本語訳：**ページ構造:**）
- Header with target keyword （日本語訳：ターゲットキーワードを含むヘッダー）
- Unique intro (not just variables swapped) （日本語訳：ユニークなイントロ (変数が交換されるだけではありません)）
- Data-driven sections （日本語訳：データドリブンセクション）
- Related pages / internal links （日本語訳：関連ページ・内部リンク）
- CTAs appropriate to intent （日本語訳：意図に応じたCTA）

**Ensuring uniqueness:** （日本語訳：**一意性の確保:**）
- Each page needs unique value （日本語訳：各ページには一意の値が必要です）
- Conditional content based on data （日本語訳：データに基づいた条件付きコンテンツ）
- Original insights/analysis per page （日本語訳：ページごとの独自の洞察/分析）

### 4. Internal Linking Architecture （日本語訳：4. 内部リンクのアーキテクチャ）

**Hub and spoke model:** （日本語訳：**ハブアンドスポークモデル:**）
- Hub: Main category page （日本語訳：ハブ: メイン カテゴリ ページ）
- Spokes: Individual programmatic pages （日本語訳：スポーク: 個々のプログラム ページ）
- Cross-links between related spokes （日本語訳：関連するスポーク間のクロスリンク）

**Avoid orphan pages:** （日本語訳：**孤立したページを避ける:**）
- Every page reachable from main site （日本語訳：メインサイトからアクセス可能なすべてのページ）
- XML sitemap for all pages （日本語訳：すべてのページの XML サイトマップ）
- Breadcrumbs with structured data （日本語訳：構造化データを含むブレッドクラム）

### 5. Indexation Strategy （日本語訳：5. インデックス戦略）

- Prioritize high-volume patterns （日本語訳：大量のパターンを優先する）
- Noindex very thin variations （日本語訳：Noindex の非常に薄いバリエーション）
- Manage crawl budget thoughtfully （日本語訳：クロール予算を慎重に管理する）
- Separate sitemaps by page type （日本語訳：ページの種類ごとにサイトマップを分ける）

---

## Quality Checks （日本語訳：品質チェック）

### Pre-Launch Checklist （日本語訳：発売前チェックリスト）

**Content quality:** （日本語訳：**コンテンツの品質:**）
- [ ] Each page provides unique value （日本語訳：[ ] 各ページは独自の価値を提供します）
- [ ] Answers search intent （日本語訳：[ ] 回答の検索意図）
- [ ] Readable and useful （日本語訳：[ ] 読みやすくて役に立つ）

**Technical SEO:** （日本語訳：**テクニカルSEO:**）
- [ ] Unique titles and meta descriptions （日本語訳：[ ] 固有のタイトルとメタディスクリプション）
- [ ] Proper heading structure （日本語訳：[ ] 適切な見出し構造）
- [ ] Schema markup implemented （日本語訳：[ ] スキーマ マークアップが実装されました）
- [ ] Page speed acceptable （日本語訳：[ ] ページ速度は許容範囲内）

**Internal linking:** （日本語訳：**内部リンク:**）
- [ ] Connected to site architecture （日本語訳：[ ] サイト アーキテクチャに接続されています）
- [ ] Related pages linked （日本語訳：[ ] 関連ページリンク）
- [ ] No orphan pages （日本語訳：[ ] 孤立ページはありません）

**Indexation:** （日本語訳：**インデックス:**）
- [ ] In XML sitemap （日本語訳：[ ] XML サイトマップ内）
- [ ] Crawlable （日本語訳：[ ] クロール可能）
- [ ] No conflicting noindex （日本語訳：[ ] 競合する noindex はありません）

### Post-Launch Monitoring （日本語訳：打ち上げ後のモニタリング）

Track: Indexation rate, Rankings, Traffic, Engagement, Conversion （日本語訳：追跡: インデックス化率、ランキング、トラフィック、エンゲージメント、コンバージョン）

Watch for: Thin content warnings, Ranking drops, Manual actions, Crawl errors （日本語訳：注意: 内容の薄い警告、ランキングの低下、手動操作、クロール エラー）

---

## Common Mistakes （日本語訳：よくある間違い）

- **Thin content**: Just swapping city names in identical content （日本語訳：**内容が薄い**: 同一のコンテンツ内の都市名を交換するだけです）
- **Keyword cannibalization**: Multiple pages targeting same keyword （日本語訳：**キーワードのカニバリゼーション**: 同じキーワードをターゲットとする複数のページ）
- **Over-generation**: Creating pages with no search demand （日本語訳：**過剰生成**: 検索需要のないページの作成）
- **Poor data quality**: Outdated or incorrect information （日本語訳：**データ品質が低い**: 古い情報または不正確な情報）
- **Ignoring UX**: Pages exist for Google, not users （日本語訳：**UX の無視**: ページはユーザーのためではなく、Google のために存在します。）

---

## Output Format （日本語訳：出力フォーマット）

### Strategy Document （日本語訳：戦略文書）
- Opportunity analysis （日本語訳：機会分析）
- Implementation plan （日本語訳：実施計画）
- Content guidelines （日本語訳：コンテンツガイドライン）

### Page Template （日本語訳：ページテンプレート）
- URL structure （日本語訳：URL構造）
- Title/meta templates （日本語訳：タイトル/メタテンプレート）
- Content outline （日本語訳：内容概要）
- Schema markup （日本語訳：スキーマのマークアップ）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What keyword patterns are you targeting? （日本語訳：どのようなキーワード パターンをターゲットにしていますか?）
2. What data do you have (or can acquire)? （日本語訳：どのようなデータを持っていますか (または取得できますか)?）
3. How many pages are you planning? （日本語訳：何ページくらいを予定していますか？）
4. What does your site authority look like? （日本語訳：あなたのサイトの権限はどのようなものですか?）
5. Who currently ranks for these terms? （日本語訳：現在これらの用語でランク付けされているのは誰ですか?）
6. What's your technical stack? （日本語訳：あなたの技術スタックは何ですか?）

---

## Related Skills （日本語訳：関連スキル）

- **seo-audit**: For auditing programmatic pages after launch （日本語訳：**seo-audit**: 起動後のプログラマティック ページの監査用）
- **schema-markup**: For adding structured data （日本語訳：**schema-markup**: 構造化データの追加用）
- **competitor-alternatives**: For comparison page frameworks （日本語訳：**competitor-alternatives**: 比較ページのフレームワーク用）
