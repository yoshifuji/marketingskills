# Pricing Research Methods （日本語訳：価格調査方法）

## Van Westendorp Price Sensitivity Meter （日本語訳：Van Westendorp 価格感度メーター）

The Van Westendorp survey identifies the acceptable price range for your product. （日本語訳：Van Westendorp の調査により、製品の許容可能な価格範囲が特定されます。）

### The Four Questions （日本語訳：4つの質問）

Ask each respondent: （日本語訳：各回答者に次のように尋ねます。）
1. "At what price would you consider [product] to be so expensive that you would not consider buying it?" (Too expensive) （日本語訳：「[製品] が高すぎて購入を検討できないと思いますか?」 (高すぎる)）
2. "At what price would you consider [product] to be priced so low that you would question its quality?" (Too cheap) （日本語訳：「[製品] の価格が、その品質を疑問視するほど低すぎると思いますか?」 (安すぎる)）
3. "At what price would you consider [product] to be starting to get expensive, but you still might consider it?" (Expensive/high side) （日本語訳：「[製品] が高価になり始めていますが、それでも検討できる価格はいくらだと思いますか?」 （高価・ハイサイド））
4. "At what price would you consider [product] to be a bargain—a great buy for the money?" (Cheap/good value) （日本語訳：「[製品] はどのくらいの価格であればお買い得だと思いますか?」 (安い・お値打ち)）

### How to Analyze （日本語訳：分析方法）

1. Plot cumulative distributions for each question （日本語訳：各質問の累積分布をプロットする）
2. Find the intersections: （日本語訳：交点を見つけます。）
   - **Point of Marginal Cheapness (PMC):** "Too cheap" crosses "Expensive" （日本語訳：**限界安ポイント (PMC):** 「安すぎる」が「高価」を超える）
   - **Point of Marginal Expensiveness (PME):** "Too expensive" crosses "Cheap" （日本語訳：**限界費用点 (PME):** 「高すぎる」が「安い」を超える）
   - **Optimal Price Point (OPP):** "Too cheap" crosses "Too expensive" （日本語訳：**最適価格帯 (OPP):** 「安すぎる」は「高すぎる」を超える）
   - **Indifference Price Point (IDP):** "Expensive" crosses "Cheap" （日本語訳：**無関心価格点 (IDP):** 「高い」と「安い」が交差します）

**The acceptable price range:** PMC to PME （日本語訳：**許容可能な価格範囲:** PMC から PME）
**Optimal pricing zone:** Between OPP and IDP （日本語訳：**最適な価格設定ゾーン:** OPP と IDP の間）

### Survey Tips （日本語訳：調査のヒント）
- Need 100-300 respondents for reliable data （日本語訳：信頼できるデータを得るには 100 ～ 300 人の回答者が必要）
- Segment by persona (different willingness to pay) （日本語訳：ペルソナごとにセグメント化する（支払い意思の違い））
- Use realistic product descriptions （日本語訳：現実的な商品説明を使用する）
- Consider adding purchase intent questions （日本語訳：購入意向に関する質問の追加を検討してください）

### Sample Output （日本語訳：サンプル出力）

```
Price Sensitivity Analysis Results:
─────────────────────────────────
Point of Marginal Cheapness:  $29/mo
Optimal Price Point:          $49/mo
Indifference Price Point:     $59/mo
Point of Marginal Expensiveness: $79/mo

Recommended range: $49-59/mo
Current price: $39/mo (below optimal)
Opportunity: 25-50% price increase without significant demand impact
```

---

## MaxDiff Analysis (Best-Worst Scaling) （日本語訳：MaxDiff 分析 (最良-最悪のスケーリング)）

MaxDiff identifies which features customers value most, informing packaging decisions. （日本語訳：MaxDiff は、顧客がどの機能を最も重視しているかを特定し、パッケージングの決定に役立ちます。）

### How It Works （日本語訳：仕組み）

1. List 8-15 features you could include （日本語訳：含めることができる機能を 8 ～ 15 個挙げてください）
2. Show respondents sets of 4-5 features at a time （日本語訳：回答者に一度に 4 ～ 5 つの特徴のセットを表示する）
3. Ask: "Which is MOST important? Which is LEAST important?" （日本語訳：「どれが最も重要ですか? どれが最も重要ではありませんか?」と尋ねます。）
4. Repeat across multiple sets until all features compared （日本語訳：すべての特徴が比較されるまで、複数のセットにわたって繰り返します）
5. Statistical analysis produces importance scores （日本語訳：統計分析により重要度スコアが生成されます）

