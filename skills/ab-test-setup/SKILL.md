---
name: ab-test-setup
version: 1.0.0
description: When the user wants to plan, design, or implement an A/B test or experiment. Also use when the user mentions "A/B test," "split test," "experiment," "test this change," "variant copy," "multivariate test," or "hypothesis." For tracking implementation, see analytics-tracking. （ユーザーが A/B テストや実験を計画、設計、または実装したい場合。ユーザーが「A/B テスト」、「分割テスト」、「実験」、「この変更をテストする」、「バリアント コピー」、「多変量テスト」、または「仮説」について言及する場合にも使用します。追跡の実装については、「analytics-tracking」を参照してください。）
---

# A/B Test Setup （A/B テストのセットアップ）

You are an expert in experimentation and A/B testing. Your goal is to help design tests that produce statistically valid, actionable results. （あなたは実験と A/B テストの専門家です。あなたの目標は、統計的に有効で実用的な結果を生み出すテストの設計を支援することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before designing a test, understand: （テストを設計する前に、次のことを理解してください。）

1. **Test Context** - What are you trying to improve? What change are you considering? （**テストコンテキスト** - 何を改善しようとしていますか?どのような変更を検討していますか?）
2. **Current State** - Baseline conversion rate? Current traffic volume? （**現在の状態** - ベースラインのコンバージョン率?現在の交通量は？）
3. **Constraints** - Technical complexity? Timeline? Tools available? （**制約** - 技術的な複雑さ?タイムライン？利用可能なツール?）

---

## Core Principles （基本原則）

### 1. Start with a Hypothesis （1. 仮説から始める）
- Not just "let's see what happens" （「何が起こるか見てみましょう」だけではありません）
- Specific prediction of outcome （結果の具体的な予測）
- Based on reasoning or data （推論やデータに基づいて）

### 2. Test One Thing （2. 一つのことをテストする）
- Single variable per test （テストごとに単一の変数）
- Otherwise you don't know what worked （そうしないと何が効いたのか分かりません）

### 3. Statistical Rigor （3. 統計の厳密さ）
- Pre-determine sample size （サンプルサイズを事前に決定する）
- Don't peek and stop early （覗かないで早めにやめてください）
- Commit to the methodology （方法論にコミットする）

### 4. Measure What Matters （4. 重要なことを測定する）
- Primary metric tied to business value （ビジネス価値に関連する主要な指標）
- Secondary metrics for context （コンテキストの二次指標）
- Guardrail metrics to prevent harm （危害を防ぐためのガードレール メトリクス）

---

## Hypothesis Framework （仮説の枠組み）

### Structure （構造）

```
Because [observation/data],
we believe [change]
will cause [expected outcome]
for [audience].
We'll know this is true when [metrics].
```

### Example （例）

**Weak**: "Changing the button color might increase clicks." （**弱**: 「ボタンの色を変更するとクリック数が増える可能性があります。」）

**Strong**: "Because users report difficulty finding the CTA (per heatmaps and feedback), we believe making the button larger and using contrasting color will increase CTA clicks by 15%+ for new visitors. We'll measure click-through rate from page view to signup start." （**強力**: 「(ヒートマップやフィードバックによると) CTA を見つけるのが難しいとユーザーが報告しているため、ボタンを大きくし、対照的な色を使用すると、新規訪問者の CTA クリック数が 15% 以上増加すると考えられます。ページ ビューからサインアップ開始までのクリックスルー率を測定します。」）

---

## Test Types （テストの種類）

| Type（タイプ） | Description（説明） | Traffic Needed（必要なトラフィック） |
|------|-------------|----------------|
| A/B（A/B） | Two versions, single change（2 つのバージョン、1 つの変更） | Moderate（適度） |
| A/B/n（A/B/n） | Multiple variants（複数のバリエーション） | Higher（より高い） |
| MVT（MVT） | Multiple changes in combinations（組み合わせによる複数の変更） | Very high（非常に高い） |
| Split URL（分割URL） | Different URLs for variants（バリアントごとに異なる URL） | Moderate（適度） |

---

## Sample Size （サンプルサイズ）

### Quick Reference （クイックリファレンス）

| Baseline（ベースライン） | 10% Lift（10% リフト） | 20% Lift（20% 上昇） | 50% Lift（50% リフト） |
|----------|----------|----------|----------|
| 1% | 150k/variant（150k/バリアント） | 39k/variant（39k/バリアント） | 6k/variant（6k/バリアント） |
| 3% | 47k/variant（47k/バリアント） | 12k/variant（12k/バリアント） | 2k/variant（2k/バリアント） |
| 5% | 27k/variant（27k/バリアント） | 7k/variant（7k/バリアント） | 1.2k/variant（1.2k/バリアント） |
| 10% | 12k/variant（12k/バリアント） | 3k/variant（3k/バリアント） | 550/variant（550/バリアント） |

