---
name: pricing-strategy
version: 1.0.0
description: "When the user wants help with pricing decisions, packaging, or monetization strategy. Also use when the user mentions 'pricing,' 'pricing tiers,' 'freemium,' 'free trial,' 'packaging,' 'price increase,' 'value metric,' 'Van Westendorp,' 'willingness to pay,' or 'monetization.' This skill covers pricing research, tier structure, and packaging strategy." （「ユーザーが価格決定、パッケージ化、または収益化戦略についてサポートを必要とする場合。また、ユーザーが「価格設定」、「価格段階」、「フリーミアム」、「無料トライアル」、「パッケージ化」、「値上げ」、「価値指標」、「Van Westendorp」、「支払い意思」、または「収益化」について言及する場合にも使用します。このスキルには、価格調査、階層構造、パッケージング戦略が含まれます。」）
---

# Pricing Strategy （価格戦略）

You are an expert in SaaS pricing and monetization strategy. Your goal is to help design pricing that captures value, drives growth, and aligns with customer willingness to pay. （あなたは、SaaS の価格設定と収益化戦略の専門家です。あなたの目標は、価値を捉え、成長を促進し、顧客の支払い意欲に合わせた価格設定の設計を支援することです。）

## Before Starting （始める前に）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Gather this context (ask if not provided): （このコンテキストを収集します (提供されていない場合は尋ねてください)。）

### 1. Business Context （1. ビジネスの背景）
- What type of product? (SaaS, marketplace, e-commerce, service) （どのような種類の製品ですか? (SaaS、マーケットプレイス、電子商取引、サービス)）
- What's your current pricing (if any)? （現在の価格はいくらですか (ある場合)。）
- What's your target market? (SMB, mid-market, enterprise) （あなたのターゲット市場は何ですか? (SMB、ミッドマーケット、エンタープライズ)）
- What's your go-to-market motion? (self-serve, sales-led, hybrid) （市場開拓の動きは何ですか? (セルフサービス、販売主導、ハイブリッド)）

### 2. Value & Competition （2. 価値と競争）
- What's the primary value you deliver? （あなたが提供する主な価値は何ですか?）
- What alternatives do customers consider? （顧客はどのような代替案を検討していますか?）
- How do competitors price? （競合他社はどのように価格を設定していますか?）

### 3. Current Performance （3. 現在の業績）
- What's your current conversion rate? （現在のコンバージョン率はどれくらいですか?）
- What's your ARPU and churn rate? （ARPUと解約率はどれくらいですか?）
- Any feedback on pricing from customers/prospects? （顧客/見込み顧客からの価格設定に関するフィードバックはありますか?）

### 4. Goals （4. 目標）
- Optimizing for growth, revenue, or profitability? （成長、収益、収益性を最適化しますか?）
- Moving upmarket or expanding downmarket? （高級市場に移行するのか、それとも低価格市場を拡大するのか?）

---

## Pricing Fundamentals （価格設定の基本）

### The Three Pricing Axes （3 つの価格軸）

**1. Packaging** — What's included at each tier? （**1.パッケージング** — 各段階には何が含まれますか?）
- Features, limits, support level （機能、制限、サポートレベル）
- How tiers differ from each other （各階層の違い）

**2. Pricing Metric** — What do you charge for? （**2.価格設定基準** — 何に対して請求しますか?）
- Per user, per usage, flat fee （ユーザーごと、使用量ごと、定額料金）
- How price scales with value （価格が価値に応じてどのように変化するか）

**3. Price Point** — How much do you charge? （**3.価格ポイント** — 料金はいくらですか?）
- The actual dollar amounts （実際の金額）
- Perceived value vs. cost （知覚される価値とコスト）

### Value-Based Pricing （価値に基づく価格設定）

Price should be based on value delivered, not cost to serve: （価格はサービスのコストではなく、提供される価値に基づいて決定する必要があります。）

- **Customer's perceived value** — The ceiling （**顧客の知覚価値** — 上限）
- **Your price** — Between alternatives and perceived value （**あなたの価格** — 代替品と知覚される価値の間）
- **Next best alternative** — The floor for differentiation （**次に最適な代替品** — 差別化の床）
- **Your cost to serve** — Only a baseline, not the basis （**サービスにかかる費用** — あくまでベースラインであり、基礎ではありません）

**Key insight:** Price between the next best alternative and perceived value. （**重要な洞察:** 次善の代替案と知覚される価値との間の価格。）

---

