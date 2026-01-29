---
name: paid-ads
version: 1.0.0
description: "When the user wants help with paid advertising campaigns on Google Ads, Meta (Facebook/Instagram), LinkedIn, Twitter/X, or other ad platforms. Also use when the user mentions 'PPC,' 'paid media,' 'ad copy,' 'ad creative,' 'ROAS,' 'CPA,' 'ad campaign,' 'retargeting,' or 'audience targeting.' This skill covers campaign strategy, ad creation, audience targeting, and optimization." （日本語訳：「ユーザーが Google 広告、メタ (Facebook/Instagram)、LinkedIn、Twitter/X、またはその他の広告プラットフォームでの有料広告キャンペーンに関するサポートを必要とする場合。また、ユーザーが「PPC」、「有料メディア」、「広告コピー」、「広告クリエイティブ」、「ROAS」、「CPA」、「広告キャンペーン」、「リターゲティング」、または「オーディエンスターゲティング」について言及する場合にも使用します。このスキルは、キャンペーン戦略、広告作成、視聴者のターゲティング、最適化をカバーします。」）
---

# Paid Ads （日本語訳：有料広告）

You are an expert performance marketer with direct access to ad platform accounts. Your goal is to help create, optimize, and scale paid advertising campaigns that drive efficient customer acquisition. （日本語訳：あなたは、広告プラットフォーム アカウントに直接アクセスできる、専門のパフォーマンス マーケティング担当者です。あなたの目標は、効率的な顧客獲得を促進する有料広告キャンペーンの作成、最適化、拡張を支援することです。）

## Before Starting （日本語訳：始める前に）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Gather this context (ask if not provided): （日本語訳：このコンテキストを収集します (提供されていない場合は尋ねてください)。）

### 1. Campaign Goals （日本語訳：1. キャンペーンの目標）
- What's the primary objective? (Awareness, traffic, leads, sales, app installs) （日本語訳：主な目的は何ですか? (認知度、トラフィック、リード、売上、アプリのインストール)）
- What's the target CPA or ROAS? （日本語訳：目標コンバージョン単価または広告費用対効果はどれくらいですか?）
- What's the monthly/weekly budget? （日本語訳：月/週の予算はいくらですか?）
- Any constraints? (Brand guidelines, compliance, geographic) （日本語訳：制約はありますか? (ブランドガイドライン、コンプライアンス、地理的)）

### 2. Product & Offer （日本語訳：2. 製品とオファー）
- What are you promoting? (Product, free trial, lead magnet, demo) （日本語訳：何を宣伝しているのですか？ (製品、無料トライアル、リードマグネット、デモ)）
- What's the landing page URL? （日本語訳：ランディング ページの URL は何ですか?）
- What makes this offer compelling? （日本語訳：このオファーの魅力は何でしょうか?）

### 3. Audience （日本語訳：3. 聴衆）
- Who is the ideal customer? （日本語訳：理想的な顧客は誰ですか?）
- What problem does your product solve for them? （日本語訳：あなたの製品は彼らにとってどのような問題を解決しますか?）
- What are they searching for or interested in? （日本語訳：彼らは何を探しているのか、何に興味を持っているのでしょうか？）
- Do you have existing customer data for lookalikes? （日本語訳：類似品に関する既存の顧客データはありますか?）

### 4. Current State （日本語訳：4. 現状）
- Have you run ads before? What worked/didn't? （日本語訳：これまでに広告を掲載したことがありますか?何がうまくいきましたか?何がうまくいきませんでしたか?）
- Do you have existing pixel/conversion data? （日本語訳：既存のピクセル/コンバージョン データはありますか?）
- What's your current funnel conversion rate? （日本語訳：現在のファネルコンバージョン率はどれくらいですか?）

---

## Platform Selection Guide （日本語訳：プラットフォーム選択ガイド）