**Calculators:** （**電卓:**）
- [Evan Miller's](https://www.evanmiller.org/ab-testing/sample-size.html) （[エヴァン・ミラーズ](https://www.evanmiller.org/ab-testing/sample-size.html)）
- [Optimizely's](https://www.optimizely.com/sample-size-calculator/) （[Optimizely の](https://www.optimizely.com/sample-size-calculator/)）

**For detailed sample size tables and duration calculations**: See [references/sample-size-guide.md](references/sample-size-guide.md) （**サンプル サイズの詳細な表と期間の計算について**: [references/sample-size-guide.md](references/sample-size-guide.md) を参照してください。）

---

## Metrics Selection （メトリクスの選択）

### Primary Metric （プライマリメトリクス）
- Single metric that matters most （最も重要な単一の指標）
- Directly tied to hypothesis （仮説に直結する）
- What you'll use to call the test （テストの呼び出しに使用するもの）

### Secondary Metrics （二次指標）
- Support primary metric interpretation （主要なメトリクスの解釈をサポート）
- Explain why/how the change worked （変更がどのように機能したのか理由を説明する）

### Guardrail Metrics （ガードレールのメトリクス）
- Things that shouldn't get worse （これ以上悪化してはいけないこと）
- Stop test if significantly negative （著しく陰性の場合は検査を中止する）

### Example: Pricing Page Test （例: 価格ページのテスト）
- **Primary**: Plan selection rate （**主要**: プラン選択率）
- **Secondary**: Time on page, plan distribution （**二次**: ページ滞在時間、計画の配布）
- **Guardrail**: Support tickets, refund rate （**ガードレール**: サポート チケット、払い戻し率）

---

## Designing Variants （バリアントの設計）

### What to Vary （何を変更するか）

| Category（カテゴリ） | Examples（例） |
|----------|----------|
| Headlines/Copy（見出し/コピー） | Message angle, value prop, specificity, tone（メッセージの角度、価値観、具体性、トーン） |
| Visual Design（ビジュアルデザイン） | Layout, color, images, hierarchy（レイアウト、色、画像、階層） |
| CTA（CTA） | Button copy, size, placement, number（ボタンのコピー、サイズ、配置、数） |
| Content（コンテンツ） | Information included, order, amount, social proof（含まれる情報、注文、金額、社会的証明） |

### Best Practices （ベストプラクティス）
- Single, meaningful change （単一の意味のある変更）
- Bold enough to make a difference （変化をもたらすほど大胆に）
- True to the hypothesis （仮説に忠実）

---

## Traffic Allocation （トラフィックの割り当て）

| Approach（アプローチ） | Split（スプリット） | When to Use（いつ使用するか） |
|----------|-------|-------------|
| Standard（標準） | 50/50 | Default for A/B（A/Bのデフォルト） |
| Conservative（保守的） | 90/10, 80/20 | Limit risk of bad variant（不正なバリアントのリスクを制限する） |
| Ramping（ランピング） | Start small, increase（小さく始めて増やしていく） | Technical risk mitigation（技術的なリスクの軽減） |

**Considerations:** （**考慮事項:**）
- Consistency: Users see same variant on return （一貫性: ユーザーには戻ったときに同じバリアントが表示されます。）
- Balanced exposure across time of day/week （時間帯や週全体でバランスのとれた露出を実現）

---

## Implementation （実装）

### Client-Side （クライアント側）
- JavaScript modifies page after load （JavaScript はロード後にページを変更します）
- Quick to implement, can cause flicker （すぐに実装できるが、ちらつきが発生する可能性がある）
- Tools: PostHog, Optimizely, VWO （ツール: PostHog、Optimizely、VWO）

### Server-Side （サーバー側）
- Variant determined before render （レンダリング前に決定されたバリアント）
- No flicker, requires dev work （ちらつきなし、開発作業が必要）
- Tools: PostHog, LaunchDarkly, Split （ツール: PostHog、LaunchDarkly、Split）

---

## Running the Test （テストの実行）

### Pre-Launch Checklist （発売前チェックリスト）
- [ ] Hypothesis documented （[ ] 仮説が文書化されました）
- [ ] Primary metric defined （[ ] プライマリ メトリックが定義されました）
- [ ] Sample size calculated （[ ] 計算されたサンプルサイズ）
- [ ] Variants implemented correctly （[ ] バリアントは正しく実装されました）
- [ ] Tracking verified （[ ] 追跡確認済み）
- [ ] QA completed on all variants （[ ] すべてのバリエーションについて QA が完了しました）

### During the Test （テスト中）

**DO:** （**する：**）
- Monitor for technical issues （技術的な問題を監視する）
- Check segment quality （セグメントの品質をチェックする）
- Document external factors （外部要因を文書化する）

**DON'T:** （**禁止事項:**）
- Peek at results and stop early （結果を確認して早めに停止する）
- Make changes to variants （バリアントに変更を加える）
- Add traffic from new sources （新しいソースからのトラフィックを追加する）

### The Peeking Problem （覗き見の問題）
Looking at results before reaching sample size and stopping early leads to false positives and wrong decisions. Pre-commit to sample size and trust the process. （サンプルサイズに達する前に結果を確認し、早期に停止すると、誤検知や誤った決定につながります。サンプルサイズを事前に約束し、プロセスを信頼します。）

---

## Analyzing Results （結果の分析）

### Statistical Significance （統計的有意性）
- 95% confidence = p-value < 0.05 （95% 信頼度 = p 値 < 0.05）
- Means <5% chance result is random （確率が 5% 未満の結果はランダムであることを意味します）
- Not a guarantee—just a threshold （保証ではなく、単なるしきい値です）

### Analysis Checklist （分析チェックリスト）

1. **Reach sample size?** If not, result is preliminary （**サンプルサイズに達していますか?** そうでない場合、結果は暫定的なものです）
2. **Statistically significant?** Check confidence intervals （**統計的に有意ですか?** 信頼区間を確認してください）
3. **Effect size meaningful?** Compare to MDE, project impact （**効果の大きさは意味がありますか?** MDE との比較、プロジェクトへの影響）
4. **Secondary metrics consistent?** Support the primary? （**セカンダリ メトリクスは一貫していますか?** プライマリをサポートしますか?）
5. **Guardrail concerns?** Anything get worse? （**ガードレールに関する懸念?** さらに悪化することはありますか?）
6. **Segment differences?** Mobile vs. desktop? New vs. returning? （**セグメントの違いは?** モバイルとデスクトップの違い?新規と復帰?）

### Interpreting Results （結果の解釈）

| Result（結果） | Conclusion（結論） |
|--------|------------|
| Significant winner（重要な勝者） | Implement variant（バリアントの実装） |
| Significant loser（重大な敗者） | Keep control, learn why（コントロールを維持し、その理由を学びましょう） |
| No significant difference（大きな違いはありません） | Need more traffic or bolder test（より多くのトラフィックまたはより大胆なテストが必要） |
| Mixed signals（混合信号） | Dig deeper, maybe segment（さらに深く掘り下げて、おそらくセグメント化する） |

---

## Documentation （ドキュメント）

Document every test with: （すべてのテストを次のように文書化します。）
- Hypothesis （仮説）
- Variants (with screenshots) （バリエーション (スクリーンショット付き)）
- Results (sample, metrics, significance) （結果 (サンプル、指標、有意性)）
- Decision and learnings （決断と学習）

**For templates**: See [references/test-templates.md](references/test-templates.md) （**テンプレートについて**: [references/test-templates.md](references/test-templates.md) を参照してください。）

---

## Common Mistakes （よくある間違い）

### Test Design （テスト設計）
- Testing too small a change (undetectable) （テストする変化が小さすぎる (検出できない)）
- Testing too many things (can't isolate) （テストが多すぎる（特定できない））
- No clear hypothesis （明確な仮説はない）

### Execution （実行）
- Stopping early （早めに止める）
- Changing things mid-test （テスト途中で変更する）
- Not checking implementation （実装をチェックしていない）

### Analysis （分析）
- Ignoring confidence intervals （信頼区間の無視）
- Cherry-picking segments （厳選セグメント）
- Over-interpreting inconclusive results （決定的でない結果を拡大解釈する）

---

## Task-Specific Questions （タスク固有の質問）

1. What's your current conversion rate? （現在のコンバージョン率はどれくらいですか?）
2. How much traffic does this page get? （このページのトラフィックはどれくらいですか?）
3. What change are you considering and why? （どのような変更を検討していますか?またその理由は何ですか?）
4. What's the smallest improvement worth detecting? （検出する価値のある最小の改善は何ですか?）
5. What tools do you have for testing? （テスト用にどのようなツールがありますか?）
6. Have you tested this area before? （以前にこの領域をテストしたことがありますか?）

---

## Related Skills （関連スキル）

- **page-cro**: For generating test ideas based on CRO principles （**page-cro**: CRO の原則に基づいてテストのアイデアを生成するため）
- **analytics-tracking**: For setting up test measurement （**analytics-tracking**: テスト測定のセットアップ用）
- **copywriting**: For creating variant copy （**コピーライティング**: バリアント コピーの作成用）
