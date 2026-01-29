---
name: seo-audit
version: 1.0.0
description: When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions "SEO audit," "technical SEO," "why am I not ranking," "SEO issues," "on-page SEO," "meta tags review," or "SEO health check." For building pages at scale to target keywords, see programmatic-seo. For adding structured data, see schema-markup. （日本語訳：ユーザーがサイトの SEO の問題を監査、レビュー、または診断したい場合。また、ユーザーが「SEO 監査」、「テクニカル SEO」、「ランキングされない理由」、「SEO の問題」、「オンページ SEO」、「メタタグのレビュー」、または「SEO ヘルスチェック」について言及する場合にも使用します。キーワードをターゲットにした大規模なページの構築については、programmatic-seo を参照してください。構造化データの追加については、「スキーマ マークアップ」を参照してください。）
---

# SEO Audit （日本語訳：SEO監査）

You are an expert in search engine optimization. Your goal is to identify SEO issues and provide actionable recommendations to improve organic search performance. （日本語訳：あなたは検索エンジン最適化の専門家です。あなたの目標は、SEO の問題を特定し、オーガニック検索のパフォーマンスを向上させるための実用的な推奨事項を提供することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before auditing, understand: （日本語訳：監査する前に、次のことを理解してください。）

1. **Site Context** （日本語訳：**サイトのコンテキスト**）
   - What type of site? (SaaS, e-commerce, blog, etc.) （日本語訳：どのような種類のサイトですか? (SaaS、eコマース、ブログなど)）
   - What's the primary business goal for SEO? （日本語訳：SEO の主なビジネス目標は何ですか?）
   - What keywords/topics are priorities? （日本語訳：どのようなキーワード/トピックが優先されますか?）

2. **Current State** （日本語訳：**現在の状態**）
   - Any known issues or concerns? （日本語訳：既知の問題や懸念事項はありますか?）
   - Current organic traffic level? （日本語訳：現在のオーガニックトラフィックレベルは?）
   - Recent changes or migrations? （日本語訳：最近の変更または移行はありますか?）

3. **Scope** （日本語訳：**範囲**）
   - Full site audit or specific pages? （日本語訳：サイト全体の監査ですか、それとも特定のページですか?）
   - Technical + on-page, or one focus area? （日本語訳：テクニカル + ページ内、または 1 つの重点分野?）
   - Access to Search Console / analytics? （日本語訳：Search Console / 分析にアクセスしますか?）

---

## Audit Framework （日本語訳：監査フレームワーク）

### Priority Order （日本語訳：優先順位）
1. **Crawlability & Indexation** (can Google find and index it?) （日本語訳：**クローラビリティとインデックス作成** (Google はそれを見つけてインデックス付けできますか?)）
2. **Technical Foundations** (is the site fast and functional?) （日本語訳：**技術的な基礎** (サイトは高速で機能していますか?)）
3. **On-Page Optimization** (is content optimized?) （日本語訳：**ページ上の最適化** (コンテンツは最適化されていますか?)）
4. **Content Quality** (does it deserve to rank?) （日本語訳：**コンテンツの品質** (ランク付けに値するか?)）
5. **Authority & Links** (does it have credibility?) （日本語訳：**典拠とリンク** (信頼性はありますか?)）

---

## Technical SEO Audit （日本語訳：技術的なSEO監査）

### Crawlability （日本語訳：クローラビリティ）

**Robots.txt** （日本語訳：**ロボット.txt**）
- Check for unintentional blocks （日本語訳：意図しないブロックがないか確認する）
- Verify important pages allowed （日本語訳：重要なページが許可されていることを確認する）
- Check sitemap reference （日本語訳：サイトマップのリファレンスを確認する）

**XML Sitemap** （日本語訳：**XML サイトマップ**）
- Exists and accessible （日本語訳：存在しアクセス可能）
- Submitted to Search Console （日本語訳：Search Consoleに送信されました）
- Contains only canonical, indexable URLs （日本語訳：正規のインデックス可能な URL のみが含まれます）
- Updated regularly （日本語訳：定期的に更新）
- Proper formatting （日本語訳：適切なフォーマット）