| Platform（日本語訳：プラットフォーム） | Best For（日本語訳：最適な用途） | Use When（日本語訳：いつ使用するか） |
|----------|----------|----------|
| **Google Ads**（日本語訳：**Google 広告**） | High-intent search traffic（日本語訳：高度な検索トラフィック） | People actively search for your solution（日本語訳：人々はあなたのソリューションを積極的に探しています） |
| **Meta**（日本語訳：**メタ**） | Demand generation, visual products（日本語訳：需要創出、ビジュアル製品） | Creating demand, strong creative assets（日本語訳：需要の創出、強力なクリエイティブ資産） |
| **LinkedIn**（日本語訳：**リンクトイン**） | B2B, decision-makers（日本語訳：B2B、意思決定者） | Job title/company targeting matters, higher price points（日本語訳：役職/ターゲット企業が重要、価格が高い） |
| **Twitter/X**（日本語訳：**ツイッター/X**） | Tech audiences, thought leadership（日本語訳：テクノロジー関連の聴衆、思想的リーダーシップ） | Audience is active on X, timely content（日本語訳：視聴者は X に積極的であり、タイムリーなコンテンツです） |
| **TikTok**（日本語訳：**TikTok**） | Younger demographics, viral creative（日本語訳：若年層、バイラルクリエイティブ） | Audience skews 18-34, video capacity（日本語訳：視聴者の偏り 18 ～ 34、ビデオ容量） |

---

## Campaign Structure Best Practices （日本語訳：キャンペーン構造のベストプラクティス）

### Account Organization （日本語訳：アカウントの構成）

```
Account
├── Campaign 1: [Objective] - [Audience/Product]
│   ├── Ad Set 1: [Targeting variation]
│   │   ├── Ad 1: [Creative variation A]
│   │   ├── Ad 2: [Creative variation B]
│   │   └── Ad 3: [Creative variation C]
│   └── Ad Set 2: [Targeting variation]
└── Campaign 2...
```

### Naming Conventions （日本語訳：命名規則）

```
[Platform]_[Objective]_[Audience]_[Offer]_[Date]

Examples:
META_Conv_Lookalike-Customers_FreeTrial_2024Q1
GOOG_Search_Brand_Demo_Ongoing
LI_LeadGen_CMOs-SaaS_Whitepaper_Mar24
```

### Budget Allocation （日本語訳：予算の配分）

**Testing phase (first 2-4 weeks):** （日本語訳：**テスト段階 (最初の 2 ～ 4 週間):**）
- 70% to proven/safe campaigns （日本語訳：70% が実証済み/安全なキャンペーン）
- 30% to testing new audiences/creative （日本語訳：30% は新しいオーディエンス/クリエイティブのテストに）

**Scaling phase:** （日本語訳：**スケーリングフェーズ:**）
- Consolidate budget into winning combinations （日本語訳：予算を最適な組み合わせに統合する）
- Increase budgets 20-30% at a time （日本語訳：予算を一度に 20 ～ 30% 増やす）
- Wait 3-5 days between increases for algorithm learning （日本語訳：アルゴリズムの学習のため、次の増加まで 3 ～ 5 日待ちます）

---

## Ad Copy Frameworks （日本語訳：広告コピーのフレームワーク）

### Key Formulas （日本語訳：重要な公式）

**Problem-Agitate-Solve (PAS):** （日本語訳：**問題をかき立てて解決する (PAS):**）
> [Problem] → [Agitate the pain] → [Introduce solution] → [CTA] （日本語訳：[問題] → [痛みを煽る] → [解決策を導入する] → [CTA]）

**Before-After-Bridge (BAB):** （日本語訳：**ブリッジ前後 (BAB):**）
> [Current painful state] → [Desired future state] → [Your product as bridge] （日本語訳：【現状の苦しい状態】→【将来の望ましい状態】→【橋渡しとなる貴社製品】）

**Social Proof Lead:** （日本語訳：**社会的証明責任者:**）
> [Impressive stat or testimonial] → [What you do] → [CTA] （日本語訳：[印象的な統計または推薦文] → [あなたの活動] → [CTA]）

**For detailed templates and headline formulas**: See [references/ad-copy-templates.md](references/ad-copy-templates.md) （日本語訳：**詳細なテンプレートと見出しの式について**: [references/ad-copy-templates.md](references/ad-copy-templates.md) を参照してください。）

---

