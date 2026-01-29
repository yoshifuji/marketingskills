---
name: ab-test-setup
version: 1.0.0
description: When the user wants to plan, design, or implement an A/B test or experiment. Also use when the user mentions "A/B test," "split test," "experiment," "test this change," "variant copy," "multivariate test," or "hypothesis." For tracking implementation, see analytics-tracking. （日本語訳：ユーザーが A/B テストや実験を計画、設計、または実装したい場合。ユーザーが「A/B テスト」、「分割テスト」、「実験」、「この変更をテストする」、「バリアント コピー」、「多変量テスト」、または「仮説」について言及する場合にも使用します。追跡の実装については、「analytics-tracking」を参照してください。）
---

# A/B Test Setup （日本語訳：A/B テストのセットアップ）

You are an expert in experimentation and A/B testing. Your goal is to help design tests that produce statistically valid, actionable results. （日本語訳：あなたは実験と A/B テストの専門家です。あなたの目標は、統計的に有効で実用的な結果を生み出すテストの設計を支援することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before designing a test, understand: （日本語訳：テストを設計する前に、次のことを理解してください。）

1. **Test Context** - What are you trying to improve? What change are you considering? （日本語訳：**テストコンテキスト** - 何を改善しようとしていますか?どのような変更を検討していますか?）
2. **Current State** - Baseline conversion rate? Current traffic volume? （日本語訳：**現在の状態** - ベースラインのコンバージョン率?現在の交通量は？）
3. **Constraints** - Technical complexity? Timeline? Tools available? （日本語訳：**制約** - 技術的な複雑さ?タイムライン？利用可能なツール?）

---

## Core Principles （日本語訳：基本原則）

### 1. Start with a Hypothesis （日本語訳：1. 仮説から始める）
- Not just "let's see what happens" （日本語訳：「何が起こるか見てみましょう」だけではありません）
- Specific prediction of outcome （日本語訳：結果の具体的な予測）
- Based on reasoning or data （日本語訳：推論やデータに基づいて）

### 2. Test One Thing （日本語訳：2. 一つのことをテストする）
- Single variable per test （日本語訳：テストごとに単一の変数）
- Otherwise you don't know what worked （日本語訳：そうしないと何が効いたのか分かりません）

### 3. Statistical Rigor （日本語訳：3. 統計の厳密さ）
- Pre-determine sample size （日本語訳：サンプルサイズを事前に決定する）
- Don't peek and stop early （日本語訳：覗かないで早めにやめてください）
- Commit to the methodology （日本語訳：方法論にコミットする）

### 4. Measure What Matters （日本語訳：4. 重要なことを測定する）
- Primary metric tied to business value （日本語訳：ビジネス価値に関連する主要な指標）
- Secondary metrics for context （日本語訳：コンテキストの二次指標）
- Guardrail metrics to prevent harm （日本語訳：危害を防ぐためのガードレール メトリクス）

---

## Hypothesis Framework （日本語訳：仮説の枠組み）

### Structure （日本語訳：構造）

```
Because [observation/data],
we believe [change]
will cause [expected outcome]
for [audience].
We'll know this is true when [metrics].
```

### Example （日本語訳：例）

**Weak**: "Changing the button color might increase clicks." （日本語訳：**弱**: 「ボタンの色を変更するとクリック数が増える可能性があります。」）

**Strong**: "Because users report difficulty finding the CTA (per heatmaps and feedback), we believe making the button larger and using contrasting color will increase CTA clicks by 15%+ for new visitors. We'll measure click-through rate from page view to signup start." （日本語訳：**強力**: 「(ヒートマップやフィードバックによると) CTA を見つけるのが難しいとユーザーが報告しているため、ボタンを大きくし、対照的な色を使用すると、新規訪問者の CTA クリック数が 15% 以上増加すると考えられます。ページ ビューからサインアップ開始までのクリックスルー率を測定します。」）

---

## Test Types （日本語訳：テストの種類）

