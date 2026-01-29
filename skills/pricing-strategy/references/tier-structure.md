# Tier Structure and Packaging （階層構造とパッケージング）

## How Many Tiers? （階層は何層ですか?）

**2 tiers:** Simple, clear choice （**2 層:** シンプルで明確な選択）
- Works for: Clear SMB vs. Enterprise split （対象: SMB とエンタープライズの明確な分割）
- Risk: May leave money on table （リスク: テーブルにお金が残る可能性があります）

**3 tiers:** Industry standard （**3 層:** 業界標準）
- Good tier = Entry point （良好な層 = エントリーポイント）
- Better tier = Recommended (anchor to best) （より良い層 = 推奨 (最適なものへのアンカー)）
- Best tier = High-value customers （最良の層 = 価値の高い顧客）

**4+ tiers:** More granularity （**4 層以上:** より詳細な粒度）
- Works for: Wide range of customer sizes （対象: 幅広い顧客規模）
- Risk: Decision paralysis, complexity （リスク: 意思決定の麻痺、複雑さ）

---

## Good-Better-Best Framework （Good-Better-Best フレームワーク）

**Good tier (Entry):** （**良い層 (エントリー):**）
- Purpose: Remove barriers to entry （目的: 参入障壁を取り除く）
- Includes: Core features, limited usage （含まれるもの: コア機能、限定された使用法）
- Price: Low, accessible （価格：低価格、アクセスしやすい）
- Target: Small teams, try before you buy （対象: 小規模チーム、購入前にお試しください）

**Better tier (Recommended):** （**より良い層 (推奨):**）
- Purpose: Where most customers land （目的: ほとんどの顧客が到着する場所）
- Includes: Full features, reasonable limits （含まれるもの: フル機能、妥当な制限）
- Price: Your "anchor" price （価格: あなたの「アンカー」価格）
- Target: Growing teams, serious users （ターゲット: 成長中のチーム、本格的なユーザー）

**Best tier (Premium):** （**最高レベル (プレミアム):**）
- Purpose: Capture high-value customers （目的: 価値の高い顧客を獲得する）
- Includes: Everything, advanced features, higher limits （含まれるもの: すべて、高度な機能、より高い制限）
- Price: Premium (often 2-3x "Better") （価格: プレミアム (多くの場合 2 ～ 3 倍の「優れた」)）
- Target: Larger teams, power users, enterprises （対象: 大規模なチーム、パワー ユーザー、企業）

---

## Tier Differentiation Strategies （階層差別化戦略）

**Feature gating:** （**機能ゲーティング:**）
- Basic features in all tiers （すべてのレベルの基本機能）
- Advanced features in higher tiers （上位層の高度な機能）
- Works when features have clear value differences （特徴に明確な値の違いがある場合に機能します）

**Usage limits:** （**使用制限:**）
- Same features, different limits （同じ機能、異なる制限）
- More users, storage, API calls at higher tiers （上位層でのユーザー、ストレージ、API コールの増加）
- Works when value scales with usage （使用量に応じて値が増減する場合に機能します）

**Support level:** （**サポートレベル:**）
- Email support → Priority support → Dedicated success （電子メールサポート → 優先サポート → 専用のサポート）
- Works for products with implementation complexity （実装が複雑な製品にも対応）

**Access and customization:** （**アクセスとカスタマイズ:**）
- API access, SSO, custom branding （API アクセス、SSO、カスタム ブランディング）
- Works for enterprise differentiation （企業の差別化に貢献）

---

## Example Tier Structure （階層構造の例）

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

## Packaging for Personas （ペルソナ向けのパッケージング）

### Identifying Pricing Personas （価格設定ペルソナの特定）

Different customers have different: （顧客ごとに次のような違いがあります。）
- Willingness to pay （支払い意思）
- Feature needs （機能のニーズ）
- Buying processes （購入プロセス）
- Value perception （価値観）

**Segment by:** （**セグメント化:**）
- Company size (solopreneur → SMB → enterprise) （会社規模（個人事業主→中小企業→大企業））
- Use case (marketing vs. sales vs. support) （使用例 (マーケティング vs 販売 vs サポート)）
- Sophistication (beginner → power user) （洗練（初心者→パワーユーザー））
- Industry (different budget norms) （業界 (予算基準が異なる)）

### Persona-Based Packaging （ペルソナベースのパッケージング）

**Step 1: Define personas** （**ステップ 1: ペルソナを定義する**）

| Persona（ペルソナ） | Size（サイズ） | Needs（ニーズ） | WTP（浄水場） | Example（例） |
|---------|------|-------|-----|---------|
| Freelancer（フリーランサー） | 1 person（1名） | Basic features（基本機能） | Low（低い） | $19/mo（$19/月） |
| Small Team（小規模チーム） | 2-10 | Collaboration（コラボレーション） | Medium（中くらい） | $49/mo（$49/月） |
| Growing Co（成長する会社） | 10-50 | Scale, integrations（スケール、統合） | Higher（より高い） | $149/mo（$149/月） |
| Enterprise（企業） | 50+ | Security, support（セキュリティ、サポート） | High（高い） | Custom（カスタム） |

**Step 2: Map features to personas** （**ステップ 2: 特徴をペルソナにマッピングする**）

| Feature（特徴） | Freelancer（フリーランサー） | Small Team（小規模チーム） | Growing（成長する） | Enterprise（企業） |
|---------|------------|------------|---------|------------|
| Core features（コア機能） | ✓ | ✓ | ✓ | ✓ |
| Collaboration（コラボレーション） | — | ✓ | ✓ | ✓ |
| Integrations（統合） | — | Limited（限定） | Full（満杯） | Full（満杯） |
| API access（APIアクセス） | — | — | ✓ | ✓ |
| SSO/SAML（SSO/SAML） | — | — | — | ✓ |
| Audit logs（監査ログ） | — | — | — | ✓ |
| Custom contract（カスタム契約） | — | — | — | ✓ |