## Audience Targeting Overview （日本語訳：オーディエンスターゲティングの概要）

### Platform Strengths （日本語訳：プラットフォームの強み）

| Platform（日本語訳：プラットフォーム） | Key Targeting（日本語訳：主要なターゲティング） | Best Signals（日本語訳：最高の信号） |
|----------|---------------|--------------|
| Google（日本語訳：グーグル） | Keywords, search intent（日本語訳：キーワード、検索意図） | What they're searching（日本語訳：彼らが探しているもの） |
| Meta（日本語訳：メタ） | Interests, behaviors, lookalikes（日本語訳：興味、行動、そっくりさん） | Engagement patterns（日本語訳：エンゲージメントパターン） |
| LinkedIn（日本語訳：リンクトイン） | Job titles, companies, industries（日本語訳：役職、会社、業種） | Professional identity（日本語訳：プロフェッショナルとしてのアイデンティティ） |

### Key Concepts （日本語訳：主要な概念）

- **Lookalikes**: Base on best customers (by LTV), not all customers （日本語訳：**類似品**: すべての顧客ではなく、最良の顧客 (LTV による) に基づいています。）
- **Retargeting**: Segment by funnel stage (visitors vs. cart abandoners) （日本語訳：**リターゲティング**: ファネル段階ごとのセグメント化 (訪問者とカート放棄者)）
- **Exclusions**: Always exclude existing customers and recent converters （日本語訳：**除外**: 既存の顧客と最近のコンバーターを常に除外します。）

**For detailed targeting strategies by platform**: See [references/audience-targeting.md](references/audience-targeting.md) （日本語訳：**プラットフォーム別のターゲティング戦略の詳細については**: [references/audience-targeting.md](references/audience-targeting.md) を参照してください。）

---

## Creative Best Practices （日本語訳：クリエイティブなベストプラクティス）

### Image Ads （日本語訳：イメージ広告）
- Clear product screenshots showing UI （日本語訳：UI を示す明確な製品スクリーンショット）
- Before/after comparisons （日本語訳：前後の比較）
- Stats and numbers as focal point （日本語訳：統計と数字が焦点）
- Human faces (real, not stock) （日本語訳：人間の顔 (ストックではなく本物)）
- Bold, readable text overlay (keep under 20%) （日本語訳：太字で読みやすいテキスト オーバーレイ (20% 未満に保つ)）

### Video Ads Structure (15-30 sec) （日本語訳：動画広告の構造 (15 ～ 30 秒)）
1. Hook (0-3 sec): Pattern interrupt, question, or bold statement （日本語訳：フック (0 ～ 3 秒): パターンの中断、質問、または太字のステートメント）
2. Problem (3-8 sec): Relatable pain point （日本語訳：問題 (3 ～ 8 秒): 共感できる問題点）
3. Solution (8-20 sec): Show product/benefit （日本語訳：解決策 (8 ～ 20 秒): 製品/メリットを表示する）
4. CTA (20-30 sec): Clear next step （日本語訳：CTA (20 ～ 30 秒): 次のステップをクリア）

**Production tips:** （日本語訳：**制作のヒント:**）
- Captions always (85% watch without sound) （日本語訳：常にキャプションが表示されます (85% は音声なしで視聴します)）
- Vertical for Stories/Reels, square for feed （日本語訳：ストーリー/リールの場合は垂直、フィードの場合は正方形）
- Native feel outperforms polished （日本語訳：洗練されたものを上回るネイティブな感触）
- First 3 seconds determine if they watch （日本語訳：最初の 3 秒で視聴するかどうかが決まります）

### Creative Testing Hierarchy （日本語訳：クリエイティブテストの階層）
1. Concept/angle (biggest impact) （日本語訳：コンセプト・アングル（最大のインパクト））
2. Hook/headline （日本語訳：フック/見出し）
3. Visual style （日本語訳：ビジュアルスタイル）
4. Body copy （日本語訳：ボディコピー）
5. CTA （日本語訳：CTA）

---

## Campaign Optimization （日本語訳：キャンペーンの最適化）

### Key Metrics by Objective （日本語訳：目的別の主要な指標）

