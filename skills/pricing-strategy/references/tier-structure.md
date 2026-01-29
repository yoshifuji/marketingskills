# Tier Structure and Packaging （日本語訳：階層構造とパッケージング）

## How Many Tiers? （日本語訳：階層は何層ですか?）

**2 tiers:** Simple, clear choice （日本語訳：**2 層:** シンプルで明確な選択）
- Works for: Clear SMB vs. Enterprise split （日本語訳：対象: SMB とエンタープライズの明確な分割）
- Risk: May leave money on table （日本語訳：リスク: テーブルにお金が残る可能性があります）

**3 tiers:** Industry standard （日本語訳：**3 層:** 業界標準）
- Good tier = Entry point （日本語訳：良好な層 = エントリーポイント）
- Better tier = Recommended (anchor to best) （日本語訳：より良い層 = 推奨 (最適なものへのアンカー)）
- Best tier = High-value customers （日本語訳：最良の層 = 価値の高い顧客）

**4+ tiers:** More granularity （日本語訳：**4 層以上:** より詳細な粒度）
- Works for: Wide range of customer sizes （日本語訳：対象: 幅広い顧客規模）
- Risk: Decision paralysis, complexity （日本語訳：リスク: 意思決定の麻痺、複雑さ）

---

## Good-Better-Best Framework （日本語訳：Good-Better-Best フレームワーク）

**Good tier (Entry):** （日本語訳：**良い層 (エントリー):**）
- Purpose: Remove barriers to entry （日本語訳：目的: 参入障壁を取り除く）
- Includes: Core features, limited usage （日本語訳：含まれるもの: コア機能、限定された使用法）
- Price: Low, accessible （日本語訳：価格：低価格、アクセスしやすい）
- Target: Small teams, try before you buy （日本語訳：対象: 小規模チーム、購入前にお試しください）

**Better tier (Recommended):** （日本語訳：**より良い層 (推奨):**）
- Purpose: Where most customers land （日本語訳：目的: ほとんどの顧客が到着する場所）
- Includes: Full features, reasonable limits （日本語訳：含まれるもの: フル機能、妥当な制限）
- Price: Your "anchor" price （日本語訳：価格: あなたの「アンカー」価格）
- Target: Growing teams, serious users （日本語訳：ターゲット: 成長中のチーム、本格的なユーザー）

**Best tier (Premium):** （日本語訳：**最高レベル (プレミアム):**）
- Purpose: Capture high-value customers （日本語訳：目的: 価値の高い顧客を獲得する）
- Includes: Everything, advanced features, higher limits （日本語訳：含まれるもの: すべて、高度な機能、より高い制限）
- Price: Premium (often 2-3x "Better") （日本語訳：価格: プレミアム (多くの場合 2 ～ 3 倍の「優れた」)）
- Target: Larger teams, power users, enterprises （日本語訳：対象: 大規模なチーム、パワー ユーザー、企業）

---

## Tier Differentiation Strategies （日本語訳：階層差別化戦略）

**Feature gating:** （日本語訳：**機能ゲーティング:**）
- Basic features in all tiers （日本語訳：すべてのレベルの基本機能）
- Advanced features in higher tiers （日本語訳：上位層の高度な機能）
- Works when features have clear value differences （日本語訳：特徴に明確な値の違いがある場合に機能します）

**Usage limits:** （日本語訳：**使用制限:**）
- Same features, different limits （日本語訳：同じ機能、異なる制限）
- More users, storage, API calls at higher tiers （日本語訳：上位層でのユーザー、ストレージ、API コールの増加）
- Works when value scales with usage （日本語訳：使用量に応じて値が増減する場合に機能します）

**Support level:** （日本語訳：**サポートレベル:**）
- Email support → Priority support → Dedicated success （日本語訳：電子メールサポート → 優先サポート → 専用のサポート）
- Works for products with implementation complexity （日本語訳：実装が複雑な製品にも対応）

**Access and customization:** （日本語訳：**アクセスとカスタマイズ:**）
- API access, SSO, custom branding （日本語訳：API アクセス、SSO、カスタム ブランディング）
- Works for enterprise differentiation （日本語訳：企業の差別化に貢献）

---

## Example Tier Structure （日本語訳：階層構造の例）

```
┌────────────────┬─────────────────┬─────────────────┬─────────────────┐
│                │ Starter         │ Pro             │ Business        │
│                │ $29/mo          │ $79/mo          │ $199/mo         │
├────────────────┼─────────────────┼─────────────────┼─────────────────┤
│ Users          │ Up to 5         │ Up to 20        │ Unlimited       │
│ Projects       │ 10              │ Unlimited       │ Unlimited       │
│ Storage        │ 5 GB            │ 50 GB           │ 500 GB          │
│ Integrations   │ 3               │ 10              │ Unlimited       │
│ Analytics      │ Basic           │ Advanced        │ Custom          │
│ Support        │ Email           │ Priority        │ Dedicated       │
│ API Access     │ ✗               │ ✓               │ ✓               │
│ SSO            │ ✗               │ ✗               │ ✓               │
│ Audit logs     │ ✗               │ ✗               │ ✓               │
└────────────────┴─────────────────┴─────────────────┴─────────────────┘
```

