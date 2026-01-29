# Content Architecture for Competitor Pages （日本語訳：競合他社のページのコンテンツ アーキテクチャ）

How to structure and maintain competitor data for scalable comparison pages. （日本語訳：スケーラブルな比較ページ用に競合他社のデータを構造化して維持する方法。）

## Centralized Competitor Data （日本語訳：一元化された競合他社データ）

Create a single source of truth for each competitor: （日本語訳：競合他社ごとに単一の信頼できる情報源を作成します。）

```
competitor_data/
├── notion.md
├── airtable.md
├── monday.md
└── ...
```

---

## Competitor Data Template （日本語訳：競合他社のデータテンプレート）

Per competitor, document: （日本語訳：競合他社ごとに、次の文書を作成します。）

```yaml
name: Notion
website: notion.so
tagline: "The all-in-one workspace"
founded: 2016
headquarters: San Francisco

# Positioning
primary_use_case: "docs + light databases"
target_audience: "teams wanting flexible workspace"
market_position: "premium, feature-rich"

# Pricing
pricing_model: per-seat
free_tier: true
free_tier_limits: "limited blocks, 1 user"
starter_price: $8/user/month
business_price: $15/user/month
enterprise: custom

# Features (rate 1-5 or describe)
features:
  documents: 5
  databases: 4
  project_management: 3
  collaboration: 4
  integrations: 3
  mobile_app: 3
  offline_mode: 2
  api: 4

# Strengths (be honest)
strengths:
  - Extremely flexible and customizable
  - Beautiful, modern interface
  - Strong template ecosystem
  - Active community

# Weaknesses (be fair)
weaknesses:
  - Can be slow with large databases
  - Learning curve for advanced features
  - Limited automations compared to dedicated tools
  - Offline mode is limited

# Best for
best_for:
  - Teams wanting all-in-one workspace
  - Content-heavy workflows
  - Documentation-first teams
  - Startups and small teams

# Not ideal for
not_ideal_for:
  - Complex project management needs
  - Large databases (1000s of rows)
  - Teams needing robust offline
  - Enterprise with strict compliance

# Common complaints (from reviews)
common_complaints:
  - "Gets slow with lots of content"
  - "Hard to find things as workspace grows"
  - "Mobile app is clunky"

# Migration notes
migration_from:
  difficulty: medium
  data_export: "Markdown, CSV, HTML"
  what_transfers: "Pages, databases"
  what_doesnt: "Automations, integrations setup"
  time_estimate: "1-3 days for small team"
```

---

## Your Product Data （日本語訳：製品データ）

Same structure for yourself—be honest: （日本語訳：あなた自身も同じ構造です。正直に言ってください。）

```yaml
name: [Your Product]
# ... same fields

strengths:
  - [Your real strengths]

weaknesses:
  - [Your honest weaknesses]

best_for:
  - [Your ideal customers]

not_ideal_for:
  - [Who should use something else]
```

---

## Page Generation （日本語訳：ページの生成）

Each page pulls from centralized data: （日本語訳：各ページは一元化されたデータから取得します。）

- **[Competitor] Alternative page**: Pulls competitor data + your data （日本語訳：**[競合他社] 代替ページ**: 競合他社のデータとお客様のデータを取得します）
- **[Competitor] Alternatives page**: Pulls competitor data + your data + other alternatives （日本語訳：**[競合他社] 代替案ページ**: 競合他社のデータ + 自社のデータ + 他の代替案を取得します）
- **You vs [Competitor] page**: Pulls your data + competitor data （日本語訳：**あなた vs [競合他社] ページ**: 自社のデータと競合他社のデータを取得します）
- **[A] vs [B] page**: Pulls both competitor data + your data （日本語訳：**[A] ページと [B] ページ**: 競合他社のデータと自社のデータの両方を取得します）

**Benefits**: （日本語訳：**利点**：）
- Update competitor pricing once, updates everywhere （日本語訳：競合他社の価格を一度更新すれば、どこでも更新できます）
- Add new feature comparison once, appears on all pages （日本語訳：新しい機能の比較を一度追加すると、すべてのページに表示されます）
- Consistent accuracy across pages （日本語訳：ページ全体で一貫した精度）
- Easier to maintain at scale （日本語訳：大規模なメンテナンスが容易になる）

---