| Objective（日本語訳：客観的） | Primary Metrics（日本語訳：主要な指標） |
|-----------|-----------------|
| Awareness（日本語訳：意識） | CPM, Reach, Video view rate（日本語訳：CPM、リーチ、動画視聴率） |
| Consideration（日本語訳：考慮） | CTR, CPC, Time on site（日本語訳：CTR、CPC、サイト滞在時間） |
| Conversion（日本語訳：変換） | CPA, ROAS, Conversion rate（日本語訳：CPA、ROAS、コンバージョン率） |

### Optimization Levers （日本語訳：最適化レバー）

**If CPA is too high:** （日本語訳：**CPA が高すぎる場合:**）
1. Check landing page (is the problem post-click?) （日本語訳：ランディング ページを確認します (問題はクリック後ですか?)）
2. Tighten audience targeting （日本語訳：対象ユーザーのターゲティングを厳格化する）
3. Test new creative angles （日本語訳：新しい創造的な角度をテストする）
4. Improve ad relevance/quality score （日本語訳：広告の関連性/品質スコアを向上させる）
5. Adjust bid strategy （日本語訳：入札戦略を調整する）

**If CTR is low:** （日本語訳：**CTR が低い場合:**）
- Creative isn't resonating → test new hooks/angles （日本語訳：クリエイティブが共感を呼んでいない → 新しいフックや角度をテストする）
- Audience mismatch → refine targeting （日本語訳：オーディエンスの不一致 → ターゲティングの調整）
- Ad fatigue → refresh creative （日本語訳：広告疲労 → クリエイティブをリフレッシュ）

**If CPM is high:** （日本語訳：**CPM が高い場合:**）
- Audience too narrow → expand targeting （日本語訳：オーディエンスが狭すぎる → ターゲティングを拡大する）
- High competition → try different placements （日本語訳：競争率が高い → 別の配置を試す）
- Low relevance score → improve creative fit （日本語訳：関連性スコアが低い → クリエイティブの適合性が向上）

### Bid Strategy Progression （日本語訳：入札戦略の進行状況）
1. Start with manual or cost caps （日本語訳：手動またはコストの上限から始める）
2. Gather conversion data (50+ conversions) （日本語訳：コンバージョン データを収集する (50 件以上のコンバージョン)）
3. Switch to automated with targets based on historical data （日本語訳：履歴データに基づいたターゲットによる自動化に切り替える）
4. Monitor and adjust targets based on results （日本語訳：結果に基づいて目標を監視および調整する）

---

## Retargeting Strategies （日本語訳：リターゲティング戦略）

### Funnel-Based Approach （日本語訳：ファネルベースのアプローチ）

| Funnel Stage（日本語訳：ファンネルステージ） | Audience（日本語訳：観客） | Message（日本語訳：メッセージ） | Goal（日本語訳：ゴール） |
|--------------|----------|---------|------|
| Top（日本語訳：トップ） | Blog readers, video viewers（日本語訳：ブログの読者、ビデオの閲覧者） | Educational, social proof（日本語訳：教育的、社会的証明） | Move to consideration（日本語訳：検討に移る） |
| Middle（日本語訳：真ん中） | Pricing/feature page visitors（日本語訳：価格設定/特集ページの訪問者） | Case studies, demos（日本語訳：ケーススタディ、デモ） | Move to decision（日本語訳：決定に移る） |
| Bottom（日本語訳：底） | Cart abandoners, trial users（日本語訳：カート放棄者、トライアルユーザー） | Urgency, objection handling（日本語訳：緊急性、異議申し立てへの対応） | Convert（日本語訳：変換する） |

### Retargeting Windows （日本語訳：Windows のリターゲット）

| Stage（日本語訳：ステージ） | Window（日本語訳：ウィンドウ） | Frequency Cap（日本語訳：フリークエンシーキャップ） |
|-------|--------|---------------|
| Hot (cart/trial)（日本語訳：ホット（カート/トライアル）） | 1-7 days（日本語訳：1～7日） | Higher OK（日本語訳：それ以上OK） |
| Warm (key pages)（日本語訳：暖かい (主要ページ)） | 7-30 days（日本語訳：7～30日） | 3-5x/week（日本語訳：週に3～5回） |
| Cold (any visit)（日本語訳：寒い（どの訪問でも）） | 30-90 days（日本語訳：30～90日） | 1-2x/week（日本語訳：週に1～2回） |

