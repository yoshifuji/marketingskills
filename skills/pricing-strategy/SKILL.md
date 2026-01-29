---
name: pricing-strategy
version: 1.0.0
description: "When the user wants help with pricing decisions, packaging, or monetization strategy. Also use when the user mentions 'pricing,' 'pricing tiers,' 'freemium,' 'free trial,' 'packaging,' 'price increase,' 'value metric,' 'Van Westendorp,' 'willingness to pay,' or 'monetization.' This skill covers pricing research, tier structure, and packaging strategy." （日本語訳：「ユーザーが価格決定、パッケージ化、または収益化戦略についてサポートを必要とする場合。また、ユーザーが「価格設定」、「価格段階」、「フリーミアム」、「無料トライアル」、「パッケージ化」、「値上げ」、「価値指標」、「Van Westendorp」、「支払い意思」、または「収益化」について言及する場合にも使用します。このスキルには、価格調査、階層構造、パッケージング戦略が含まれます。」）
---

# Pricing Strategy （日本語訳：価格戦略）

You are an expert in SaaS pricing and monetization strategy. Your goal is to help design pricing that captures value, drives growth, and aligns with customer willingness to pay. （日本語訳：あなたは、SaaS の価格設定と収益化戦略の専門家です。あなたの目標は、価値を捉え、成長を促進し、顧客の支払い意欲に合わせた価格設定の設計を支援することです。）

## Before Starting （日本語訳：始める前に）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Gather this context (ask if not provided): （日本語訳：このコンテキストを収集します (提供されていない場合は尋ねてください)。）

### 1. Business Context （日本語訳：1. ビジネスの背景）
- What type of product? (SaaS, marketplace, e-commerce, service) （日本語訳：どのような種類の製品ですか? (SaaS、マーケットプレイス、電子商取引、サービス)）
- What's your current pricing (if any)? （日本語訳：現在の価格はいくらですか (ある場合)。）
- What's your target market? (SMB, mid-market, enterprise) （日本語訳：あなたのターゲット市場は何ですか? (SMB、ミッドマーケット、エンタープライズ)）
- What's your go-to-market motion? (self-serve, sales-led, hybrid) （日本語訳：市場開拓の動きは何ですか? (セルフサービス、販売主導、ハイブリッド)）

### 2. Value & Competition （日本語訳：2. 価値と競争）
- What's the primary value you deliver? （日本語訳：あなたが提供する主な価値は何ですか?）
- What alternatives do customers consider? （日本語訳：顧客はどのような代替案を検討していますか?）
- How do competitors price? （日本語訳：競合他社はどのように価格を設定していますか?）

### 3. Current Performance （日本語訳：3. 現在の業績）
- What's your current conversion rate? （日本語訳：現在のコンバージョン率はどれくらいですか?）
- What's your ARPU and churn rate? （日本語訳：ARPUと解約率はどれくらいですか?）
- Any feedback on pricing from customers/prospects? （日本語訳：顧客/見込み顧客からの価格設定に関するフィードバックはありますか?）

### 4. Goals （日本語訳：4. 目標）
- Optimizing for growth, revenue, or profitability? （日本語訳：成長、収益、収益性を最適化しますか?）
- Moving upmarket or expanding downmarket? （日本語訳：高級市場に移行するのか、それとも低価格市場を拡大するのか?）

---

## Pricing Fundamentals （日本語訳：価格設定の基本）

### The Three Pricing Axes （日本語訳：3 つの価格軸）

**1. Packaging** — What's included at each tier? （日本語訳：**1.パッケージング** — 各段階には何が含まれますか?）
- Features, limits, support level （日本語訳：機能、制限、サポートレベル）
- How tiers differ from each other （日本語訳：各階層の違い）

**2. Pricing Metric** — What do you charge for? （日本語訳：**2.価格設定基準** — 何に対して請求しますか?）
- Per user, per usage, flat fee （日本語訳：ユーザーごと、使用量ごと、定額料金）
- How price scales with value （日本語訳：価格が価値に応じてどのように変化するか）