**Step 3: Price to value for each persona** （**ステップ 3: 各ペルソナの価格対価値**）
- Research willingness to pay per segment （セグメントごとの支払い意欲を調査）
- Set prices that capture value without blocking adoption （導入を妨げることなく価値を獲得できる価格を設定する）
- Consider segment-specific landing pages （セグメント固有のランディング ページを検討する）

---

## Freemium vs. Free Trial （フリーミアムと無料トライアル）

### When to Use Freemium （フリーミアムを使用する場合）

**Freemium works when:** （**フリーミアムは次の場合に機能します:**）
- Product has viral/network effects （製品にはウイルス/ネットワーク効果があります）
- Free users provide value (content, data, referrals) （無料ユーザーは価値を提供します (コンテンツ、データ、紹介)）
- Large market where % conversion drives volume （コンバージョン率がボリュームを高める大規模市場）
- Low marginal cost to serve free users （無料ユーザーにサービスを提供するための低い限界コスト）
- Clear feature/usage limits for upgrade trigger （アップグレードトリガーの機能/使用制限を明確にする）

**Freemium risks:** （**フリーミアムのリスク:**）
- Free users may never convert （無料ユーザーは変換できない）
- Devalues product perception （製品に対する認識の価値を下げる）
- Support costs for non-paying users （無料ユーザーのサポート費用）
- Harder to raise prices later （後から値上げするのが難しくなる）

### When to Use Free Trial （無料トライアルを使用する場合）

**Free trial works when:** （**無料トライアルは次の場合に機能します。**）
- Product needs time to demonstrate value （製品が価値を発揮するには時間がかかる）
- Onboarding/setup investment required （オンボーディング/セットアップへの投資が必要）
- B2B with buying committees （購買委員会との B2B）
- Higher price points （より高い価格帯）
- Product is "sticky" once configured （製品は一度設定されると「スティッキー」になります）

**Trial best practices:** （**トライアルのベスト プラクティス:**）
- 7-14 days for simple products （シンプルな商品の場合は7～14日）
- 14-30 days for complex products （複雑な製品の場合は 14 ～ 30 日）
- Full access (not feature-limited) （フルアクセス (機能制限なし)）
- Clear countdown and reminders （カウントダウンとリマインダーをクリアする）
- Credit card optional vs. required trade-off （クレジット カードのオプションと必須のトレードオフ）

**Credit card upfront:** （**クレジットカードによる前払い:**）
- Higher trial-to-paid conversion (40-50% vs. 15-25%) （トライアルから有料へのコンバージョン率が高い (40-50% 対 15-25%)）
- Lower trial volume （試用量を減らす）
- Better qualified leads （より優れた見込み客の獲得）

### Hybrid Approaches （ハイブリッドアプローチ）

**Freemium + Trial:** （**フリーミアム + トライアル:**）
- Free tier with limited features （機能が制限された無料枠）
- Trial of premium features （プレミアム機能のトライアル）
- Example: Zoom (free 40-min, trial of Pro) （例: Zoom (40 分間の無料トライアル、Pro のトライアル)）

**Reverse trial:** （**逆トライアル:**）
- Start with full access （フルアクセスで始める）
- After trial, downgrade to free tier （試用後、無料利用枠にダウングレード）
- Example: See premium value, live with limitations until ready （例: プレミアム価値を参照し、準備が整うまでは制限を設けてください）

---

## Enterprise Pricing （エンタープライズ価格）

### When to Add Custom Pricing （カスタム価格を追加する場合）

Add "Contact Sales" when: （次の場合に「営業担当者へのお問い合わせ」を追加します。）
- Deal sizes exceed $10k+ ARR （取引規模がARR10,000ドル以上を超える）
- Customers need custom contracts （顧客にはカスタム契約が必要です）
- Implementation/onboarding required （実装/オンボーディングが必要）
- Security/compliance requirements （セキュリティ/コンプライアンスの要件）
- Procurement processes involved （関連する調達プロセス）

### Enterprise Tier Elements （エンタープライズ層の要素）

**Table stakes:** （**テーブルステークス:**）
- SSO/SAML （SSO/SAML）
- Audit logs （監査ログ）
- Admin controls （管理者コントロール）
- Uptime SLA （稼働時間 SLA）
- Security certifications （セキュリティ認証）

**Value-adds:** （**付加価値:**）
- Dedicated support/success （献身的なサポート/成功）
- Custom onboarding （カスタムオンボーディング）
- Training sessions （トレーニングセッション）
- Custom integrations （カスタム統合）
- Priority roadmap input （優先ロードマップの入力）

### Enterprise Pricing Strategies （エンタープライズ価格戦略）

**Per-seat at scale:** （**座席ごとの規模:**）
- Volume discounts for large teams （大規模チーム向けのボリュームディスカウント）
- Example: $15/user (standard) → $10/user (100+) （例: $15/ユーザー (標準) → $10/ユーザー (100+)）

**Platform fee + usage:** （**プラットフォーム料金 + 使用量:**）
- Base fee for access （アクセス基本料金）
- Usage-based above thresholds （使用量ベースのしきい値超過）
- Example: $500/mo base + $0.01 per API call （例: 基本 $500/月 + API 呼び出しごとに $0.01）

**Value-based contracts:** （**価値ベースの契約:**）
- Price tied to customer's revenue/outcomes （価格は顧客の収益/成果に連動します）
- Example: % of transactions, revenue share （例: トランザクションの割合、収益分配率）
