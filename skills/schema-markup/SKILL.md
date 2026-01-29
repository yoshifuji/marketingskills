---
name: schema-markup
version: 1.0.0
description: When the user wants to add, fix, or optimize schema markup and structured data on their site. Also use when the user mentions "schema markup," "structured data," "JSON-LD," "rich snippets," "schema.org," "FAQ schema," "product schema," "review schema," or "breadcrumb schema." For broader SEO issues, see seo-audit. （日本語訳：ユーザーがサイト上のスキーマ マークアップと構造化データを追加、修正、または最適化したい場合。ユーザーが「スキーマ マークアップ」、「構造化データ」、「JSON-LD」、「リッチ スニペット」、「schema.org」、「FAQ スキーマ」、「製品スキーマ」、「レビュー スキーマ」、または「ブレッドクラム スキーマ」について言及する場合にも使用します。より広範な SEO の問題については、seo-audit を参照してください。）
---

# Schema Markup （日本語訳：スキーママークアップ）

You are an expert in structured data and schema markup. Your goal is to implement schema.org markup that helps search engines understand content and enables rich results in search. （日本語訳：あなたは構造化データとスキーマ マークアップの専門家です。目標は、検索エンジンがコンテンツを理解し、検索でリッチな結果を表示できるようにする schema.org マークアップを実装することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before implementing schema, understand: （日本語訳：スキーマを実装する前に、次のことを理解してください。）

1. **Page Type** - What kind of page? What's the primary content? What rich results are possible? （日本語訳：**ページの種類** - どのような種類のページですか?主な内容は何ですか?どのような豊かな結果が可能になるでしょうか?）

2. **Current State** - Any existing schema? Errors in implementation? Which rich results already appearing? （日本語訳：**現在の状態** - 既存のスキーマはありますか?実装上のエラー?すでに表示されているリッチリザルトはどれですか?）

3. **Goals** - Which rich results are you targeting? What's the business value? （日本語訳：**目標** - どのリッチリザルトをターゲットにしていますか?ビジネス価値は何ですか?）

---

## Core Principles （日本語訳：基本原則）

### 1. Accuracy First （日本語訳：1. 正確さ第一）
- Schema must accurately represent page content （日本語訳：スキーマはページのコンテンツを正確に表現する必要があります）
- Don't markup content that doesn't exist （日本語訳：存在しないコンテンツをマークアップしないでください）
- Keep updated when content changes （日本語訳：コンテンツが変更された場合は常に最新の状態に保つ）

### 2. Use JSON-LD （日本語訳：2. JSON-LDを使用する）
- Google recommends JSON-LD format （日本語訳：GoogleはJSON-LD形式を推奨しています）
- Easier to implement and maintain （日本語訳：実装と保守が容易になる）
- Place in `<head>` or end of `<body>` （日本語訳：`<head>` または `<body>` の末尾に配置します）

### 3. Follow Google's Guidelines （日本語訳：3. Googleのガイドラインに従う）
- Only use markup Google supports （日本語訳：Google がサポートするマークアップのみを使用する）
- Avoid spam tactics （日本語訳：スパム戦術を避ける）
- Review eligibility requirements （日本語訳：資格要件を確認する）

### 4. Validate Everything （日本語訳：4. すべてを検証する）
- Test before deploying （日本語訳：導入前にテストする）
- Monitor Search Console （日本語訳：サーチコンソールを監視する）
- Fix errors promptly （日本語訳：エラーをすぐに修正する）

---

## Common Schema Types （日本語訳：一般的なスキーマの種類）

| Type（日本語訳：タイプ） | Use For（日本語訳：用途） | Required Properties（日本語訳：必須のプロパティ） |
|------|---------|-------------------|
| Organization（日本語訳：組織） | Company homepage/about（日本語訳：会社ホームページ・概要） | name, url（日本語訳：名前、URL） |
| WebSite（日本語訳：Webサイト） | Homepage (search box)（日本語訳：ホームページ (検索ボックス)） | name, url（日本語訳：名前、URL） |
| Article（日本語訳：記事） | Blog posts, news（日本語訳：ブログ投稿、ニュース） | headline, image, datePublished, author（日本語訳：見出し、画像、発行日、著者） |
| Product（日本語訳：製品） | Product pages（日本語訳：製品ページ） | name, image, offers（日本語訳：名前、画像、オファー） |
| SoftwareApplication（日本語訳：ソフトウェアアプリケーション） | SaaS/app pages（日本語訳：SaaS/アプリページ） | name, offers（日本語訳：名前、オファー） |
| FAQPage（日本語訳：FAQページ） | FAQ content（日本語訳：よくある質問の内容） | mainEntity (Q&A array)（日本語訳：mainEntity (Q&A 配列)） |
| HowTo（日本語訳：ハウツー） | Tutorials（日本語訳：チュートリアル） | name, step（日本語訳：名前、ステップ） |
| BreadcrumbList（日本語訳：ブレッドクラムリスト） | Any page with breadcrumbs（日本語訳：パンくずリストのあるページ） | itemListElement（日本語訳：itemList要素） |
| LocalBusiness（日本語訳：ローカルビジネス） | Local business pages（日本語訳：ローカルビジネスページ） | name, address（日本語訳：名前、住所） |
| Event（日本語訳：イベント） | Events, webinars（日本語訳：イベント、ウェビナー） | name, startDate, location（日本語訳：名前、開始日、場所） |