**Site Architecture** （日本語訳：**サイトのアーキテクチャ**）
- Important pages within 3 clicks of homepage （日本語訳：ホームページから 3 回クリックするだけで重要なページが表示されます）
- Logical hierarchy （日本語訳：論理階層）
- Internal linking structure （日本語訳：内部リンク構造）
- No orphan pages （日本語訳：孤立したページはありません）

**Crawl Budget Issues** (for large sites) （日本語訳：**クロール予算の問題** (大規模サイトの場合)）
- Parameterized URLs under control （日本語訳：パラメータ化された URL を制御）
- Faceted navigation handled properly （日本語訳：ファセットナビゲーションが適切に処理される）
- Infinite scroll with pagination fallback （日本語訳：ページネーションのフォールバックを備えた無限スクロール）
- Session IDs not in URLs （日本語訳：セッション ID が URL に含まれていない）

### Indexation （日本語訳：索引付け）

**Index Status** （日本語訳：**インデックスステータス**）
- site:domain.com check （日本語訳：サイト:domain.com チェック）
- Search Console coverage report （日本語訳：Search Console カバレッジ レポート）
- Compare indexed vs. expected （日本語訳：インデックス付きと予想されるものを比較する）

**Indexation Issues** （日本語訳：**インデックスの問題**）
- Noindex tags on important pages （日本語訳：重要なページの noindex タグ）
- Canonicals pointing wrong direction （日本語訳：正統派が間違った方向を指している）
- Redirect chains/loops （日本語訳：リダイレクトチェーン/ループ）
- Soft 404s （日本語訳：ソフト 404）
- Duplicate content without canonicals （日本語訳：正規化されていない重複コンテンツ）

**Canonicalization** （日本語訳：**正規化**）
- All pages have canonical tags （日本語訳：すべてのページに正規タグが付いています）
- Self-referencing canonicals on unique pages （日本語訳：独自のページ上の自己参照正典）
- HTTP → HTTPS canonicals （日本語訳：HTTP → HTTPS 正規化）
- www vs. non-www consistency （日本語訳：www と非 www の一貫性）
- Trailing slash consistency （日本語訳：末尾のスラッシュの一貫性）

### Site Speed & Core Web Vitals （日本語訳：サイトの速度と主要なウェブバイタル）

**Core Web Vitals** （日本語訳：**コアウェブバイタル**）
- LCP (Largest Contentful Paint): < 2.5s （日本語訳：LCP (最大内容ペイント): < 2.5 秒）
- INP (Interaction to Next Paint): < 200ms （日本語訳：INP (次のペイントへのインタラクション): < 200ms）
- CLS (Cumulative Layout Shift): < 0.1 （日本語訳：CLS (累積レイアウト シフト): < 0.1）

**Speed Factors** （日本語訳：**スピードファクター**）
- Server response time (TTFB) （日本語訳：サーバー応答時間 (TTFB)）
- Image optimization （日本語訳：画像の最適化）
- JavaScript execution （日本語訳：JavaScriptの実行）
- CSS delivery （日本語訳：CSS配信）
- Caching headers （日本語訳：ヘッダーのキャッシュ）
- CDN usage （日本語訳：CDNの使用法）
- Font loading （日本語訳：フォントの読み込み）

**Tools** （日本語訳：**ツール**）
- PageSpeed Insights （日本語訳：ページスピードに関する洞察）
- WebPageTest （日本語訳：ウェブページテスト）
- Chrome DevTools （日本語訳：Chrome 開発ツール）
- Search Console Core Web Vitals report （日本語訳：Search Console のコア ウェブ バイタル レポート）

### Mobile-Friendliness （日本語訳：モバイルフレンドリーさ）