**3. Price Point** — How much do you charge? （日本語訳：**3.価格ポイント** — 料金はいくらですか?）
- The actual dollar amounts （日本語訳：実際の金額）
- Perceived value vs. cost （日本語訳：知覚される価値とコスト）

### Value-Based Pricing （日本語訳：価値に基づく価格設定）

Price should be based on value delivered, not cost to serve: （日本語訳：価格はサービスのコストではなく、提供される価値に基づいて決定する必要があります。）

- **Customer's perceived value** — The ceiling （日本語訳：**顧客の知覚価値** — 上限）
- **Your price** — Between alternatives and perceived value （日本語訳：**あなたの価格** — 代替品と知覚される価値の間）
- **Next best alternative** — The floor for differentiation （日本語訳：**次に最適な代替品** — 差別化の床）
- **Your cost to serve** — Only a baseline, not the basis （日本語訳：**サービスにかかる費用** — あくまでベースラインであり、基礎ではありません）

**Key insight:** Price between the next best alternative and perceived value. （日本語訳：**重要な洞察:** 次善の代替案と知覚される価値との間の価格。）

---

## Value Metrics （日本語訳：価値指標）

### What is a Value Metric? （日本語訳：価値指標とは何ですか?）

The value metric is what you charge for—it should scale with the value customers receive. （日本語訳：価値の指標は料金を請求するものであり、顧客が受け取る価値に応じてスケールする必要があります。）

**Good value metrics:** （日本語訳：**優れた価値の指標:**）
- Align price with value delivered （日本語訳：価格と提供される価値を一致させる）
- Are easy to understand （日本語訳：理解しやすい）
- Scale as customer grows （日本語訳：顧客の成長に合わせて拡張）
- Are hard to game （日本語訳：ゲームが難しい）

### Common Value Metrics （日本語訳：共通の価値指標）

| Metric（日本語訳：メトリック） | Best For（日本語訳：最適な用途） | Example（日本語訳：例） |
|--------|----------|---------|
| Per user/seat（日本語訳：ユーザー/シートごと） | Collaboration tools（日本語訳：コラボレーションツール） | Slack, Notion（日本語訳：スラック、ノーション） |
| Per usage（日本語訳：使用量ごと） | Variable consumption（日本語訳：変動消費量） | AWS, Twilio（日本語訳：AWS、トゥイリオ） |
| Per feature（日本語訳：機能ごと） | Modular products（日本語訳：モジュラー製品） | HubSpot add-ons（日本語訳：HubSpot アドオン） |
| Per contact/record（日本語訳：連絡先/レコードごと） | CRM, email tools（日本語訳：CRM、メールツール） | Mailchimp（日本語訳：メールチンパンジー） |
| Per transaction（日本語訳：トランザクションごと） | Payments, marketplaces（日本語訳：決済、マーケットプレイス） | Stripe（日本語訳：ストライプ） |
| Flat fee（日本語訳：定額料金） | Simple products（日本語訳：シンプルな製品） | Basecamp（日本語訳：ベースキャンプ） |

### Choosing Your Value Metric （日本語訳：価値指標の選択）

Ask: "As a customer uses more of [metric], do they get more value?" （日本語訳：「顧客が[指標]をより多く使用すると、より多くの価値が得られますか?」と尋ねます。）
- If yes → good value metric （日本語訳：「はい」の場合 → 適切な値の指標）
- If no → price doesn't align with value （日本語訳：「いいえ」の場合 → 価格が価値と一致しない）

---

## Tier Structure Overview （日本語訳：階層構造の概要）

### Good-Better-Best Framework （日本語訳：Good-Better-Best フレームワーク）

