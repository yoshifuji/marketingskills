# Sample Size Guide （サンプルサイズガイド）

Reference for calculating sample sizes and test duration. （サンプルサイズとテスト期間を計算するためのリファレンス。）

## Sample Size Fundamentals （サンプルサイズの基礎）

### Required Inputs （必須の入力）

1. **Baseline conversion rate**: Your current rate （**ベースライン コンバージョン率**: 現在のレート）
2. **Minimum detectable effect (MDE)**: Smallest change worth detecting （**最小検出可能効果 (MDE)**: 検出する価値のある最小の変化）
3. **Statistical significance level**: Usually 95% (α = 0.05) （**統計的有意水準**: 通常 95% (α = 0.05)）
4. **Statistical power**: Usually 80% (β = 0.20) （**統計検出力**: 通常 80% (β = 0.20)）

### What These Mean （これらの意味）

**Baseline conversion rate**: If your page converts at 5%, that's your baseline. （**ベースライン コンバージョン率**: ページのコンバージョン率が 5% であれば、それがベースラインです。）

**MDE (Minimum Detectable Effect)**: The smallest improvement you care about detecting. Set this based on: （**MDE (Minimum Detectable Effect)**: 検出したい最小の改善。以下に基づいてこれを設定します。）
- Business impact (is a 5% lift meaningful?) （ビジネスへの影響 (5% の引き上げは意味があるか?)）
- Implementation cost (worth the effort?) （導入コスト（労力に見合う価値があるか？））
- Realistic expectations (what have past tests shown?) （現実的な期待 (過去のテストで何が示されたか?)）

**Statistical significance (95%)**: Means there's less than 5% chance the observed difference is due to random chance. （**統計的有意性 (95%)**: 観察された差異がランダムな偶然によるものである可能性が 5% 未満であることを意味します。）

**Statistical power (80%)**: Means if there's a real effect of size MDE, you have 80% chance of detecting it. （**統計検出力 (80%)**: サイズ MDE の実際の影響がある場合、80% の確率でそれを検出できることを意味します。）

---

## Sample Size Quick Reference Tables （サンプルサイズの早見表）

### Conversion Rate: 1% （変換率: 1%）

| Lift to Detect（持ち上げて検出する） | Sample per Variant（バリエーションごとのサンプル） | Total Sample（合計サンプル） |
|----------------|-------------------|--------------|
| 5% (1% → 1.05%) | 1,500,000 | 3,000,000 |
| 10% (1% → 1.1%) | 380,000 | 760,000 |
| 20% (1% → 1.2%) | 97,000 | 194,000 |
| 50% (1% → 1.5%) | 16,000 | 32,000 |
| 100% (1% → 2%) | 4,200 | 8,400 |

### Conversion Rate: 3% （コンバージョン率: 3%）

| Lift to Detect（持ち上げて検出する） | Sample per Variant（バリエーションごとのサンプル） | Total Sample（合計サンプル） |
|----------------|-------------------|--------------|
| 5% (3% → 3.15%) | 480,000 | 960,000 |
| 10% (3% → 3.3%) | 120,000 | 240,000 |
| 20% (3% → 3.6%) | 31,000 | 62,000 |
| 50% (3% → 4.5%) | 5,200 | 10,400 |
| 100% (3% → 6%) | 1,400 | 2,800 |

### Conversion Rate: 5% （変換率: 5%）

| Lift to Detect（持ち上げて検出する） | Sample per Variant（バリエーションごとのサンプル） | Total Sample（合計サンプル） |
|----------------|-------------------|--------------|
| 5% (5% → 5.25%) | 280,000 | 560,000 |
| 10% (5% → 5.5%) | 72,000 | 144,000 |
| 20% (5% → 6%) | 18,000 | 36,000 |
| 50% (5% → 7.5%) | 3,100 | 6,200 |
| 100% (5% → 10%) | 810 | 1,620 |

### Conversion Rate: 10% （変換率: 10%）

| Lift to Detect（持ち上げて検出する） | Sample per Variant（バリエーションごとのサンプル） | Total Sample（合計サンプル） |
|----------------|-------------------|--------------|
| 5% (10% → 10.5%) | 130,000 | 260,000 |
| 10% (10% → 11%) | 34,000 | 68,000 |
| 20% (10% → 12%) | 8,700 | 17,400 |
| 50% (10% → 15%) | 1,500 | 3,000 |
| 100% (10% → 20%) | 400 | 800 |

### Conversion Rate: 20% （コンバージョン率: 20%）

| Lift to Detect（持ち上げて検出する） | Sample per Variant（バリエーションごとのサンプル） | Total Sample（合計サンプル） |
|----------------|-------------------|--------------|
| 5% (20% → 21%) | 60,000 | 120,000 |
| 10% (20% → 22%) | 16,000 | 32,000 |
| 20% (20% → 24%) | 4,000 | 8,000 |
| 50% (20% → 30%) | 700 | 1,400 |
| 100% (20% → 40%) | 200 | 400 |