---

## Packaging for Personas （日本語訳：ペルソナ向けのパッケージング）

### Identifying Pricing Personas （日本語訳：価格設定ペルソナの特定）

Different customers have different: （日本語訳：顧客ごとに次のような違いがあります。）
- Willingness to pay （日本語訳：支払い意思）
- Feature needs （日本語訳：機能のニーズ）
- Buying processes （日本語訳：購入プロセス）
- Value perception （日本語訳：価値観）

**Segment by:** （日本語訳：**セグメント化:**）
- Company size (solopreneur → SMB → enterprise) （日本語訳：会社規模（個人事業主→中小企業→大企業））
- Use case (marketing vs. sales vs. support) （日本語訳：使用例 (マーケティング vs 販売 vs サポート)）
- Sophistication (beginner → power user) （日本語訳：洗練（初心者→パワーユーザー））
- Industry (different budget norms) （日本語訳：業界 (予算基準が異なる)）

### Persona-Based Packaging （日本語訳：ペルソナベースのパッケージング）

**Step 1: Define personas** （日本語訳：**ステップ 1: ペルソナを定義する**）

| Persona（日本語訳：ペルソナ） | Size（日本語訳：サイズ） | Needs（日本語訳：ニーズ） | WTP（日本語訳：浄水場） | Example（日本語訳：例） |
|---------|------|-------|-----|---------|
| Freelancer（日本語訳：フリーランサー） | 1 person（日本語訳：1名） | Basic features（日本語訳：基本機能） | Low（日本語訳：低い） | $19/mo（日本語訳：$19/月） |
| Small Team（日本語訳：小規模チーム） | 2-10 | Collaboration（日本語訳：コラボレーション） | Medium（日本語訳：中くらい） | $49/mo（日本語訳：$49/月） |
| Growing Co（日本語訳：成長する会社） | 10-50 | Scale, integrations（日本語訳：スケール、統合） | Higher（日本語訳：より高い） | $149/mo（日本語訳：$149/月） |
| Enterprise（日本語訳：企業） | 50+ | Security, support（日本語訳：セキュリティ、サポート） | High（日本語訳：高い） | Custom（日本語訳：カスタム） |

**Step 2: Map features to personas** （日本語訳：**ステップ 2: 特徴をペルソナにマッピングする**）

| Feature（日本語訳：特徴） | Freelancer（日本語訳：フリーランサー） | Small Team（日本語訳：小規模チーム） | Growing（日本語訳：成長する） | Enterprise（日本語訳：企業） |
|---------|------------|------------|---------|------------|
| Core features（日本語訳：コア機能） | ✓ | ✓ | ✓ | ✓ |
| Collaboration（日本語訳：コラボレーション） | — | ✓ | ✓ | ✓ |
| Integrations（日本語訳：統合） | — | Limited（日本語訳：限定） | Full（日本語訳：満杯） | Full（日本語訳：満杯） |
| API access（日本語訳：APIアクセス） | — | — | ✓ | ✓ |
| SSO/SAML（日本語訳：SSO/SAML） | — | — | — | ✓ |
| Audit logs（日本語訳：監査ログ） | — | — | — | ✓ |
| Custom contract（日本語訳：カスタム契約） | — | — | — | ✓ |

**Step 3: Price to value for each persona** （日本語訳：**ステップ 3: 各ペルソナの価格対価値**）
- Research willingness to pay per segment （日本語訳：セグメントごとの支払い意欲を調査）
- Set prices that capture value without blocking adoption （日本語訳：導入を妨げることなく価値を獲得できる価格を設定する）
- Consider segment-specific landing pages （日本語訳：セグメント固有のランディング ページを検討する）

---

## Freemium vs. Free Trial （日本語訳：フリーミアムと無料トライアル）

### When to Use Freemium （日本語訳：フリーミアムを使用する場合）

**Freemium works when:** （日本語訳：**フリーミアムは次の場合に機能します:**）
- Product has viral/network effects （日本語訳：製品にはウイルス/ネットワーク効果があります）
- Free users provide value (content, data, referrals) （日本語訳：無料ユーザーは価値を提供します (コンテンツ、データ、紹介)）
- Large market where % conversion drives volume （日本語訳：コンバージョン率がボリュームを高める大規模市場）
- Low marginal cost to serve free users （日本語訳：無料ユーザーにサービスを提供するための低い限界コスト）
- Clear feature/usage limits for upgrade trigger （日本語訳：アップグレードトリガーの機能/使用制限を明確にする）

**Freemium risks:** （日本語訳：**フリーミアムのリスク:**）
- Free users may never convert （日本語訳：無料ユーザーは変換できない）
- Devalues product perception （日本語訳：製品に対する認識の価値を下げる）
- Support costs for non-paying users （日本語訳：無料ユーザーのサポート費用）
- Harder to raise prices later （日本語訳：後から値上げするのが難しくなる）