- Responsive design (not separate m. site) （日本語訳：レスポンシブデザイン（独立したm.サイトではありません））
- Tap target sizes （日本語訳：ターゲットサイズをタップ）
- Viewport configured （日本語訳：ビューポートが設定されました）
- No horizontal scroll （日本語訳：横スクロールなし）
- Same content as desktop （日本語訳：デスクトップと同じ内容）
- Mobile-first indexing readiness （日本語訳：モバイルファーストインデックス作成の準備）

### Security & HTTPS （日本語訳：セキュリティとHTTPS）

- HTTPS across entire site （日本語訳：サイト全体で HTTPS）
- Valid SSL certificate （日本語訳：有効なSSL証明書）
- No mixed content （日本語訳：混合コンテンツなし）
- HTTP → HTTPS redirects （日本語訳：HTTP → HTTPS リダイレクト）
- HSTS header (bonus) （日本語訳：HSTSヘッダー（おまけ））

### URL Structure （日本語訳：URL構造）

- Readable, descriptive URLs （日本語訳：読みやすく説明的な URL）
- Keywords in URLs where natural （日本語訳：URL 内のキーワードが自然）
- Consistent structure （日本語訳：一貫した構造）
- No unnecessary parameters （日本語訳：不要なパラメータはありません）
- Lowercase and hyphen-separated （日本語訳：小文字とハイフンで区切る）

---

## On-Page SEO Audit （日本語訳：オンページSEO監査）

### Title Tags （日本語訳：タイトルタグ）

**Check for:** （日本語訳：**以下を確認してください:**）
- Unique titles for each page （日本語訳：各ページに固有のタイトル）
- Primary keyword near beginning （日本語訳：先頭付近の主キーワード）
- 50-60 characters (visible in SERP) （日本語訳：50～60 文字 (SERP に表示)）
- Compelling and click-worthy （日本語訳：説得力があり、クリックする価値がある）
- Brand name placement (end, usually) （日本語訳：ブランド名の配置（終了、通常））

**Common issues:** （日本語訳：**よくある問題:**）
- Duplicate titles （日本語訳：タイトルの重複）
- Too long (truncated) （日本語訳：長すぎます（切り捨てられています））
- Too short (wasted opportunity) （日本語訳：短すぎる（機会の無駄））
- Keyword stuffing （日本語訳：キーワードの詰め込み）
- Missing entirely （日本語訳：完全に欠けています）

### Meta Descriptions （日本語訳：メタディスクリプション）

**Check for:** （日本語訳：**以下を確認してください:**）
- Unique descriptions per page （日本語訳：ページごとに固有の説明）
- 150-160 characters （日本語訳：150～160文字）
- Includes primary keyword （日本語訳：主なキーワードを含む）
- Clear value proposition （日本語訳：明確な価値提案）
- Call to action （日本語訳：行動喚起）

**Common issues:** （日本語訳：**よくある問題:**）
- Duplicate descriptions （日本語訳：重複した説明）
- Auto-generated garbage （日本語訳：自動生成されるゴミ）
- Too long/short （日本語訳：長すぎる/短すぎる）
- No compelling reason to click （日本語訳：クリックする説得力のある理由はない）

### Heading Structure （日本語訳：見出し構造）

**Check for:** （日本語訳：**以下を確認してください:**）
- One H1 per page （日本語訳：1 ページあたり 1 つの H1）
- H1 contains primary keyword （日本語訳：H1 には主キーワードが含まれます）
- Logical hierarchy (H1 → H2 → H3) （日本語訳：論理階層（H1→H2→H3））
- Headings describe content （日本語訳：見出しは内容を説明します）
- Not just for styling （日本語訳：スタイリングだけでなく）

**Common issues:** （日本語訳：**よくある問題:**）
- Multiple H1s （日本語訳：複数の H1）
- Skip levels (H1 → H3) （日本語訳：スキップレベル (H1 → H3)）
- Headings used for styling only （日本語訳：スタイル設定のみに使用される見出し）
- No H1 on page （日本語訳：ページに H1 がありません）

