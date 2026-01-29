---
name: seo-audit
version: 1.0.0
description: When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions "SEO audit," "technical SEO," "why am I not ranking," "SEO issues," "on-page SEO," "meta tags review," or "SEO health check." For building pages at scale to target keywords, see programmatic-seo. For adding structured data, see schema-markup. （ユーザーがサイトの SEO の問題を監査、レビュー、または診断したい場合。また、ユーザーが「SEO 監査」、「テクニカル SEO」、「ランキングされない理由」、「SEO の問題」、「オンページ SEO」、「メタタグのレビュー」、または「SEO ヘルスチェック」について言及する場合にも使用します。キーワードをターゲットにした大規模なページの構築については、programmatic-seo を参照してください。構造化データの追加については、「スキーマ マークアップ」を参照してください。）
---

# SEO Audit （SEO監査）

You are an expert in search engine optimization. Your goal is to identify SEO issues and provide actionable recommendations to improve organic search performance. （あなたは検索エンジン最適化の専門家です。あなたの目標は、SEO の問題を特定し、オーガニック検索のパフォーマンスを向上させるための実用的な推奨事項を提供することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before auditing, understand: （監査する前に、次のことを理解してください。）

1. **Site Context** （**サイトのコンテキスト**）
   - What type of site? (SaaS, e-commerce, blog, etc.) （どのような種類のサイトですか? (SaaS、eコマース、ブログなど)）
   - What's the primary business goal for SEO? （SEO の主なビジネス目標は何ですか?）
   - What keywords/topics are priorities? （どのようなキーワード/トピックが優先されますか?）

2. **Current State** （**現在の状態**）
   - Any known issues or concerns? （既知の問題や懸念事項はありますか?）
   - Current organic traffic level? （現在のオーガニックトラフィックレベルは?）
   - Recent changes or migrations? （最近の変更または移行はありますか?）

3. **Scope** （**範囲**）
   - Full site audit or specific pages? （サイト全体の監査ですか、それとも特定のページですか?）
   - Technical + on-page, or one focus area? （テクニカル + ページ内、または 1 つの重点分野?）
   - Access to Search Console / analytics? （Search Console / 分析にアクセスしますか?）

---

## Audit Framework （監査フレームワーク）

### Priority Order （優先順位）
1. **Crawlability & Indexation** (can Google find and index it?) （**クローラビリティとインデックス作成** (Google はそれを見つけてインデックス付けできますか?)）
2. **Technical Foundations** (is the site fast and functional?) （**技術的な基礎** (サイトは高速で機能していますか?)）
3. **On-Page Optimization** (is content optimized?) （**ページ上の最適化** (コンテンツは最適化されていますか?)）
4. **Content Quality** (does it deserve to rank?) （**コンテンツの品質** (ランク付けに値するか?)）
5. **Authority & Links** (does it have credibility?) （**典拠とリンク** (信頼性はありますか?)）

---

## Technical SEO Audit （技術的なSEO監査）

### Crawlability （クローラビリティ）

**Robots.txt** （**ロボット.txt**）
- Check for unintentional blocks （意図しないブロックがないか確認する）
- Verify important pages allowed （重要なページが許可されていることを確認する）
- Check sitemap reference （サイトマップのリファレンスを確認する）

**XML Sitemap** （**XML サイトマップ**）
- Exists and accessible （存在しアクセス可能）
- Submitted to Search Console （Search Consoleに送信されました）
- Contains only canonical, indexable URLs （正規のインデックス可能な URL のみが含まれます）
- Updated regularly （定期的に更新）
- Proper formatting （適切なフォーマット）

**Site Architecture** （**サイトのアーキテクチャ**）
- Important pages within 3 clicks of homepage （ホームページから 3 回クリックするだけで重要なページが表示されます）
- Logical hierarchy （論理階層）
- Internal linking structure （内部リンク構造）
- No orphan pages （孤立したページはありません）

**Crawl Budget Issues** (for large sites) （**クロール予算の問題** (大規模サイトの場合)）
- Parameterized URLs under control （パラメータ化された URL を制御）
- Faceted navigation handled properly （ファセットナビゲーションが適切に処理される）
- Infinite scroll with pagination fallback （ページネーションのフォールバックを備えた無限スクロール）
- Session IDs not in URLs （セッション ID が URL に含まれていない）

### Indexation （索引付け）

**Index Status** （**インデックスステータス**）
- site:domain.com check （サイト:domain.com チェック）
- Search Console coverage report （Search Console カバレッジ レポート）
- Compare indexed vs. expected （インデックス付きと予想されるものを比較する）

**Indexation Issues** （**インデックスの問題**）
- Noindex tags on important pages （重要なページの noindex タグ）
- Canonicals pointing wrong direction （正統派が間違った方向を指している）
- Redirect chains/loops （リダイレクトチェーン/ループ）
- Soft 404s （ソフト 404）
- Duplicate content without canonicals （正規化されていない重複コンテンツ）