### Example Survey Question （日本語訳：アンケートの質問例）

```
Which feature is MOST important to you?
Which feature is LEAST important to you?

□ Unlimited projects
□ Custom branding
□ Priority support
□ API access
□ Advanced analytics
```

### Analyzing Results （日本語訳：結果の分析）

Features are ranked by utility score: （日本語訳：機能はユーティリティ スコアによってランク付けされます。）
- High utility = Must-have (include in base tier) （日本語訳：高い実用性 = 必須 (基本層に含まれる)）
- Medium utility = Differentiator (use for tier separation) （日本語訳：中程度のユーティリティ = 差別化要因 (層の分離に使用)）
- Low utility = Nice-to-have (premium tier or cut) （日本語訳：実用性が低い = あれば便利 (プレミアム層またはカット)）

### Using MaxDiff for Packaging （日本語訳：パッケージ化に MaxDiff を使用する）

| Utility Score（日本語訳：ユーティリティスコア） | Packaging Decision（日本語訳：包装の決定） |
|---------------|-------------------|
| Top 20%（日本語訳：上位 20%） | Include in all tiers (table stakes)（日本語訳：すべてのティアに含める (テーブル ステークス)） |
| 20-50% | Use to differentiate tiers（日本語訳：階層を区別するために使用します） |
| 50-80% | Higher tiers only（日本語訳：上位層のみ） |
| Bottom 20%（日本語訳：下位 20%） | Consider cutting or premium add-on（日本語訳：カットまたはプレミアムアドオンを検討してください） |

---

## Willingness to Pay Surveys （日本語訳：調査への支払い意思）

**Direct method (simple but biased):** （日本語訳：**直接的な方法 (シンプルですが偏りがあります):**）
"How much would you pay for [product]?" （日本語訳：「[製品]にいくら支払いますか?」）

**Better: Gabor-Granger method:** （日本語訳：**より良い: ガボール・グレンジャー法:**）
"Would you buy [product] at [$X]?" (Yes/No) （日本語訳：「[製品]を[$X]で購入してくれませんか?」 (はい/いいえ)）
Vary price across respondents to build demand curve. （日本語訳：回答者間で価格を変化させて需要曲線を作成します。）

**Even better: Conjoint analysis:** （日本語訳：**さらに良い点: コンジョイント分析:**）
Show product bundles at different prices （日本語訳：さまざまな価格の製品バンドルを表示する）
Respondents choose preferred option （日本語訳：回答者は希望するオプションを選択します）
Statistical analysis reveals price sensitivity per feature （日本語訳：統計分析により、機能ごとの価格感度が明らかになります）

---

## Usage-Value Correlation Analysis （日本語訳：使用量と価値の相関分析）

### 1. Instrument usage data （日本語訳：1. 機器の使用状況データ）
Track how customers use your product: （日本語訳：顧客が製品をどのように使用しているかを追跡します。）
- Feature usage frequency （日本語訳：機能の使用頻度）
- Volume metrics (users, records, API calls) （日本語訳：ボリュームメトリクス (ユーザー、レコード、API 呼び出し)）
- Outcome metrics (revenue generated, time saved) （日本語訳：成果指標 (収益の発生、時間の節約)）

### 2. Correlate with customer success （日本語訳：2. 顧客の成功と相関付ける）
- Which usage patterns predict retention? （日本語訳：どの使用パターンがリテンションを予測しますか?）
- Which usage patterns predict expansion? （日本語訳：拡大を予測する使用パターンはどれですか?）
- Which customers pay the most, and why? （日本語訳：どの顧客が最も多くお金を払っていますか?またその理由は何ですか?）

### 3. Identify value thresholds （日本語訳：3. 値のしきい値を特定する）
- At what usage level do customers "get it"? （日本語訳：顧客はどのような使用レベルで「理解」しますか?）
- At what usage level do they expand? （日本語訳：どのような使用レベルで拡張されますか?）
- At what usage level should price increase? （日本語訳：どの使用レベルで価格を上げる必要がありますか?）

### Example Analysis （日本語訳：分析例）

```
Usage-Value Correlation Analysis:
─────────────────────────────────
Segment: High-LTV customers (>$10k ARR)
Average monthly active users: 15
Average projects: 8
Average integrations: 4

Segment: Churned customers
Average monthly active users: 3
Average projects: 2
Average integrations: 0

Insight: Value correlates with team adoption (users)
        and depth of use (integrations)

Recommendation: Price per user, gate integrations to higher tiers
```