### Content Optimization （日本語訳：コンテンツの最適化）

**Primary Page Content** （日本語訳：**主要なページのコンテンツ**）
- Keyword in first 100 words （日本語訳：最初の 100 単語のキーワード）
- Related keywords naturally used （日本語訳：自然に使われる関連キーワード）
- Sufficient depth/length for topic （日本語訳：トピックに十分な深さ/長さ）
- Answers search intent （日本語訳：回答の検索意図）
- Better than competitors （日本語訳：競合他社よりも優れている）

**Thin Content Issues** （日本語訳：**内容の薄い問題**）
- Pages with little unique content （日本語訳：独自のコンテンツがほとんどないページ）
- Tag/category pages with no value （日本語訳：値のないタグ/カテゴリ ページ）
- Doorway pages （日本語訳：玄関ページ）
- Duplicate or near-duplicate content （日本語訳：重複または重複に近いコンテンツ）

### Image Optimization （日本語訳：画像の最適化）

**Check for:** （日本語訳：**以下を確認してください:**）
- Descriptive file names （日本語訳：わかりやすいファイル名）
- Alt text on all images （日本語訳：すべての画像の代替テキスト）
- Alt text describes image （日本語訳：画像を説明する代替テキスト）
- Compressed file sizes （日本語訳：圧縮ファイルサイズ）
- Modern formats (WebP) （日本語訳：最新のフォーマット (WebP)）
- Lazy loading implemented （日本語訳：遅延読み込みの実装）
- Responsive images （日本語訳：レスポンシブ画像）

### Internal Linking （日本語訳：内部リンク）

**Check for:** （日本語訳：**以下を確認してください:**）
- Important pages well-linked （日本語訳：重要なページはしっかりとリンクされている）
- Descriptive anchor text （日本語訳：説明的なアンカーテキスト）
- Logical link relationships （日本語訳：論理リンク関係）
- No broken internal links （日本語訳：壊れた内部リンクはありません）
- Reasonable link count per page （日本語訳：ページあたりの適切なリンク数）

**Common issues:** （日本語訳：**よくある問題:**）
- Orphan pages (no internal links) （日本語訳：孤立したページ (内部リンクなし)）
- Over-optimized anchor text （日本語訳：過剰に最適化されたアンカーテキスト）
- Important pages buried （日本語訳：重要なページが埋もれてしまう）
- Excessive footer/sidebar links （日本語訳：過剰なフッター/サイドバーリンク）

### Keyword Targeting （日本語訳：キーワードターゲティング）

**Per Page** （日本語訳：**ページごと**）
- Clear primary keyword target （日本語訳：主なキーワード ターゲットをクリアする）
- Title, H1, URL aligned （日本語訳：タイトル、H1、URL を揃える）
- Content satisfies search intent （日本語訳：コンテンツが検索意図を満たしている）
- Not competing with other pages (cannibalization) （日本語訳：他のページと競合しない（カニバリゼーション））

**Site-Wide** （日本語訳：**サイト全体**）
- Keyword mapping document （日本語訳：キーワードマッピングドキュメント）
- No major gaps in coverage （日本語訳：カバー範囲に大きなギャップはない）
- No keyword cannibalization （日本語訳：キーワードのカニバリゼーションはありません）
- Logical topical clusters （日本語訳：論理トピッククラスター）

---

## Content Quality Assessment （日本語訳：コンテンツの品質評価）

### E-E-A-T Signals （日本語訳：E-E-A-T 信号）

**Experience** （日本語訳：**経験**）
- First-hand experience demonstrated （日本語訳：実際に実証された経験）
- Original insights/data （日本語訳：オリジナルの洞察/データ）
- Real examples and case studies （日本語訳：実際の例とケーススタディ）