## Index Page Structure （日本語訳：インデックスページの構造）

### Alternatives Index （日本語訳：代替インデックス）

**URL**: `/alternatives` or `/alternatives/index` （日本語訳：**URL**: `/alternatives` または `/alternatives/index`）

**Purpose**: Lists all "[Competitor] Alternative" pages （日本語訳：**目的**: すべての「[競合他社] 代替」ページをリストします。）

**Page structure**: （日本語訳：**ページ構造**:）
1. Headline: "[Your Product] as an Alternative" （日本語訳：見出し: 「[貴社​​の製品] が代替品として」）
2. Brief intro on why people switch to you （日本語訳：人々があなたに乗り換える理由についての簡単な紹介）
3. List of all alternative pages with: （日本語訳：すべての代替ページのリスト:）
   - Competitor name/logo （日本語訳：競合他社の名前/ロゴ）
   - One-line summary of key differentiator vs. that competitor （日本語訳：主要な差別化要因と競合他社の概要を 1 行でまとめたもの）
   - Link to full comparison （日本語訳：完全な比較へのリンク）
4. Common reasons people switch (aggregated) （日本語訳：人が乗り換える一般的な理由 (集計)）
5. CTA （日本語訳：CTA）

**Example**: （日本語訳：**例**：）
```markdown
## Explore [Your Product] as an Alternative

Looking to switch? See how [Your Product] compares to the tools you're evaluating:

- **[Notion Alternative](/alternatives/notion)** — Better for teams who need [X]
- **[Airtable Alternative](/alternatives/airtable)** — Better for teams who need [Y]
- **[Monday Alternative](/alternatives/monday)** — Better for teams who need [Z]
```

---

### Vs Comparisons Index （日本語訳：対比較インデックス）

**URL**: `/vs` or `/compare` （日本語訳：**URL**: `/vs` または `/compare`）

**Purpose**: Lists all "You vs [Competitor]" and "[A] vs [B]" pages （日本語訳：**目的**: すべての「あなた vs [競合他社]」および「[A] vs [B]」ページをリストします。）

**Page structure**: （日本語訳：**ページ構造**:）
1. Headline: "Compare [Your Product]" （日本語訳：見出し: 「[製品] を比較してください」）
2. Section: "[Your Product] vs Competitors" — list of direct comparisons （日本語訳：セクション: 「[貴社​​の製品] と競合他社」 - 直接比較のリスト）
3. Section: "Head-to-Head Comparisons" — list of [A] vs [B] pages （日本語訳：セクション: 「直接比較」 - [A] ページと [B] ページのリスト）
4. Brief methodology note （日本語訳：方法論の簡単なメモ）
5. CTA （日本語訳：CTA）

---

### Index Page Best Practices （日本語訳：インデックスページのベストプラクティス）

**Keep them updated**: When you add a new comparison page, add it to the relevant index. （日本語訳：**常に最新の状態に保ってください**: 新しい比較ページを追加するときは、関連するインデックスに追加します。）

**Internal linking**: （日本語訳：**内部リンク**:）
- Link from index → individual pages （日本語訳：目次→個別ページからリンク）
- Link from individual pages → back to index （日本語訳：各ページからリンク → 目次に戻る）
- Cross-link between related comparisons （日本語訳：関連する比較間の相互リンク）

**SEO value**: （日本語訳：**SEO の価値**:）
- Index pages can rank for broad terms like "project management tool comparisons" （日本語訳：インデックス ページは、「プロジェクト管理ツールの比較」などの広範な用語でランク付けできます。）
- Pass link equity to individual comparison pages （日本語訳：リンクの資産を個々の比較ページに渡す）
- Help search engines discover all comparison content （日本語訳：検索エンジンがすべての比較コンテンツを発見できるようにする）

**Sorting options**: （日本語訳：**並べ替えオプション**:）
- By popularity (search volume) （日本語訳：人気順（検索ボリューム））
- Alphabetically （日本語訳：アルファベット順）
- By category/use case （日本語訳：カテゴリ/ユースケース別）
- By date added (show freshness) （日本語訳：追加日順 (鮮度を表示)）

**Include on index pages**: （日本語訳：**インデックス ページに含める**:）
- Last updated date for credibility （日本語訳：信頼性のための最終更新日）
- Number of pages/comparisons available （日本語訳：ページ数/比較可能）
- Quick filters if you have many comparisons （日本語訳：多くの比較がある場合のクイックフィルター）