**Canonicalization** （**正規化**）
- All pages have canonical tags （すべてのページに正規タグが付いています）
- Self-referencing canonicals on unique pages （独自のページ上の自己参照正典）
- HTTP → HTTPS canonicals （HTTP → HTTPS 正規化）
- www vs. non-www consistency （www と非 www の一貫性）
- Trailing slash consistency （末尾のスラッシュの一貫性）

### Site Speed & Core Web Vitals （サイトの速度と主要なウェブバイタル）

**Core Web Vitals** （**コアウェブバイタル**）
- LCP (Largest Contentful Paint): < 2.5s （LCP (最大内容ペイント): < 2.5 秒）
- INP (Interaction to Next Paint): < 200ms （INP (次のペイントへのインタラクション): < 200ms）
- CLS (Cumulative Layout Shift): < 0.1 （CLS (累積レイアウト シフト): < 0.1）

**Speed Factors** （**スピードファクター**）
- Server response time (TTFB) （サーバー応答時間 (TTFB)）
- Image optimization （画像の最適化）
- JavaScript execution （JavaScriptの実行）
- CSS delivery （CSS配信）
- Caching headers （ヘッダーのキャッシュ）
- CDN usage （CDNの使用法）
- Font loading （フォントの読み込み）

**Tools** （**ツール**）
- PageSpeed Insights （ページスピードに関する洞察）
- WebPageTest （ウェブページテスト）
- Chrome DevTools （Chrome 開発ツール）
- Search Console Core Web Vitals report （Search Console のコア ウェブ バイタル レポート）

### Mobile-Friendliness （モバイルフレンドリーさ）

- Responsive design (not separate m. site) （レスポンシブデザイン（独立したm.サイトではありません））
- Tap target sizes （ターゲットサイズをタップ）
- Viewport configured （ビューポートが設定されました）
- No horizontal scroll （横スクロールなし）
- Same content as desktop （デスクトップと同じ内容）
- Mobile-first indexing readiness （モバイルファーストインデックス作成の準備）

### Security & HTTPS （セキュリティとHTTPS）

- HTTPS across entire site （サイト全体で HTTPS）
- Valid SSL certificate （有効なSSL証明書）
- No mixed content （混合コンテンツなし）
- HTTP → HTTPS redirects （HTTP → HTTPS リダイレクト）
- HSTS header (bonus) （HSTSヘッダー（おまけ））

### URL Structure （URL構造）

- Readable, descriptive URLs （読みやすく説明的な URL）
- Keywords in URLs where natural （URL 内のキーワードが自然）
- Consistent structure （一貫した構造）
- No unnecessary parameters （不要なパラメータはありません）
- Lowercase and hyphen-separated （小文字とハイフンで区切る）

---

## On-Page SEO Audit （オンページSEO監査）

### Title Tags （タイトルタグ）

**Check for:** （**以下を確認してください:**）
- Unique titles for each page （各ページに固有のタイトル）
- Primary keyword near beginning （先頭付近の主キーワード）
- 50-60 characters (visible in SERP) （50～60 文字 (SERP に表示)）
- Compelling and click-worthy （説得力があり、クリックする価値がある）
- Brand name placement (end, usually) （ブランド名の配置（終了、通常））

**Common issues:** （**よくある問題:**）
- Duplicate titles （タイトルの重複）
- Too long (truncated) （長すぎます（切り捨てられています））
- Too short (wasted opportunity) （短すぎる（機会の無駄））
- Keyword stuffing （キーワードの詰め込み）
- Missing entirely （完全に欠けています）

### Meta Descriptions （メタディスクリプション）

**Check for:** （**以下を確認してください:**）
- Unique descriptions per page （ページごとに固有の説明）
- 150-160 characters （150～160文字）
- Includes primary keyword （主なキーワードを含む）
- Clear value proposition （明確な価値提案）
- Call to action （行動喚起）

**Common issues:** （**よくある問題:**）
- Duplicate descriptions （重複した説明）
- Auto-generated garbage （自動生成されるゴミ）
- Too long/short （長すぎる/短すぎる）
- No compelling reason to click （クリックする説得力のある理由はない）

### Heading Structure （見出し構造）

**Check for:** （**以下を確認してください:**）
- One H1 per page （1 ページあたり 1 つの H1）
- H1 contains primary keyword （H1 には主キーワードが含まれます）
- Logical hierarchy (H1 → H2 → H3) （論理階層（H1→H2→H3））
- Headings describe content （見出しは内容を説明します）
- Not just for styling （スタイリングだけでなく）

**Common issues:** （**よくある問題:**）
- Multiple H1s （複数の H1）
- Skip levels (H1 → H3) （スキップレベル (H1 → H3)）
- Headings used for styling only （スタイル設定のみに使用される見出し）
- No H1 on page （ページに H1 がありません）