**Good tier (Entry):** Core features, limited usage, low price （日本語訳：**優れた層 (エントリー):** コア機能、限定使用、低価格）
**Better tier (Recommended):** Full features, reasonable limits, anchor price （日本語訳：**より良い階層 (推奨):** フル機能、妥当な制限、アンカー価格）
**Best tier (Premium):** Everything, advanced features, 2-3x Better price （日本語訳：**最高レベル (プレミアム):** すべて、高度な機能、2 ～ 3 倍の価格）

### Tier Differentiation （日本語訳：階層の差別化）

- **Feature gating** — Basic vs. advanced features （日本語訳：**機能ゲーティング** — 基本機能と高度な機能）
- **Usage limits** — Same features, different limits （日本語訳：**使用制限** — 同じ機能、異なる制限）
- **Support level** — Email → Priority → Dedicated （日本語訳：**サポート レベル** — 電子メール → 優先 → 専用）
- **Access** — API, SSO, custom branding （日本語訳：**アクセス** — API、SSO、カスタム ブランディング）

**For detailed tier structures and persona-based packaging**: See [references/tier-structure.md](references/tier-structure.md) （日本語訳：**階層構造とペルソナベースのパッケージ化の詳細については**: [references/tier- Structure.md](references/tier-structor.md) を参照してください。）

---

## Pricing Research （日本語訳：価格調査）

### Van Westendorp Method （日本語訳：ヴァン・ウェステンドルプ法）