---

## Footer Navigation （日本語訳：フッターナビゲーション）

The site footer appears on all marketing pages, making it a powerful internal linking opportunity for competitor pages. （日本語訳：サイト フッターはすべてのマーケティング ページに表示されるため、競合他社のページにとって強力な内部リンクの機会となります。）

### Option 1: Link to Index Pages (Minimum) （日本語訳：オプション 1: インデックス ページへのリンク (最小)）

At minimum, add links to your comparison index pages in the footer: （日本語訳：少なくとも、比較インデックス ページへのリンクをフッターに追加します。）

```
Footer
├── Compare
│   ├── Alternatives →  /alternatives
│   └── Comparisons →  /vs
```

This ensures every marketing page passes link equity to your comparison content hub. （日本語訳：これにより、すべてのマーケティング ページがリンク エクイティを比較コンテンツ ハブに確実に渡します。）

### Option 2: Footer Columns by Format (Recommended for SEO) （日本語訳：オプション 2: フォーマット別のフッター列 (SEO に推奨)）

For stronger internal linking, create dedicated footer columns for each format you've built, linking directly to your top competitors: （日本語訳：内部リンクを強化するには、作成したフォーマットごとに専用のフッター列を作成し、上位の競合他社に直接リンクします。）

```
Footer
├── [Product] vs               ├── Alternatives to            ├── Compare
│   ├── vs Notion              │   ├── Notion Alternative     │   ├── Notion vs Airtable
│   ├── vs Airtable            │   ├── Airtable Alternative   │   ├── Monday vs Asana
│   ├── vs Monday              │   ├── Monday Alternative     │   ├── Notion vs Monday
│   ├── vs Asana               │   ├── Asana Alternative      │   ├── ...
│   ├── vs Clickup             │   ├── Clickup Alternative    │   └── View all →
│   ├── ...                    │   ├── ...                    │
│   └── View all →             │   └── View all →             │
```

**Guidelines**: （日本語訳：**ガイドライン**:）
- Include up to 8 links per column (top competitors by search volume) （日本語訳：列ごとに最大 8 つのリンクを含めます (検索ボリュームで上位の競合他社)）
- Add "View all" link to the full index page （日本語訳：完全なインデックス ページに「すべて表示」リンクを追加します。）
- Only create columns for formats you've actually built pages for （日本語訳：実際にページを作成したフォーマットの列のみを作成してください）
- Prioritize competitors with highest search volume （日本語訳：検索ボリュームが最も多い競合他社を優先する）

### Why Footer Links Matter （日本語訳：フッターリンクが重要な理由）

1. **Sitewide distribution**: Footer links appear on every marketing page, passing link equity from your entire site to comparison content （日本語訳：**サイト全体への配布**: フッター リンクはすべてのマーケティング ページに表示され、サイト全体のリンク エクイティが比較コンテンツに渡されます。）
2. **Crawl efficiency**: Search engines discover all comparison pages quickly （日本語訳：**クロール効率**: 検索エンジンはすべての比較ページを迅速に検出します）
3. **User discovery**: Visitors evaluating your product can easily find comparisons （日本語訳：**ユーザー発見**: 製品を評価している訪問者は、比較を簡単に見つけることができます）
4. **Competitive positioning**: Signals to search engines that you're a key player in the space （日本語訳：**競争力のあるポジショニング**: あなたがこの分野の主要なプレーヤーであることを検索エンジンに知らせます）

### Implementation Notes （日本語訳：実装メモ）

- Update footer when adding new high-priority comparison pages （日本語訳：新しい優先度の高い比較ページを追加するときにフッターを更新する）
- Keep footer clean—don't list every comparison, just the top ones （日本語訳：フッターをすっきりさせてください。すべての比較をリストするのではなく、上位のものだけをリストします。）
- Match column headers to your URL structure (e.g., "vs" column → `/vs/` URLs) （日本語訳：列ヘッダーを URL 構造に一致させます (例: 「vs」列 → `/vs/` URL)）
- Consider mobile: columns may stack, so order by priority （日本語訳：モバイルを考慮してください: 列は積み重ねられる可能性があるため、優先順位に従って並べ替えます。）