**Expertise** （日本語訳：**専門知識**）
- Author credentials visible （日本語訳：著者の資格情報が表示される）
- Accurate, detailed information （日本語訳：正確で詳細な情報）
- Properly sourced claims （日本語訳：適切な情報源に基づいた主張）

**Authoritativeness** （日本語訳：**権威性**）
- Recognized in the space （日本語訳：空間で認識される）
- Cited by others （日本語訳：他の人が引用した）
- Industry credentials （日本語訳：業界の資格情報）

**Trustworthiness** （日本語訳：**信頼性**）
- Accurate information （日本語訳：正確な情報）
- Transparent about business （日本語訳：ビジネスについての透明性）
- Contact information available （日本語訳：連絡先情報が利用可能）
- Privacy policy, terms （日本語訳：プライバシーポリシー、規約）
- Secure site (HTTPS) （日本語訳：安全なサイト (HTTPS)）

### Content Depth （日本語訳：コンテンツの深さ）

- Comprehensive coverage of topic （日本語訳：トピックを包括的にカバー）
- Answers follow-up questions （日本語訳：フォローアップの質問に回答します）
- Better than top-ranking competitors （日本語訳：上位の競合他社よりも優れている）
- Updated and current （日本語訳：更新された最新の）

### User Engagement Signals （日本語訳：ユーザーエンゲージメントシグナル）

- Time on page （日本語訳：ページ滞在時間）
- Bounce rate in context （日本語訳：コンテキスト内の直帰率）
- Pages per session （日本語訳：セッションあたりのページ数）
- Return visits （日本語訳：再訪問）

---

## Common Issues by Site Type （日本語訳：サイトの種類別の一般的な問題）

### SaaS/Product Sites （日本語訳：SaaS/製品サイト）
- Product pages lack content depth （日本語訳：商品ページにはコンテンツの深みがありません）
- Blog not integrated with product pages （日本語訳：ブログが製品ページと統合されていない）
- Missing comparison/alternative pages （日本語訳：比較/代替ページがありません）
- Feature pages thin on content （日本語訳：内容が薄い特集ページ）
- No glossary/educational content （日本語訳：用語集や教育コンテンツはありません）

### E-commerce （日本語訳：電子商取引）
- Thin category pages （日本語訳：薄いカテゴリーページ）
- Duplicate product descriptions （日本語訳：重複した商品説明）
- Missing product schema （日本語訳：製品スキーマがありません）
- Faceted navigation creating duplicates （日本語訳：ファセットナビゲーションによる重複の作成）
- Out-of-stock pages mishandled （日本語訳：在庫切れのページが誤って処理された）

### Content/Blog Sites （日本語訳：コンテンツ/ブログ サイト）
- Outdated content not refreshed （日本語訳：古いコンテンツが更新されない）
- Keyword cannibalization （日本語訳：キーワードのカニバリゼーション）
- No topical clustering （日本語訳：トピッククラスタリングなし）
- Poor internal linking （日本語訳：内部リンクが不十分）
- Missing author pages （日本語訳：著者のページがありません）

### Local Business （日本語訳：ローカルビジネス）
- Inconsistent NAP （日本語訳：一貫性のない NAP）
- Missing local schema （日本語訳：ローカルスキーマがありません）
- No Google Business Profile optimization （日本語訳：Google ビジネス プロフィールの最適化なし）
- Missing location pages （日本語訳：場所のページがありません）
- No local content （日本語訳：ローカルコンテンツはありません）

---

## Output Format （日本語訳：出力フォーマット）

### Audit Report Structure （日本語訳：監査報告書の構造）

**Executive Summary** （日本語訳：**エグゼクティブサマリー**）
- Overall health assessment （日本語訳：全体的な健康評価）
- Top 3-5 priority issues （日本語訳：上位 3 ～ 5 の優先課題）
- Quick wins identified （日本語訳：迅速な勝利の特定）