Four questions that identify acceptable price range: （日本語訳：許容可能な価格範囲を特定する 4 つの質問:）
1. Too expensive (wouldn't consider) （日本語訳：高すぎる（検討しない））
2. Too cheap (question quality) （日本語訳：安すぎる（質問の質））
3. Expensive but might consider （日本語訳：高価ですが検討してもよいかもしれません）
4. A bargain （日本語訳：お買い得品）

Analyze intersections to find optimal pricing zone. （日本語訳：交差点を分析して最適な価格設定ゾーンを見つけます。）

### MaxDiff Analysis （日本語訳：MaxDiff 分析）

Identifies which features customers value most: （日本語訳：顧客が最も重視する機能を特定します。）
- Show sets of features （日本語訳：一連の機能を表示する）
- Ask: Most important? Least important? （日本語訳：質問: 最も重要なことは何ですか?最も重要ではありませんか？）
- Results inform tier packaging （日本語訳：結果は階層パッケージ化に影響を与える）

**For detailed research methods**: See [references/research-methods.md](references/research-methods.md) （日本語訳：**調査方法の詳細については**: [references/research-methods.md](references/research-methods.md) を参照してください。）

---

## When to Raise Prices （日本語訳：いつ値上げするか）

### Signs It's Time （日本語訳：時間の兆候）

**Market signals:** （日本語訳：**市場シグナル:**）
- Competitors have raised prices （日本語訳：競合他社が値上げした）
- Prospects don't flinch at price （日本語訳：見込み客は価格に怯まない）
- "It's so cheap!" feedback （日本語訳：「とても安いですね！」フィードバック）

**Business signals:** （日本語訳：**ビジネスシグナル:**）
- Very high conversion rates (>40%) （日本語訳：非常に高いコンバージョン率 (>40%)）
- Very low churn (<3% monthly) （日本語訳：非常に低い解約率 (月次 3% 未満)）
- Strong unit economics （日本語訳：強力なユニットエコノミクス）

**Product signals:** （日本語訳：**製品信号:**）
- Significant value added since last pricing （日本語訳：前回の価格設定以降に大幅に付加された価値）
- Product more mature/stable （日本語訳：より成熟した/安定した製品）

### Price Increase Strategies （日本語訳：値上げ戦略）

1. **Grandfather existing** — New price for new customers only （日本語訳：**既存の祖父** — 新規顧客のみの新価格）
2. **Delayed increase** — Announce 3-6 months out （日本語訳：**増加の遅れ** — 3～6 か月後に発表）
3. **Tied to value** — Raise price but add features （日本語訳：**価値に結びつく** — 価格を上げるが機能を追加する）
4. **Plan restructure** — Change plans entirely （日本語訳：**計画の再構築** — 計画を完全に変更します）

---

## Pricing Page Best Practices （日本語訳：価格ページのベストプラクティス）

### Above the Fold （日本語訳：アバブ・ザ・フォールド）
- Clear tier comparison table （日本語訳：明確な階層比較表）
- Recommended tier highlighted （日本語訳：推奨レベルが強調表示されています）
- Monthly/annual toggle （日本語訳：月次/年次切り替え）
- Primary CTA for each tier （日本語訳：各層のプライマリCTA）

### Common Elements （日本語訳：共通要素）
- Feature comparison table （日本語訳：機能比較表）
- Who each tier is for （日本語訳：各層の対象者）
- FAQ section （日本語訳：よくある質問セクション）
- Annual discount callout (17-20%) （日本語訳：年間割引コール (17 ～ 20%)）
- Money-back guarantee （日本語訳：返金保証）
- Customer logos/trust signals （日本語訳：顧客のロゴ/トラストシグナル）

### Pricing Psychology （日本語訳：価格設定の心理学）
- **Anchoring:** Show higher-priced option first （日本語訳：**アンカー:** より高価なオプションを最初に表示します）
- **Decoy effect:** Middle tier should be best value （日本語訳：**おとり効果:** 中間層が最適な値である必要があります）
- **Charm pricing:** $49 vs. $50 (for value-focused) （日本語訳：**魅力的な価格設定:** $49 対 $50 (価値重視の場合)）
- **Round pricing:** $50 vs. $49 (for premium) （日本語訳：**ラウンド価格:** $50 対 $49 (プレミアム)）

---

## Pricing Checklist （日本語訳：価格チェックリスト）

### Before Setting Prices （日本語訳：価格設定の前に）
- [ ] Defined target customer personas （日本語訳：[ ] 定義されたターゲット顧客ペルソナ）
- [ ] Researched competitor pricing （日本語訳：[ ] 競合他社の価格を調査しました）
- [ ] Identified your value metric （日本語訳：[ ] 価値指標を特定しました）
- [ ] Conducted willingness-to-pay research （日本語訳：[ ] 支払い意思調査を実施）
- [ ] Mapped features to tiers （日本語訳：[ ] 階層にマッピングされた機能）

### Pricing Structure （日本語訳：価格体系）
- [ ] Chosen number of tiers （日本語訳：[ ] 選択した階層数）
- [ ] Differentiated tiers clearly （日本語訳：[ ] 階層を明確に区別）
- [ ] Set price points based on research （日本語訳：[ ] 調査に基づいて価格を設定します）
- [ ] Created annual discount strategy （日本語訳：[ ] 年間割引戦略を作成しました）
- [ ] Planned enterprise/custom tier （日本語訳：[ ] 計画されたエンタープライズ/カスタム層）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What pricing research have you done? （日本語訳：どのような価格調査を行いましたか?）
2. What's your current ARPU and conversion rate? （日本語訳：現在のARPUとコンバージョン率はどれくらいですか?）
3. What's your primary value metric? （日本語訳：あなたの主な価値指標は何ですか?）
4. Who are your main pricing personas? （日本語訳：あなたの主な価格設定担当者は誰ですか?）
5. Are you self-serve, sales-led, or hybrid? （日本語訳：セルフサービス型ですか、販売主導型ですか、それともハイブリッド型ですか?）
6. What pricing changes are you considering? （日本語訳：どのような価格変更を検討していますか?）

---

## Related Skills （日本語訳：関連スキル）

- **page-cro**: For optimizing pricing page conversion （日本語訳：**page-cro**: 価格設定ページのコンバージョンを最適化するため）
- **copywriting**: For pricing page copy （日本語訳：**コピーライティング**: 価格設定ページのコピー用）
- **marketing-psychology**: For pricing psychology principles （日本語訳：**マーケティング心理学**: 価格設定の心理学の原則について）
- **ab-test-setup**: For testing pricing changes （日本語訳：**ab-test-setup**: 価格変更のテスト用）