---

## Duration Calculator （期間計算ツール）

### Formula （式）

```
Duration (days) = (Sample per variant × Number of variants) / (Daily traffic × % exposed)
```

### Examples （例）

**Scenario 1: High-traffic page** （**シナリオ 1: トラフィックの多いページ**）
- Need: 10,000 per variant (2 variants = 20,000 total) （必要量: バリエーションごとに 10,000 (2 バリエーション = 合計 20,000)）
- Daily traffic: 5,000 visitors （毎日の訪問者数: 5,000 人）
- 100% exposed to test （100% テストにさらされる）
- Duration: 20,000 / 5,000 = **4 days** （期間: 20,000 / 5,000 = **4 日**）

**Scenario 2: Medium-traffic page** （**シナリオ 2: 中程度のトラフィックのページ**）
- Need: 30,000 per variant (60,000 total) （必要量: バリエーションごとに 30,000 (合計 60,000)）
- Daily traffic: 2,000 visitors （毎日の訪問者数: 2,000 人）
- 100% exposed （100%露出）
- Duration: 60,000 / 2,000 = **30 days** （期間: 60,000 / 2,000 = **30 日**）

**Scenario 3: Low-traffic with partial exposure** （**シナリオ 3: トラフィックが少なく、部分的に露出している**）
- Need: 15,000 per variant (30,000 total) （必要量: バリエーションごとに 15,000 (合計 30,000)）
- Daily traffic: 500 visitors （毎日のトラフィック: 500 人の訪問者）
- 50% exposed to test （50% がテストにさらされる）
- Effective daily: 250 （毎日有効: 250）
- Duration: 30,000 / 250 = **120 days** (too long!) （期間: 30,000 / 250 = **120 日** (長すぎます!)）

### Minimum Duration Rules （最小期間ルール）

Even with sufficient sample size, run tests for at least: （十分なサンプル サイズがある場合でも、少なくとも次のテストを実行します。）
- **1 full week**: To capture day-of-week variation （**丸 1 週間**: 曜日の変動を把握するため）
- **2 business cycles**: If B2B (weekday vs. weekend patterns) （**2 つのビジネス サイクル**: B2B の場合 (平日と週末のパターン)）
- **Through paydays**: If e-commerce (beginning/end of month) （**給料日を通して**: 電子商取引の場合 (月初め/月末)）

### Maximum Duration Guidelines （最大継続時間のガイドライン）

Avoid running tests longer than 4-8 weeks: （4 ～ 8 週間を超えるテストの実行は避けてください。）
- Novelty effects wear off （ノベルティ効果が薄れる）
- External factors intervene （外部要因が介入する）
- Opportunity cost of other tests （他のテストの機会費用）

---

## Online Calculators （オンライン計算機）

### Recommended Tools （推奨ツール）

**Evan Miller's Calculator** （**エヴァン・ミラーの電卓**）
https://www.evanmiller.org/ab-testing/sample-size.html （https://www.evanmiller.org/ab-testing/sample-size.html）
- Simple interface （シンプルなインターフェース）
- Bookmark-worthy （ブックマークに値する）

**Optimizely's Calculator** （**Optimizely の計算機**）
https://www.optimizely.com/sample-size-calculator/ （https://www.optimizely.com/sample-size-calculator/）
- Business-friendly language （ビジネスに適した言語）
- Duration estimates （期間の見積もり）

**AB Test Guide Calculator** （**AB テスト ガイド カリキュレーター**）
https://www.abtestguide.com/calc/ （https://www.abtestguide.com/calc/）
- Includes Bayesian option （ベイジアンオプションを含む）
- Multiple test types （複数のテストタイプ）

**VWO Duration Calculator** （**VWO期間計算ツール**）
https://vwo.com/tools/ab-test-duration-calculator/ （https://vwo.com/tools/ab-test-duration-calculator/）
- Duration-focused （持続時間重視）
- Good for planning （計画を立てるのに良い）

---

## Adjusting for Multiple Variants （複数のバリアントの調整）

With more than 2 variants (A/B/n tests), you need more sample: （2 つ以上のバリアント (A/B/n テスト) がある場合は、より多くのサンプルが必要になります。）

| Variants（バリエーション） | Multiplier（乗数） |
|----------|------------|
| 2 (A/B)（2 (A/B)） | 1x（1x） |
| 3 (A/B/C)（3 (A/B/C)） | ~1.5x（～1.5倍） |
| 4 (A/B/C/D)（4 (A/B/C/D)） | ~2x（～2倍） |
| 5+ | Consider reducing variants（バリアントの削減を検討する） |