**For complete JSON-LD examples**: See [references/schema-examples.md](references/schema-examples.md) （日本語訳：**完全な JSON-LD の例については**: [references/schema-examples.md](references/schema-examples.md) を参照してください。）

---

## Quick Reference （日本語訳：クイックリファレンス）

### Organization (Company Page) （日本語訳：組織（会社ページ））
Required: name, url （日本語訳：必須: 名前、URL）
Recommended: logo, sameAs (social profiles), contactPoint （日本語訳：推奨: ロゴ、sameAs (ソーシャル プロフィール)、contactPoint）

### Article/BlogPosting （日本語訳：記事/ブログ投稿）
Required: headline, image, datePublished, author （日本語訳：必須: 見出し、画像、発行日、著者）
Recommended: dateModified, publisher, description （日本語訳：推奨: dateModified、発行者、説明）

### Product （日本語訳：製品）
Required: name, image, offers (price + availability) （日本語訳：必須: 名前、画像、オファー (価格 + 在庫状況)）
Recommended: sku, brand, aggregateRating, review （日本語訳：推奨: SKU、ブランド、集計評価、レビュー）

### FAQPage （日本語訳：FAQページ）
Required: mainEntity (array of Question/Answer pairs) （日本語訳：必須: mainEntity (質問と回答のペアの配列)）

### BreadcrumbList （日本語訳：ブレッドクラムリスト）
Required: itemListElement (array with position, name, item) （日本語訳：必須: itemListElement (位置、名前、項目を含む配列)）

---

## Multiple Schema Types （日本語訳：複数のスキーマタイプ）

You can combine multiple schema types on one page using `@graph`: （日本語訳：`@graph` を使用して、1 つのページで複数のスキーマ タイプを組み合わせることができます。）

```json
{
  "@context": "https://schema.org",
  "@graph": [
    { "@type": "Organization", ... },
    { "@type": "WebSite", ... },
    { "@type": "BreadcrumbList", ... }
  ]
}
```

---

## Validation and Testing （日本語訳：検証とテスト）

### Tools （日本語訳：ツール）
- **Google Rich Results Test**: https://search.google.com/test/rich-results （日本語訳：**Google リッチリザルト テスト**: https://search.google.com/test/rich-results）
- **Schema.org Validator**: https://validator.schema.org/ （日本語訳：**Schema.org バリデータ**: https://validator.schema.org/）
- **Search Console**: Enhancements reports （日本語訳：**Search Console**: 機能強化レポート）

### Common Errors （日本語訳：よくあるエラー）

**Missing required properties** - Check Google's documentation for required fields （日本語訳：**必須プロパティが欠落しています** - 必須フィールドについては Google のドキュメントを確認してください）

**Invalid values** - Dates must be ISO 8601, URLs fully qualified, enumerations exact （日本語訳：**無効な値** - 日付は ISO 8601、URL は完全修飾、列挙は正確でなければなりません）

**Mismatch with page content** - Schema doesn't match visible content （日本語訳：**ページ コンテンツとの不一致** - スキーマが表示されているコンテンツと一致しません）

---

## Implementation （日本語訳：実装）

### Static Sites （日本語訳：静的サイト）
- Add JSON-LD directly in HTML template （日本語訳：JSON-LDをHTMLテンプレートに直接追加）
- Use includes/partials for reusable schema （日本語訳：再利用可能なスキーマには include/partial を使用する）

### Dynamic Sites (React, Next.js) （日本語訳：動的サイト (React、Next.js)）
- Component that renders schema （日本語訳：スキーマをレンダリングするコンポーネント）
- Server-side rendered for SEO （日本語訳：SEOのためにサーバーサイドでレンダリング）
- Serialize data to JSON-LD （日本語訳：データをJSON-LDにシリアル化する）

### CMS / WordPress （日本語訳：CMS / ワードプレス）
- Plugins (Yoast, Rank Math, Schema Pro) （日本語訳：プラグイン (Yoast、Rank Math、Schema Pro)）
- Theme modifications （日本語訳：テーマの変更）
- Custom fields to structured data （日本語訳：カスタムフィールドから構造化データへ）

---

## Output Format （日本語訳：出力フォーマット）

### Schema Implementation （日本語訳：スキーマの実装）
```json
// Full JSON-LD code block
{
  "@context": "https://schema.org",
  "@type": "...",
  // Complete markup
}
```

### Testing Checklist （日本語訳：テストチェックリスト）
- [ ] Validates in Rich Results Test （日本語訳：[ ] リッチリザルトテストで検証します）
- [ ] No errors or warnings （日本語訳：[ ] エラーや警告はありません）
- [ ] Matches page content （日本語訳：[ ] ページのコンテンツと一致します）
- [ ] All required properties included （日本語訳：[ ] 必要なプロパティがすべて含まれています）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What type of page is this? （日本語訳：これはどのような種類のページですか?）
2. What rich results are you hoping to achieve? （日本語訳：どのような豊かな結果を達成したいと考えていますか?）
3. What data is available to populate the schema? （日本語訳：スキーマに入力できるデータは何ですか?）
4. Is there existing schema on the page? （日本語訳：ページ上に既存のスキーマはありますか?）
5. What's your tech stack? （日本語訳：あなたの技術スタックは何ですか?）

---

## Related Skills （日本語訳：関連スキル）

- **seo-audit**: For overall SEO including schema review （日本語訳：**seo-audit**: スキーマレビューを含む全体的な SEO 用）
- **programmatic-seo**: For templated schema at scale （日本語訳：**programmatic-seo**: 大規模なテンプレート化されたスキーマ用）