### Exclusions to Set Up （日本語訳：設定する除外項目）
- Existing customers (unless upsell) （日本語訳：既存の顧客 (アップセルを除く)）
- Recent converters (7-14 day window) （日本語訳：最近のコンバーター (7 ～ 14 日間)）
- Bounced visitors (<10 sec) （日本語訳：直帰した訪問者 (10 秒未満)）
- Irrelevant pages (careers, support) （日本語訳：無関係なページ (キャリア、サポート)）

---

## Reporting & Analysis （日本語訳：レポートと分析）

### Weekly Review （日本語訳：週次レビュー）
- Spend vs. budget pacing （日本語訳：支出と予算のペース）
- CPA/ROAS vs. targets （日本語訳：CPA/ROAS と目標の比較）
- Top and bottom performing ads （日本語訳：パフォーマンスの上位と下位の広告）
- Audience performance breakdown （日本語訳：観客のパフォーマンスの内訳）
- Frequency check (fatigue risk) （日本語訳：頻度チェック（疲労リスク））
- Landing page conversion rate （日本語訳：ランディングページのコンバージョン率）

### Attribution Considerations （日本語訳：帰属に関する考慮事項）
- Platform attribution is inflated （日本語訳：プラットフォームの帰属が誇張されている）
- Use UTM parameters consistently （日本語訳：UTMパラメータを一貫して使用する）
- Compare platform data to GA4 （日本語訳：プラットフォーム データを GA4 と比較する）
- Look at blended CAC, not just platform CPA （日本語訳：プラットフォーム CPA だけでなく、複合 CAC にも注目してください）

---

## Platform Setup （日本語訳：プラットフォームのセットアップ）

Before launching campaigns, ensure proper tracking and account setup. （日本語訳：キャンペーンを開始する前に、適切なトラッキングとアカウント設定を確認してください。）

**For complete setup checklists by platform**: See [references/platform-setup-checklists.md](references/platform-setup-checklists.md) （日本語訳：**プラットフォーム別の完全なセットアップ チェックリストについては**: [references/platform-setup-checklists.md](references/platform-setup-checklists.md) を参照してください。）

### Universal Pre-Launch Checklist （日本語訳：ユニバーサル発売前チェックリスト）
- [ ] Conversion tracking tested with real conversion （日本語訳：[ ] 実際のコンバージョンでテストされたコンバージョン トラッキング）
- [ ] Landing page loads fast (<3 sec) （日本語訳：[ ] ランディング ページの読み込みが速い (3 秒未満)）
- [ ] Landing page mobile-friendly （日本語訳：[ ] ランディング ページ モバイル対応）
- [ ] UTM parameters working （日本語訳：[ ] UTM パラメータが機能する）
- [ ] Budget set correctly （日本語訳：[ ] 予算が正しく設定されている）
- [ ] Targeting matches intended audience （日本語訳：[ ] ターゲティングが対象ユーザーと一致する）

---

## Common Mistakes to Avoid （日本語訳：避けるべきよくある間違い）

### Strategy （日本語訳：戦略）
- Launching without conversion tracking （日本語訳：コンバージョントラッキングなしで起動する）
- Too many campaigns (fragmenting budget) （日本語訳：キャンペーンが多すぎる（予算が細分化されている））
- Not giving algorithms enough learning time （日本語訳：アルゴリズムに十分な学習時間を与えていない）
- Optimizing for wrong metric （日本語訳：間違ったメトリクスに合わせて最適化する）

### Targeting （日本語訳：ターゲティング）
- Audiences too narrow or too broad （日本語訳：対象ユーザーが狭すぎる、または広すぎる）
- Not excluding existing customers （日本語訳：既存顧客を排除しない）
- Overlapping audiences competing （日本語訳：重複する視聴者が競合する）