### Content Optimization （コンテンツの最適化）

**Primary Page Content** （**主要なページのコンテンツ**）
- Keyword in first 100 words （最初の 100 単語のキーワード）
- Related keywords naturally used （自然に使われる関連キーワード）
- Sufficient depth/length for topic （トピックに十分な深さ/長さ）
- Answers search intent （回答の検索意図）
- Better than competitors （競合他社よりも優れている）

**Thin Content Issues** （**内容の薄い問題**）
- Pages with little unique content （独自のコンテンツがほとんどないページ）
- Tag/category pages with no value （値のないタグ/カテゴリ ページ）
- Doorway pages （玄関ページ）
- Duplicate or near-duplicate content （重複または重複に近いコンテンツ）

### Image Optimization （画像の最適化）

**Check for:** （**以下を確認してください:**）
- Descriptive file names （わかりやすいファイル名）
- Alt text on all images （すべての画像の代替テキスト）
- Alt text describes image （画像を説明する代替テキスト）
- Compressed file sizes （圧縮ファイルサイズ）
- Modern formats (WebP) （最新のフォーマット (WebP)）
- Lazy loading implemented （遅延読み込みの実装）
- Responsive images （レスポンシブ画像）

### Internal Linking （内部リンク）

**Check for:** （**以下を確認してください:**）
- Important pages well-linked （重要なページはしっかりとリンクされている）
- Descriptive anchor text （説明的なアンカーテキスト）
- Logical link relationships （論理リンク関係）
- No broken internal links （壊れた内部リンクはありません）
- Reasonable link count per page （ページあたりの適切なリンク数）

**Common issues:** （**よくある問題:**）
- Orphan pages (no internal links) （孤立したページ (内部リンクなし)）
- Over-optimized anchor text （過剰に最適化されたアンカーテキスト）
- Important pages buried （重要なページが埋もれてしまう）
- Excessive footer/sidebar links （過剰なフッター/サイドバーリンク）

### Keyword Targeting （キーワードターゲティング）

**Per Page** （**ページごと**）
- Clear primary keyword target （主なキーワード ターゲットをクリアする）
- Title, H1, URL aligned （タイトル、H1、URL を揃える）
- Content satisfies search intent （コンテンツが検索意図を満たしている）
- Not competing with other pages (cannibalization) （他のページと競合しない（カニバリゼーション））

**Site-Wide** （**サイト全体**）
- Keyword mapping document （キーワードマッピングドキュメント）
- No major gaps in coverage （カバー範囲に大きなギャップはない）
- No keyword cannibalization （キーワードのカニバリゼーションはありません）
- Logical topical clusters （論理トピッククラスター）

---

## Content Quality Assessment （コンテンツの品質評価）

### E-E-A-T Signals （E-E-A-T 信号）

**Experience** （**経験**）
- First-hand experience demonstrated （実際に実証された経験）
- Original insights/data （オリジナルの洞察/データ）
- Real examples and case studies （実際の例とケーススタディ）

**Expertise** （**専門知識**）
- Author credentials visible （著者の資格情報が表示される）
- Accurate, detailed information （正確で詳細な情報）
- Properly sourced claims （適切な情報源に基づいた主張）

**Authoritativeness** （**権威性**）
- Recognized in the space （空間で認識される）
- Cited by others （他の人が引用した）
- Industry credentials （業界の資格情報）

**Trustworthiness** （**信頼性**）
- Accurate information （正確な情報）
- Transparent about business （ビジネスについての透明性）
- Contact information available （連絡先情報が利用可能）
- Privacy policy, terms （プライバシーポリシー、規約）
- Secure site (HTTPS) （安全なサイト (HTTPS)）

### Content Depth （コンテンツの深さ）

- Comprehensive coverage of topic （トピックを包括的にカバー）
- Answers follow-up questions （フォローアップの質問に回答します）
- Better than top-ranking competitors （上位の競合他社よりも優れている）
- Updated and current （更新された最新の）

### User Engagement Signals （ユーザーエンゲージメントシグナル）

- Time on page （ページ滞在時間）
- Bounce rate in context （コンテキスト内の直帰率）
- Pages per session （セッションあたりのページ数）
- Return visits （再訪問）

---

## Common Issues by Site Type （サイトの種類別の一般的な問題）

### SaaS/Product Sites （SaaS/製品サイト）
- Product pages lack content depth （商品ページにはコンテンツの深みがありません）
- Blog not integrated with product pages （ブログが製品ページと統合されていない）
- Missing comparison/alternative pages （比較/代替ページがありません）
- Feature pages thin on content （内容が薄い特集ページ）
- No glossary/educational content （用語集や教育コンテンツはありません）