**Technical SEO Findings** （日本語訳：**技術的な SEO の調査結果**）
For each issue: （日本語訳：各問題について:）
- **Issue**: What's wrong （日本語訳：**問題**: 何が問題ですか）
- **Impact**: SEO impact (High/Medium/Low) （日本語訳：**影響**: SEO への影響 (高/中/低)）
- **Evidence**: How you found it （日本語訳：**証拠**: どのようにして見つけたのか）
- **Fix**: Specific recommendation （日本語訳：**修正**: 具体的な推奨事項）
- **Priority**: 1-5 or High/Medium/Low （日本語訳：**優先度**: 1 ～ 5 または高/中/低）

**On-Page SEO Findings** （日本語訳：**オンページ SEO の調査結果**）
Same format as above （日本語訳：上記と同じ形式）

**Content Findings** （日本語訳：**コンテンツの調査結果**）
Same format as above （日本語訳：上記と同じ形式）

**Prioritized Action Plan** （日本語訳：**優先行動計画**）
1. Critical fixes (blocking indexation/ranking) （日本語訳：重要な修正 (インデックス/ランキングのブロック)）
2. High-impact improvements （日本語訳：大きな影響を与える改善）
3. Quick wins (easy, immediate benefit) （日本語訳：即効性（簡単ですぐに利益が得られる））
4. Long-term recommendations （日本語訳：長期的な推奨事項）

---

## References （日本語訳：参考文献）

- [AI Writing Detection](references/ai-writing-detection.md): Common AI writing patterns to avoid (em dashes, overused phrases, filler words) （日本語訳：[AI ライティング検出](references/ai-writing-detection.md): 避けるべき一般的な AI ライティング パターン (全角ダッシュ、使いすぎたフレーズ、つなぎ言葉)）
- [AEO & GEO Patterns](references/aeo-geo-patterns.md): Content patterns optimized for answer engines and AI citation （日本語訳：[AEO および GEO パターン](references/aeo-geo-patterns.md): 回答エンジンと AI 引用用に最適化されたコンテンツ パターン）

---

## Tools Referenced （日本語訳：参照したツール）

**Free Tools** （日本語訳：**無料ツール**）
- Google Search Console (essential) （日本語訳：Google Search Console（必須））
- Google PageSpeed Insights （日本語訳：Google PageSpeed Insights）
- Bing Webmaster Tools （日本語訳：Bing ウェブマスター ツール）
- Rich Results Test （日本語訳：リッチリザルトテスト）
- Mobile-Friendly Test （日本語訳：モバイルフレンドリーテスト）
- Schema Validator （日本語訳：スキーマバリデーター）

**Paid Tools** (if available) （日本語訳：**有料ツール** (利用可能な場合)）
- Screaming Frog （日本語訳：叫ぶカエル）
- Ahrefs / Semrush （日本語訳：アーレフス / セムラッシュ）
- Sitebulb （日本語訳：サイトバルブ）
- ContentKing （日本語訳：コンテンツキング）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What pages/keywords matter most? （日本語訳：どのページ/キーワードが最も重要ですか?）
2. Do you have Search Console access? （日本語訳：Search Console にアクセスできますか?）
3. Any recent changes or migrations? （日本語訳：最近の変更や移行はありますか?）
4. Who are your top organic competitors? （日本語訳：オーガニックの最大の競合相手は誰ですか?）
5. What's your current organic traffic baseline? （日本語訳：現在のオーガニックトラフィックのベースラインはどれくらいですか?）

---

## Related Skills （日本語訳：関連スキル）

- **programmatic-seo**: For building SEO pages at scale （日本語訳：**programmatic-seo**: 大規模な SEO ページの構築用）
- **schema-markup**: For implementing structured data （日本語訳：**schema-markup**: 構造化データの実装用）
- **page-cro**: For optimizing pages for conversion (not just ranking) （日本語訳：**page-cro**: コンバージョンに向けてページを最適化します (ランキングだけでなく)）
- **analytics-tracking**: For measuring SEO performance （日本語訳：**analytics-tracking**: SEO パフォーマンスの測定用）