**Why?** More comparisons increase chance of false positives. You're comparing: （**なぜですか?** 比較が増えると、誤検知の可能性が高くなります。比較しているのは:）
- A vs B （A vs B）
- A vs C （A vs C）
- B vs C (sometimes) （B 対 C (場合によっては)）

Apply Bonferroni correction or use tools that handle this automatically. （ボンフェローニ補正を適用するか、これを自動的に処理するツールを使用します。）

---

## Common Sample Size Mistakes （よくあるサンプルサイズの間違い）

### 1. Underpowered tests （1. 能力不足のテスト）
**Problem**: Not enough sample to detect realistic effects （**問題**: 現実的な効果を検出するのに十分なサンプルがありません）
**Fix**: Be realistic about MDE, get more traffic, or don't test （**修正**: MDE について現実的になるか、より多くのトラフィックを取得するか、テストしないでください。）

### 2. Overpowered tests （2. 過剰なテスト）
**Problem**: Waiting for sample size when you already have significance （**問題**: すでに有意性がある場合にサンプルサイズを待機している）
**Fix**: This is actually fine—you committed to sample size, honor it （**修正**: これは実際には問題ありません。サンプル サイズを約束しましたので、それを尊重してください。）

### 3. Wrong baseline rate （3. 間違ったベースラインレート）
**Problem**: Using wrong conversion rate for calculation （**問題**: 計算に間違った変換レートを使用した）
**Fix**: Use the specific metric and page, not site-wide averages （**修正**: サイト全体の平均ではなく、特定の指標とページを使用してください）

### 4. Ignoring segments （4. セグメントの無視）
**Problem**: Calculating for full traffic, then analyzing segments （**問題**: フルトラフィックを計算してからセグメントを分析する）
**Fix**: If you plan segment analysis, calculate sample for smallest segment （**修正**: セグメント分析を計画する場合は、最小セグメントのサンプルを計算してください）

### 5. Testing too many things （5. あまりにも多くのことをテストしすぎる）
**Problem**: Dividing traffic too many ways （**問題**: トラフィックの分割方法が多すぎる）
**Fix**: Prioritize ruthlessly, run fewer concurrent tests （**修正**: 容赦なく優先順位を付け、同時実行テストの数を減らします。）

---

## When Sample Size Requirements Are Too High （サンプルサイズの要件が高すぎる場合）

Options when you can't get enough traffic: （十分なトラフィックを獲得できない場合のオプション:）

1. **Increase MDE**: Accept only detecting larger effects (20%+ lift) （**MDE を増加**: より大きな効果 (20% 以上のリフト) の検出のみを受け入れます。）
2. **Lower confidence**: Use 90% instead of 95% (risky, document it) （**信頼性が低い**: 95% ではなく 90% を使用します (危険です、文書化してください)）
3. **Reduce variants**: Test only the most promising variant （**バリアントを減らす**: 最も有望なバリアントのみをテストします）
4. **Combine traffic**: Test across multiple similar pages （**トラフィックを結合**: 複数の類似したページにわたってテストします。）
5. **Test upstream**: Test earlier in funnel where traffic is higher （**アップストリームのテスト**: トラフィックが多いファネルの早い段階でテストします。）
6. **Don't test**: Make decision based on qualitative data instead （**テストしない**: 代わりに定性データに基づいて意思決定を行います）
7. **Longer test**: Accept longer duration (weeks/months) （**より長いテスト**: より長い期間 (週/月) を受け入れます。）

---

## Sequential Testing （逐次テスト）

If you must check results before reaching sample size: （サンプルサイズに達する前に結果を確認する必要がある場合:）

### What is it? （それは何ですか？）
Statistical method that adjusts for multiple looks at data. （データを複数回見て調整する統計手法。）

### When to use （いつ使用するか）
- High-risk changes （リスクの高い変更）
- Need to stop bad variants early （悪質な亜種を早期に阻止する必要がある）
- Time-sensitive decisions （一刻を争う決断）

### Tools that support it （それをサポートするツール）
- Optimizely (Stats Accelerator) （Optimizely (統計アクセラレータ)）
- VWO (SmartStats) （VWO (スマート統計)）
- PostHog (Bayesian approach) （PostHog (ベイジアンアプローチ)）

### Tradeoff （トレード・オフ）
- More flexibility to stop early （より柔軟に早期停止が可能）
- Slightly larger sample size requirement （わずかに大きいサンプルサイズの要件）
- More complex analysis （より複雑な分析）

---

## Quick Decision Framework （迅速な意思決定のフレームワーク）

### Can I run this test? （このテストを実行できますか?）

```
Daily traffic to page: _____
Baseline conversion rate: _____
MDE I care about: _____

Sample needed per variant: _____ (from tables above)
Days to run: Sample / Daily traffic = _____

If days > 60: Consider alternatives
If days > 30: Acceptable for high-impact tests
If days < 14: Likely feasible
If days < 7: Easy to run, consider running longer anyway
```