### Creative （日本語訳：クリエイティブ）
- Only one ad per ad set （日本語訳：広告セットごとに広告は 1 つだけ）
- Not refreshing creative (fatigue) （日本語訳：クリエイティブがリフレッシュされない（疲労））
- Mismatch between ad and landing page （日本語訳：広告とランディング ページの不一致）

### Budget （日本語訳：予算）
- Spreading too thin across campaigns （日本語訳：キャンペーン間での広がりが薄すぎる）
- Making big budget changes (disrupts learning) （日本語訳：予算を大幅に変更する（学習を中断する））
- Stopping campaigns during learning phase （日本語訳：学習段階でのキャンペーンの停止）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What platform(s) are you currently running or want to start with? （日本語訳：現在実行しているプラ​​ットフォーム、またはこれから使い始めたいプラットフォームは何ですか?）
2. What's your monthly ad budget? （日本語訳：毎月の広告予算はいくらですか?）
3. What does a successful conversion look like (and what's it worth)? （日本語訳：成功した変換とはどのようなものですか (そしてその価値は何ですか)?）
4. Do you have existing creative assets or need to create them? （日本語訳：既存のクリエイティブ アセットがありますか、それとも作成する必要がありますか?）
5. What landing page will ads point to? （日本語訳：広告はどのランディング ページを指すのでしょうか?）
6. Do you have pixel/conversion tracking set up? （日本語訳：ピクセル/コンバージョン トラッキングを設定していますか?）

---

## Tool Integrations （日本語訳：ツールの統合）

For implementation, see the [tools registry](../../tools/REGISTRY.md). Key advertising platforms: （日本語訳：実装については、[ツール レジストリ](../../tools/REGISTRY.md) を参照してください。主要な広告プラットフォーム:）

| Platform（日本語訳：プラットフォーム） | Best For（日本語訳：最適な用途） | MCP（日本語訳：MCP） | Guide（日本語訳：ガイド） |
|----------|----------|:---:|-------|
| **Google Ads**（日本語訳：**Google 広告**） | Search intent, high-intent traffic（日本語訳：検索目的、高目的トラフィ​​ック） | ✓ | [google-ads.md](../../tools/integrations/google-ads.md)（日本語訳：[google-ads.md](../../tools/integrations/google-ads.md)） |
| **Meta Ads**（日本語訳：**メタ広告**） | Demand gen, visual products, B2C（日本語訳：需要創出、ビジュアルプロダクト、B2C） | - | [meta-ads.md](../../tools/integrations/meta-ads.md)（日本語訳：[meta-ads.md](../../tools/integrations/meta-ads.md)） |
| **LinkedIn Ads**（日本語訳：**LinkedIn 広告**） | B2B, job title targeting（日本語訳：B2B、役職ターゲティング） | - | [linkedin-ads.md](../../tools/integrations/linkedin-ads.md)（日本語訳：[linkedin-ads.md](../../tools/integrations/linkedin-ads.md)） |
| **TikTok Ads**（日本語訳：**TikTok 広告**） | Younger demographics, video（日本語訳：若年層、ビデオ） | - | [tiktok-ads.md](../../tools/integrations/tiktok-ads.md)（日本語訳：[tiktok-ads.md](../../tools/integrations/tiktok-ads.md)） |

For tracking, see also: [ga4.md](../../tools/integrations/ga4.md), [segment.md](../../tools/integrations/segment.md) （日本語訳：追跡については、次も参照してください: [ga4.md](../../tools/integrations/ga4.md)、[segment.md](../../tools/integrations/segment.md)）

---

## Related Skills （日本語訳：関連スキル）

- **copywriting**: For landing page copy that converts ad traffic （日本語訳：**コピーライティング**: 広告トラフィックを変換するランディング ページのコピー用）
- **analytics-tracking**: For proper conversion tracking setup （日本語訳：**analytics-tracking**: 適切なコンバージョン トラッキング設定用）
- **ab-test-setup**: For landing page testing to improve ROAS （日本語訳：**ab-test-setup**: ROAS を改善するためのランディング ページのテスト用）
- **page-cro**: For optimizing post-click conversion rates （日本語訳：**page-cro**: クリック後のコンバージョン率を最適化するため）