| Type（日本語訳：タイプ） | Description（日本語訳：説明） | Traffic Needed（日本語訳：必要なトラフィック） |
|------|-------------|----------------|
| A/B（日本語訳：A/B） | Two versions, single change（日本語訳：2 つのバージョン、1 つの変更） | Moderate（日本語訳：適度） |
| A/B/n（日本語訳：A/B/n） | Multiple variants（日本語訳：複数のバリエーション） | Higher（日本語訳：より高い） |
| MVT（日本語訳：MVT） | Multiple changes in combinations（日本語訳：組み合わせによる複数の変更） | Very high（日本語訳：非常に高い） |
| Split URL（日本語訳：分割URL） | Different URLs for variants（日本語訳：バリアントごとに異なる URL） | Moderate（日本語訳：適度） |

---

## Sample Size （日本語訳：サンプルサイズ）

### Quick Reference （日本語訳：クイックリファレンス）

| Baseline（日本語訳：ベースライン） | 10% Lift（日本語訳：10% リフト） | 20% Lift（日本語訳：20% 上昇） | 50% Lift（日本語訳：50% リフト） |
|----------|----------|----------|----------|
| 1% | 150k/variant（日本語訳：150k/バリアント） | 39k/variant（日本語訳：39k/バリアント） | 6k/variant（日本語訳：6k/バリアント） |
| 3% | 47k/variant（日本語訳：47k/バリアント） | 12k/variant（日本語訳：12k/バリアント） | 2k/variant（日本語訳：2k/バリアント） |
| 5% | 27k/variant（日本語訳：27k/バリアント） | 7k/variant（日本語訳：7k/バリアント） | 1.2k/variant（日本語訳：1.2k/バリアント） |
| 10% | 12k/variant（日本語訳：12k/バリアント） | 3k/variant（日本語訳：3k/バリアント） | 550/variant（日本語訳：550/バリアント） |