### When to Use Free Trial （日本語訳：無料トライアルを使用する場合）

**Free trial works when:** （日本語訳：**無料トライアルは次の場合に機能します。**）
- Product needs time to demonstrate value （日本語訳：製品が価値を発揮するには時間がかかる）
- Onboarding/setup investment required （日本語訳：オンボーディング/セットアップへの投資が必要）
- B2B with buying committees （日本語訳：購買委員会との B2B）
- Higher price points （日本語訳：より高い価格帯）
- Product is "sticky" once configured （日本語訳：製品は一度設定されると「スティッキー」になります）

**Trial best practices:** （日本語訳：**トライアルのベスト プラクティス:**）
- 7-14 days for simple products （日本語訳：シンプルな商品の場合は7～14日）
- 14-30 days for complex products （日本語訳：複雑な製品の場合は 14 ～ 30 日）
- Full access (not feature-limited) （日本語訳：フルアクセス (機能制限なし)）
- Clear countdown and reminders （日本語訳：カウントダウンとリマインダーをクリアする）
- Credit card optional vs. required trade-off （日本語訳：クレジット カードのオプションと必須のトレードオフ）

**Credit card upfront:** （日本語訳：**クレジットカードによる前払い:**）
- Higher trial-to-paid conversion (40-50% vs. 15-25%) （日本語訳：トライアルから有料へのコンバージョン率が高い (40-50% 対 15-25%)）
- Lower trial volume （日本語訳：試用量を減らす）
- Better qualified leads （日本語訳：より優れた見込み客の獲得）

### Hybrid Approaches （日本語訳：ハイブリッドアプローチ）

**Freemium + Trial:** （日本語訳：**フリーミアム + トライアル:**）
- Free tier with limited features （日本語訳：機能が制限された無料枠）
- Trial of premium features （日本語訳：プレミアム機能のトライアル）
- Example: Zoom (free 40-min, trial of Pro) （日本語訳：例: Zoom (40 分間の無料トライアル、Pro のトライアル)）

**Reverse trial:** （日本語訳：**逆トライアル:**）
- Start with full access （日本語訳：フルアクセスで始める）
- After trial, downgrade to free tier （日本語訳：試用後、無料利用枠にダウングレード）
- Example: See premium value, live with limitations until ready （日本語訳：例: プレミアム価値を参照し、準備が整うまでは制限を設けてください）

---

## Enterprise Pricing （日本語訳：エンタープライズ価格）

### When to Add Custom Pricing （日本語訳：カスタム価格を追加する場合）

Add "Contact Sales" when: （日本語訳：次の場合に「営業担当者へのお問い合わせ」を追加します。）
- Deal sizes exceed $10k+ ARR （日本語訳：取引規模がARR10,000ドル以上を超える）
- Customers need custom contracts （日本語訳：顧客にはカスタム契約が必要です）
- Implementation/onboarding required （日本語訳：実装/オンボーディングが必要）
- Security/compliance requirements （日本語訳：セキュリティ/コンプライアンスの要件）
- Procurement processes involved （日本語訳：関連する調達プロセス）

### Enterprise Tier Elements （日本語訳：エンタープライズ層の要素）

**Table stakes:** （日本語訳：**テーブルステークス:**）
- SSO/SAML （日本語訳：SSO/SAML）
- Audit logs （日本語訳：監査ログ）
- Admin controls （日本語訳：管理者コントロール）
- Uptime SLA （日本語訳：稼働時間 SLA）
- Security certifications （日本語訳：セキュリティ認証）

**Value-adds:** （日本語訳：**付加価値:**）
- Dedicated support/success （日本語訳：献身的なサポート/成功）
- Custom onboarding （日本語訳：カスタムオンボーディング）
- Training sessions （日本語訳：トレーニングセッション）
- Custom integrations （日本語訳：カスタム統合）
- Priority roadmap input （日本語訳：優先ロードマップの入力）

### Enterprise Pricing Strategies （日本語訳：エンタープライズ価格戦略）

**Per-seat at scale:** （日本語訳：**座席ごとの規模:**）
- Volume discounts for large teams （日本語訳：大規模チーム向けのボリュームディスカウント）
- Example: $15/user (standard) → $10/user (100+) （日本語訳：例: $15/ユーザー (標準) → $10/ユーザー (100+)）

**Platform fee + usage:** （日本語訳：**プラットフォーム料金 + 使用量:**）
- Base fee for access （日本語訳：アクセス基本料金）
- Usage-based above thresholds （日本語訳：使用量ベースのしきい値超過）
- Example: $500/mo base + $0.01 per API call （日本語訳：例: 基本 $500/月 + API 呼び出しごとに $0.01）

**Value-based contracts:** （日本語訳：**価値ベースの契約:**）
- Price tied to customer's revenue/outcomes （日本語訳：価格は顧客の収益/成果に連動します）
- Example: % of transactions, revenue share （日本語訳：例: トランザクションの割合、収益分配率）