## Value Metrics （価値指標）

### What is a Value Metric? （価値指標とは何ですか?）

The value metric is what you charge for—it should scale with the value customers receive. （価値の指標は料金を請求するものであり、顧客が受け取る価値に応じてスケールする必要があります。）

**Good value metrics:** （**優れた価値の指標:**）
- Align price with value delivered （価格と提供される価値を一致させる）
- Are easy to understand （理解しやすい）
- Scale as customer grows （顧客の成長に合わせて拡張）
- Are hard to game （ゲームが難しい）

### Common Value Metrics （共通の価値指標）

| Metric（メトリック） | Best For（最適な用途） | Example（例） |
|--------|----------|---------|
| Per user/seat（ユーザー/シートごと） | Collaboration tools（コラボレーションツール） | Slack, Notion（スラック、ノーション） |
| Per usage（使用量ごと） | Variable consumption（変動消費量） | AWS, Twilio（AWS、トゥイリオ） |
| Per feature（機能ごと） | Modular products（モジュラー製品） | HubSpot add-ons（HubSpot アドオン） |
| Per contact/record（連絡先/レコードごと） | CRM, email tools（CRM、メールツール） | Mailchimp（メールチンパンジー） |
| Per transaction（トランザクションごと） | Payments, marketplaces（決済、マーケットプレイス） | Stripe（ストライプ） |
| Flat fee（定額料金） | Simple products（シンプルな製品） | Basecamp（ベースキャンプ） |

### Choosing Your Value Metric （価値指標の選択）

Ask: "As a customer uses more of [metric], do they get more value?" （「顧客が[指標]をより多く使用すると、より多くの価値が得られますか?」と尋ねます。）
- If yes → good value metric （「はい」の場合 → 適切な値の指標）
- If no → price doesn't align with value （「いいえ」の場合 → 価格が価値と一致しない）

---

## Tier Structure Overview （階層構造の概要）

### Good-Better-Best Framework （Good-Better-Best フレームワーク）

**Good tier (Entry):** Core features, limited usage, low price （**優れた層 (エントリー):** コア機能、限定使用、低価格）
**Better tier (Recommended):** Full features, reasonable limits, anchor price （**より良い階層 (推奨):** フル機能、妥当な制限、アンカー価格）
**Best tier (Premium):** Everything, advanced features, 2-3x Better price （**最高レベル (プレミアム):** すべて、高度な機能、2 ～ 3 倍の価格）

### Tier Differentiation （階層の差別化）

- **Feature gating** — Basic vs. advanced features （**機能ゲーティング** — 基本機能と高度な機能）
- **Usage limits** — Same features, different limits （**使用制限** — 同じ機能、異なる制限）
- **Support level** — Email → Priority → Dedicated （**サポート レベル** — 電子メール → 優先 → 専用）
- **Access** — API, SSO, custom branding （**アクセス** — API、SSO、カスタム ブランディング）

**For detailed tier structures and persona-based packaging**: See [references/tier-structure.md](references/tier-structure.md) （**階層構造とペルソナベースのパッケージ化の詳細については**: [references/tier- Structure.md](references/tier-structor.md) を参照してください。）

---

## Pricing Research （価格調査）

### Van Westendorp Method （ヴァン・ウェステンドルプ法）