**Calculators:** （日本語訳：**電卓:**）
- [Evan Miller's](https://www.evanmiller.org/ab-testing/sample-size.html) （日本語訳：[エヴァン・ミラーズ](https://www.evanmiller.org/ab-testing/sample-size.html)）
- [Optimizely's](https://www.optimizely.com/sample-size-calculator/) （日本語訳：[Optimizely の](https://www.optimizely.com/sample-size-calculator/)）

**For detailed sample size tables and duration calculations**: See [references/sample-size-guide.md](references/sample-size-guide.md) （日本語訳：**サンプル サイズの詳細な表と期間の計算について**: [references/sample-size-guide.md](references/sample-size-guide.md) を参照してください。）

---

## Metrics Selection （日本語訳：メトリクスの選択）

### Primary Metric （日本語訳：プライマリメトリクス）
- Single metric that matters most （日本語訳：最も重要な単一の指標）
- Directly tied to hypothesis （日本語訳：仮説に直結する）
- What you'll use to call the test （日本語訳：テストの呼び出しに使用するもの）

### Secondary Metrics （日本語訳：二次指標）
- Support primary metric interpretation （日本語訳：主要なメトリクスの解釈をサポート）
- Explain why/how the change worked （日本語訳：変更がどのように機能したのか理由を説明する）

### Guardrail Metrics （日本語訳：ガードレールのメトリクス）
- Things that shouldn't get worse （日本語訳：これ以上悪化してはいけないこと）
- Stop test if significantly negative （日本語訳：著しく陰性の場合は検査を中止する）

### Example: Pricing Page Test （日本語訳：例: 価格ページのテスト）
- **Primary**: Plan selection rate （日本語訳：**主要**: プラン選択率）
- **Secondary**: Time on page, plan distribution （日本語訳：**二次**: ページ滞在時間、計画の配布）
- **Guardrail**: Support tickets, refund rate （日本語訳：**ガードレール**: サポート チケット、払い戻し率）

---

## Designing Variants （日本語訳：バリアントの設計）

### What to Vary （日本語訳：何を変更するか）

| Category（日本語訳：カテゴリ） | Examples（日本語訳：例） |
|----------|----------|
| Headlines/Copy（日本語訳：見出し/コピー） | Message angle, value prop, specificity, tone（日本語訳：メッセージの角度、価値観、具体性、トーン） |
| Visual Design（日本語訳：ビジュアルデザイン） | Layout, color, images, hierarchy（日本語訳：レイアウト、色、画像、階層） |
| CTA（日本語訳：CTA） | Button copy, size, placement, number（日本語訳：ボタンのコピー、サイズ、配置、数） |
| Content（日本語訳：コンテンツ） | Information included, order, amount, social proof（日本語訳：含まれる情報、注文、金額、社会的証明） |

### Best Practices （日本語訳：ベストプラクティス）
- Single, meaningful change （日本語訳：単一の意味のある変更）
- Bold enough to make a difference （日本語訳：変化をもたらすほど大胆に）
- True to the hypothesis （日本語訳：仮説に忠実）

---

## Traffic Allocation （日本語訳：トラフィックの割り当て）

| Approach（日本語訳：アプローチ） | Split（日本語訳：スプリット） | When to Use（日本語訳：いつ使用するか） |
|----------|-------|-------------|
| Standard（日本語訳：標準） | 50/50 | Default for A/B（日本語訳：A/Bのデフォルト） |
| Conservative（日本語訳：保守的） | 90/10, 80/20 | Limit risk of bad variant（日本語訳：不正なバリアントのリスクを制限する） |
| Ramping（日本語訳：ランピング） | Start small, increase（日本語訳：小さく始めて増やしていく） | Technical risk mitigation（日本語訳：技術的なリスクの軽減） |

**Considerations:** （日本語訳：**考慮事項:**）
- Consistency: Users see same variant on return （日本語訳：一貫性: ユーザーには戻ったときに同じバリアントが表示されます。）
- Balanced exposure across time of day/week （日本語訳：時間帯や週全体でバランスのとれた露出を実現）

---

## Implementation （日本語訳：実装）

### Client-Side （日本語訳：クライアント側）
- JavaScript modifies page after load （日本語訳：JavaScript はロード後にページを変更します）
- Quick to implement, can cause flicker （日本語訳：すぐに実装できるが、ちらつきが発生する可能性がある）
- Tools: PostHog, Optimizely, VWO （日本語訳：ツール: PostHog、Optimizely、VWO）

### Server-Side （日本語訳：サーバー側）
- Variant determined before render （日本語訳：レンダリング前に決定されたバリアント）
- No flicker, requires dev work （日本語訳：ちらつきなし、開発作業が必要）
- Tools: PostHog, LaunchDarkly, Split （日本語訳：ツール: PostHog、LaunchDarkly、Split）

---

## Running the Test （日本語訳：テストの実行）

### Pre-Launch Checklist （日本語訳：発売前チェックリスト）
- [ ] Hypothesis documented （日本語訳：[ ] 仮説が文書化されました）
- [ ] Primary metric defined （日本語訳：[ ] プライマリ メトリックが定義されました）
- [ ] Sample size calculated （日本語訳：[ ] 計算されたサンプルサイズ）
- [ ] Variants implemented correctly （日本語訳：[ ] バリアントは正しく実装されました）
- [ ] Tracking verified （日本語訳：[ ] 追跡確認済み）
- [ ] QA completed on all variants （日本語訳：[ ] すべてのバリエーションについて QA が完了しました）

### During the Test （日本語訳：テスト中）

**DO:** （日本語訳：**する：**）
- Monitor for technical issues （日本語訳：技術的な問題を監視する）
- Check segment quality （日本語訳：セグメントの品質をチェックする）
- Document external factors （日本語訳：外部要因を文書化する）

**DON'T:** （日本語訳：**禁止事項:**）
- Peek at results and stop early （日本語訳：結果を確認して早めに停止する）
- Make changes to variants （日本語訳：バリアントに変更を加える）
- Add traffic from new sources （日本語訳：新しいソースからのトラフィックを追加する）

### The Peeking Problem （日本語訳：覗き見の問題）
Looking at results before reaching sample size and stopping early leads to false positives and wrong decisions. Pre-commit to sample size and trust the process. （日本語訳：サンプルサイズに達する前に結果を確認し、早期に停止すると、誤検知や誤った決定につながります。サンプルサイズを事前に約束し、プロセスを信頼します。）

---

## Analyzing Results （日本語訳：結果の分析）

### Statistical Significance （日本語訳：統計的有意性）
- 95% confidence = p-value < 0.05 （日本語訳：95% 信頼度 = p 値 < 0.05）
- Means <5% chance result is random （日本語訳：確率が 5% 未満の結果はランダムであることを意味します）
- Not a guarantee—just a threshold （日本語訳：保証ではなく、単なるしきい値です）

### Analysis Checklist （日本語訳：分析チェックリスト）

1. **Reach sample size?** If not, result is preliminary （日本語訳：**サンプルサイズに達していますか?** そうでない場合、結果は暫定的なものです）
2. **Statistically significant?** Check confidence intervals （日本語訳：**統計的に有意ですか?** 信頼区間を確認してください）
3. **Effect size meaningful?** Compare to MDE, project impact （日本語訳：**効果の大きさは意味がありますか?** MDE との比較、プロジェクトへの影響）
4. **Secondary metrics consistent?** Support the primary? （日本語訳：**セカンダリ メトリクスは一貫していますか?** プライマリをサポートしますか?）
5. **Guardrail concerns?** Anything get worse? （日本語訳：**ガードレールに関する懸念?** さらに悪化することはありますか?）
6. **Segment differences?** Mobile vs. desktop? New vs. returning? （日本語訳：**セグメントの違いは?** モバイルとデスクトップの違い?新規と復帰?）

### Interpreting Results （日本語訳：結果の解釈）

| Result（日本語訳：結果） | Conclusion（日本語訳：結論） |
|--------|------------|
| Significant winner（日本語訳：重要な勝者） | Implement variant（日本語訳：バリアントの実装） |
| Significant loser（日本語訳：重大な敗者） | Keep control, learn why（日本語訳：コントロールを維持し、その理由を学びましょう） |
| No significant difference（日本語訳：大きな違いはありません） | Need more traffic or bolder test（日本語訳：より多くのトラフィックまたはより大胆なテストが必要） |
| Mixed signals（日本語訳：混合信号） | Dig deeper, maybe segment（日本語訳：さらに深く掘り下げて、おそらくセグメント化する） |

---

## Documentation （日本語訳：ドキュメント）

Document every test with: （日本語訳：すべてのテストを次のように文書化します。）
- Hypothesis （日本語訳：仮説）
- Variants (with screenshots) （日本語訳：バリエーション (スクリーンショット付き)）
- Results (sample, metrics, significance) （日本語訳：結果 (サンプル、指標、有意性)）
- Decision and learnings （日本語訳：決断と学習）

**For templates**: See [references/test-templates.md](references/test-templates.md) （日本語訳：**テンプレートについて**: [references/test-templates.md](references/test-templates.md) を参照してください。）

---

## Common Mistakes （日本語訳：よくある間違い）

### Test Design （日本語訳：テスト設計）
- Testing too small a change (undetectable) （日本語訳：テストする変化が小さすぎる (検出できない)）
- Testing too many things (can't isolate) （日本語訳：テストが多すぎる（特定できない））
- No clear hypothesis （日本語訳：明確な仮説はない）

### Execution （日本語訳：実行）
- Stopping early （日本語訳：早めに止める）
- Changing things mid-test （日本語訳：テスト途中で変更する）
- Not checking implementation （日本語訳：実装をチェックしていない）

### Analysis （日本語訳：分析）
- Ignoring confidence intervals （日本語訳：信頼区間の無視）
- Cherry-picking segments （日本語訳：厳選セグメント）
- Over-interpreting inconclusive results （日本語訳：決定的でない結果を拡大解釈する）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What's your current conversion rate? （日本語訳：現在のコンバージョン率はどれくらいですか?）
2. How much traffic does this page get? （日本語訳：このページのトラフィックはどれくらいですか?）
3. What change are you considering and why? （日本語訳：どのような変更を検討していますか?またその理由は何ですか?）
4. What's the smallest improvement worth detecting? （日本語訳：検出する価値のある最小の改善は何ですか?）
5. What tools do you have for testing? （日本語訳：テスト用にどのようなツールがありますか?）
6. Have you tested this area before? （日本語訳：以前にこの領域をテストしたことがありますか?）

---

## Related Skills （日本語訳：関連スキル）

- **page-cro**: For generating test ideas based on CRO principles （日本語訳：**page-cro**: CRO の原則に基づいてテストのアイデアを生成するため）
- **analytics-tracking**: For setting up test measurement （日本語訳：**analytics-tracking**: テスト測定のセットアップ用）
- **copywriting**: For creating variant copy （日本語訳：**コピーライティング**: バリアント コピーの作成用）