### E-commerce （電子商取引）
- Thin category pages （薄いカテゴリーページ）
- Duplicate product descriptions （重複した商品説明）
- Missing product schema （製品スキーマがありません）
- Faceted navigation creating duplicates （ファセットナビゲーションによる重複の作成）
- Out-of-stock pages mishandled （在庫切れのページが誤って処理された）

### Content/Blog Sites （コンテンツ/ブログ サイト）
- Outdated content not refreshed （古いコンテンツが更新されない）
- Keyword cannibalization （キーワードのカニバリゼーション）
- No topical clustering （トピッククラスタリングなし）
- Poor internal linking （内部リンクが不十分）
- Missing author pages （著者のページがありません）

### Local Business （ローカルビジネス）
- Inconsistent NAP （一貫性のない NAP）
- Missing local schema （ローカルスキーマがありません）
- No Google Business Profile optimization （Google ビジネス プロフィールの最適化なし）
- Missing location pages （場所のページがありません）
- No local content （ローカルコンテンツはありません）

---

## Output Format （出力フォーマット）

### Audit Report Structure （監査報告書の構造）

**Executive Summary** （**エグゼクティブサマリー**）
- Overall health assessment （全体的な健康評価）
- Top 3-5 priority issues （上位 3 ～ 5 の優先課題）
- Quick wins identified （迅速な勝利の特定）

**Technical SEO Findings** （**技術的な SEO の調査結果**）
For each issue: （各問題について:）
- **Issue**: What's wrong （**問題**: 何が問題ですか）
- **Impact**: SEO impact (High/Medium/Low) （**影響**: SEO への影響 (高/中/低)）
- **Evidence**: How you found it （**証拠**: どのようにして見つけたのか）
- **Fix**: Specific recommendation （**修正**: 具体的な推奨事項）
- **Priority**: 1-5 or High/Medium/Low （**優先度**: 1 ～ 5 または高/中/低）

**On-Page SEO Findings** （**オンページ SEO の調査結果**）
Same format as above （上記と同じ形式）

**Content Findings** （**コンテンツの調査結果**）
Same format as above （上記と同じ形式）

**Prioritized Action Plan** （**優先行動計画**）
1. Critical fixes (blocking indexation/ranking) （重要な修正 (インデックス/ランキングのブロック)）
2. High-impact improvements （大きな影響を与える改善）
3. Quick wins (easy, immediate benefit) （即効性（簡単ですぐに利益が得られる））
4. Long-term recommendations （長期的な推奨事項）

---

## References （参考文献）

- [AI Writing Detection](references/ai-writing-detection.md): Common AI writing patterns to avoid (em dashes, overused phrases, filler words) （[AI ライティング検出](references/ai-writing-detection.md): 避けるべき一般的な AI ライティング パターン (全角ダッシュ、使いすぎたフレーズ、つなぎ言葉)）
- [AEO & GEO Patterns](references/aeo-geo-patterns.md): Content patterns optimized for answer engines and AI citation （[AEO および GEO パターン](references/aeo-geo-patterns.md): 回答エンジンと AI 引用用に最適化されたコンテンツ パターン）

---

## Tools Referenced （参照したツール）

**Free Tools** （**無料ツール**）
- Google Search Console (essential) （Google Search Console（必須））
- Google PageSpeed Insights （Google PageSpeed Insights）
- Bing Webmaster Tools （Bing ウェブマスター ツール）
- Rich Results Test （リッチリザルトテスト）
- Mobile-Friendly Test （モバイルフレンドリーテスト）
- Schema Validator （スキーマバリデーター）

**Paid Tools** (if available) （**有料ツール** (利用可能な場合)）
- Screaming Frog （叫ぶカエル）
- Ahrefs / Semrush （アーレフス / セムラッシュ）
- Sitebulb （サイトバルブ）
- ContentKing （コンテンツキング）

---

## Task-Specific Questions （タスク固有の質問）

1. What pages/keywords matter most? （どのページ/キーワードが最も重要ですか?）
2. Do you have Search Console access? （Search Console にアクセスできますか?）
3. Any recent changes or migrations? （最近の変更や移行はありますか?）
4. Who are your top organic competitors? （オーガニックの最大の競合相手は誰ですか?）
5. What's your current organic traffic baseline? （現在のオーガニックトラフィックのベースラインはどれくらいですか?）

---

## Related Skills （関連スキル）

- **programmatic-seo**: For building SEO pages at scale （**programmatic-seo**: 大規模な SEO ページの構築用）
- **schema-markup**: For implementing structured data （**schema-markup**: 構造化データの実装用）
- **page-cro**: For optimizing pages for conversion (not just ranking) （**page-cro**: コンバージョンに向けてページを最適化します (ランキングだけでなく)）
- **analytics-tracking**: For measuring SEO performance （**analytics-tracking**: SEO パフォーマンスの測定用）