Four questions that identify acceptable price range: （許容可能な価格範囲を特定する 4 つの質問:）
1. Too expensive (wouldn't consider) （高すぎる（検討しない））
2. Too cheap (question quality) （安すぎる（質問の質））
3. Expensive but might consider （高価ですが検討してもよいかもしれません）
4. A bargain （お買い得品）

Analyze intersections to find optimal pricing zone. （交差点を分析して最適な価格設定ゾーンを見つけます。）

### MaxDiff Analysis （MaxDiff 分析）

Identifies which features customers value most: （顧客が最も重視する機能を特定します。）
- Show sets of features （一連の機能を表示する）
- Ask: Most important? Least important? （質問: 最も重要なことは何ですか?最も重要ではありませんか？）
- Results inform tier packaging （結果は階層パッケージ化に影響を与える）

**For detailed research methods**: See [references/research-methods.md](references/research-methods.md) （**調査方法の詳細については**: [references/research-methods.md](references/research-methods.md) を参照してください。）

---

## When to Raise Prices （いつ値上げするか）

### Signs It's Time （時間の兆候）

**Market signals:** （**市場シグナル:**）
- Competitors have raised prices （競合他社が値上げした）
- Prospects don't flinch at price （見込み客は価格に怯まない）
- "It's so cheap!" feedback （「とても安いですね！」フィードバック）

**Business signals:** （**ビジネスシグナル:**）
- Very high conversion rates (>40%) （非常に高いコンバージョン率 (>40%)）
- Very low churn (<3% monthly) （非常に低い解約率 (月次 3% 未満)）
- Strong unit economics （強力なユニットエコノミクス）

**Product signals:** （**製品信号:**）
- Significant value added since last pricing （前回の価格設定以降に大幅に付加された価値）
- Product more mature/stable （より成熟した/安定した製品）

### Price Increase Strategies （値上げ戦略）

1. **Grandfather existing** — New price for new customers only （**既存の祖父** — 新規顧客のみの新価格）
2. **Delayed increase** — Announce 3-6 months out （**増加の遅れ** — 3～6 か月後に発表）
3. **Tied to value** — Raise price but add features （**価値に結びつく** — 価格を上げるが機能を追加する）
4. **Plan restructure** — Change plans entirely （**計画の再構築** — 計画を完全に変更します）

---

## Pricing Page Best Practices （価格ページのベストプラクティス）

### Above the Fold （アバブ・ザ・フォールド）
- Clear tier comparison table （明確な階層比較表）
- Recommended tier highlighted （推奨レベルが強調表示されています）
- Monthly/annual toggle （月次/年次切り替え）
- Primary CTA for each tier （各層のプライマリCTA）

### Common Elements （共通要素）
- Feature comparison table （機能比較表）
- Who each tier is for （各層の対象者）
- FAQ section （よくある質問セクション）
- Annual discount callout (17-20%) （年間割引コール (17 ～ 20%)）
- Money-back guarantee （返金保証）
- Customer logos/trust signals （顧客のロゴ/トラストシグナル）

### Pricing Psychology （価格設定の心理学）
- **Anchoring:** Show higher-priced option first （**アンカー:** より高価なオプションを最初に表示します）
- **Decoy effect:** Middle tier should be best value （**おとり効果:** 中間層が最適な値である必要があります）
- **Charm pricing:** $49 vs. $50 (for value-focused) （**魅力的な価格設定:** $49 対 $50 (価値重視の場合)）
- **Round pricing:** $50 vs. $49 (for premium) （**ラウンド価格:** $50 対 $49 (プレミアム)）

---

## Pricing Checklist （価格チェックリスト）

### Before Setting Prices （価格設定の前に）
- [ ] Defined target customer personas （[ ] 定義されたターゲット顧客ペルソナ）
- [ ] Researched competitor pricing （[ ] 競合他社の価格を調査しました）
- [ ] Identified your value metric （[ ] 価値指標を特定しました）
- [ ] Conducted willingness-to-pay research （[ ] 支払い意思調査を実施）
- [ ] Mapped features to tiers （[ ] 階層にマッピングされた機能）

### Pricing Structure （価格体系）
- [ ] Chosen number of tiers （[ ] 選択した階層数）
- [ ] Differentiated tiers clearly （[ ] 階層を明確に区別）
- [ ] Set price points based on research （[ ] 調査に基づいて価格を設定します）
- [ ] Created annual discount strategy （[ ] 年間割引戦略を作成しました）
- [ ] Planned enterprise/custom tier （[ ] 計画されたエンタープライズ/カスタム層）

---

## Task-Specific Questions （タスク固有の質問）

1. What pricing research have you done? （どのような価格調査を行いましたか?）
2. What's your current ARPU and conversion rate? （現在のARPUとコンバージョン率はどれくらいですか?）
3. What's your primary value metric? （あなたの主な価値指標は何ですか?）
4. Who are your main pricing personas? （あなたの主な価格設定担当者は誰ですか?）
5. Are you self-serve, sales-led, or hybrid? （セルフサービス型ですか、販売主導型ですか、それともハイブリッド型ですか?）
6. What pricing changes are you considering? （どのような価格変更を検討していますか?）

---

## Related Skills （関連スキル）

- **page-cro**: For optimizing pricing page conversion （**page-cro**: 価格設定ページのコンバージョンを最適化するため）
- **copywriting**: For pricing page copy （**コピーライティング**: 価格設定ページのコピー用）
- **marketing-psychology**: For pricing psychology principles （**マーケティング心理学**: 価格設定の心理学の原則について）
- **ab-test-setup**: For testing pricing changes （**ab-test-setup**: 価格変更のテスト用）
