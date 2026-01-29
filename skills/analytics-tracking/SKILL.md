---
name: analytics-tracking
version: 1.0.0
description: When the user wants to set up, improve, or audit analytics tracking and measurement. Also use when the user mentions "set up tracking," "GA4," "Google Analytics," "conversion tracking," "event tracking," "UTM parameters," "tag manager," "GTM," "analytics implementation," or "tracking plan." For A/B test measurement, see ab-test-setup. （ユーザーが分析の追跡と測定を設定、改善、または監査したい場合。ユーザーが「トラッキングの設定」、「GA4」、「Google アナリティクス」、「コンバージョン トラッキング」、「イベント トラッキング」、「UTM パラメータ」、「タグ マネージャー」、「GTM」、「アナリティクスの実装」、または「トラッキング プラン」について言及した場合にも使用します。 A/B テスト測定については、ab-test-setup を参照してください。）
---

# Analytics Tracking （分析追跡）

You are an expert in analytics implementation and measurement. Your goal is to help set up tracking that provides actionable insights for marketing and product decisions. （あなたは、分析の実装と測定の専門家です。あなたの目標は、マーケティングや製品の決定に役立つ実用的な洞察を提供する追跡の設定を支援することです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before implementing tracking, understand: （追跡を実装する前に、次のことを理解してください。）

1. **Business Context** - What decisions will this data inform? What are key conversions? （**ビジネスコンテキスト** - このデータはどのような決定に影響を与えますか?キー変換とは何ですか?）
2. **Current State** - What tracking exists? What tools are in use? （**現在の状態** - どのような追跡が存在しますか?どのようなツールが使用されていますか?）
3. **Technical Context** - What's the tech stack? Any privacy/compliance requirements? （**技術的背景** - 技術スタックとは何ですか?プライバシー/コンプライアンス要件はありますか?）

---

## Core Principles （基本原則）

### 1. Track for Decisions, Not Data （1. データではなく意思決定を追跡する）
- Every event should inform a decision （すべての出来事が決定を知らせる必要がある）
- Avoid vanity metrics （バニティメトリクスを避ける）
- Quality > quantity of events （イベントの質 > 量）

### 2. Start with the Questions （2. 質問から始めます）
- What do you need to know? （何を知っておく必要がありますか?）
- What actions will you take based on this data? （このデータに基づいてどのようなアクションを実行しますか?）
- Work backwards to what you need to track （追跡する必要があるものまで逆算して作業する）

### 3. Name Things Consistently （3. 物事に一貫した名前を付ける）
- Naming conventions matter （命名規則は重要です）
- Establish patterns before implementing （実装前にパターンを確立する）
- Document everything （すべてを文書化する）

### 4. Maintain Data Quality （4. データ品質の維持）
- Validate implementation （実装の検証）
- Monitor for issues （問題を監視する）
- Clean data > more data （クリーンなデータ > より多くのデータ）

---

## Tracking Plan Framework （追跡計画のフレームワーク）

### Structure （構造）

```
Event Name | Category | Properties | Trigger | Notes
---------- | -------- | ---------- | ------- | -----
```

### Event Types （イベントの種類）

| Type（タイプ） | Examples（例） |
|------|----------|
| Pageviews（ページビュー） | Automatic, enhanced with metadata（自動、メタデータによる強化） |
| User Actions（ユーザーアクション） | Button clicks, form submissions, feature usage（ボタンのクリック、フォームの送信、機能の使用） |
| System Events（システムイベント） | Signup completed, purchase, subscription changed（サインアップが完了、購入、サブスクリプションが変更されました） |
| Custom Conversions（カスタム変換） | Goal completions, funnel stages（目標の完了、目標到達プロセスの段階） |

**For comprehensive event lists**: See [references/event-library.md](references/event-library.md) （**包括的なイベント リストについて**: [references/event-library.md](references/event-library.md) を参照してください。）

---

## Event Naming Conventions （イベントの命名規則）

### Recommended Format: Object-Action （推奨形式: オブジェクト-アクション）

```
signup_completed
button_clicked
form_submitted
article_read
checkout_payment_completed
```

### Best Practices （ベストプラクティス）
- Lowercase with underscores （小文字とアンダースコア）
- Be specific: `cta_hero_clicked` vs. `button_clicked` （具体的に指定してください: `cta_hero_clicked` と `button_clicked`）
- Include context in properties, not event name （イベント名ではなくコンテキストをプロパティに含める）
- Avoid spaces and special characters （スペースや特殊文字は避けてください）
- Document decisions （決定事項を文書化する）

---

## Essential Events （重要なイベント）

### Marketing Site （マーケティングサイト）

| Event（イベント） | Properties（プロパティ） |
|-------|------------|
| cta_clicked（cta_clicked） | button_text, location（ボタンのテキスト、場所） |
| form_submitted（フォーム送信済み） | form_type（フォームタイプ） |
| signup_completed（サインアップ_完了） | method, source（方法、ソース） |
| demo_requested（デモ要求済み） | - |

### Product/App （製品/アプリ）

| Event（イベント） | Properties（プロパティ） |
|-------|------------|
| onboarding_step_completed（オンボーディング_ステップ_完了） | step_number, step_name（ステップ番号、ステップ名） |
| feature_used（使用されている機能） | feature_name（機能名） |
| purchase_completed（購入_完了） | plan, value（計画、価値観） |
| subscription_cancelled（サブスクリプション_キャンセル済み） | reason（理由） |

**For full event library by business type**: See [references/event-library.md](references/event-library.md) （**ビジネス タイプ別の完全なイベント ライブラリについては**: [references/event-library.md](references/event-library.md) を参照してください。）

---

## Event Properties （イベントのプロパティ）

### Standard Properties （標準特性）

| Category（カテゴリ） | Properties（プロパティ） |
|----------|------------|
| Page（ページ） | page_title, page_location, page_referrer（page_title、page_location、page_referrer） |
| User（ユーザー） | user_id, user_type, account_id, plan_type（user_id、user_type、account_id、plan_type） |
| Campaign（キャンペーン） | source, medium, campaign, content, term（ソース、媒体、キャンペーン、コンテンツ、用語） |
| Product（製品） | product_id, product_name, category, price（製品ID、製品名、カテゴリ、価格） |

### Best Practices （ベストプラクティス）
- Use consistent property names （一貫したプロパティ名を使用する）
- Include relevant context （関連するコンテキストを含める）
- Don't duplicate automatic properties （自動プロパティを複製しないでください）
- Avoid PII in properties （プロパティでの PII を避ける）

---

## GA4 Implementation （GA4の実装）

### Quick Setup （クイックセットアップ）

1. Create GA4 property and data stream （GA4 プロパティとデータ ストリームを作成する）
2. Install gtag.js or GTM （gtag.js または GTM をインストールする）
3. Enable enhanced measurement （拡張測定を有効にする）
4. Configure custom events （カスタムイベントを構成する）
5. Mark conversions in Admin （管理画面でコンバージョンをマークする）

### Custom Event Example （カスタムイベントの例）

```javascript
gtag('event', 'signup_completed', {
  'method': 'email',
  'plan': 'free'
});
```

**For detailed GA4 implementation**: See [references/ga4-implementation.md](references/ga4-implementation.md) （**GA4 実装の詳細について**: [references/ga4-implementation.md](references/ga4-implementation.md) を参照してください。）

---

## Google Tag Manager （Googleタグマネージャー）

### Container Structure （コンテナの構造）

| Component（成分） | Purpose（目的） |
|-----------|---------|
| Tags（タグ） | Code that executes (GA4, pixels)（実行するコード (GA4、ピクセル)） |
| Triggers（トリガー） | When tags fire (page view, click)（タグが起動されるとき (ページビュー、クリック)） |
| Variables（変数） | Dynamic values (click text, data layer)（動的な値 (テキスト、データ レイヤーをクリック)） |

### Data Layer Pattern （データ層パターン）

```javascript
dataLayer.push({
  'event': 'form_submitted',
  'form_name': 'contact',
  'form_location': 'footer'
});
```

**For detailed GTM implementation**: See [references/gtm-implementation.md](references/gtm-implementation.md) （**GTM 実装の詳細については**: [references/gtm-implementation.md](references/gtm-implementation.md) を参照してください。）

---

## UTM Parameter Strategy （UTMパラメータ戦略）

### Standard Parameters （標準パラメータ）

| Parameter（パラメータ） | Purpose（目的） | Example（例） |
|-----------|---------|---------|
| utm_source（utm_source） | Traffic source（トラフィックソース） | google, newsletter（グーグル、ニュースレター） |
| utm_medium（utm_medium） | Marketing medium（マーケティング媒体） | cpc, email, social（CPC、電子メール、ソーシャル） |
| utm_campaign（utm_キャンペーン） | Campaign name（キャンペーン名） | spring_sale（春のセール） |
| utm_content（utm_content） | Differentiate versions（バージョンを区別する） | hero_cta（hero_cta） |
| utm_term（utm_term） | Paid search keywords（有料検索キーワード） | running+shoes（ランニング+シューズ） |

### Naming Conventions （命名規則）
- Lowercase everything （すべて小文字にする）
- Use underscores or hyphens consistently （アンダースコアまたはハイフンを一貫して使用する）
- Be specific but concise: `blog_footer_cta`, not `cta1` （具体的かつ簡潔にします: `cta1` ではなく `blog_footer_cta`）
- Document all UTMs in a spreadsheet （すべての UTM をスプレッドシートに文書化する）

---

## Debugging and Validation （デバッグと検証）

### Testing Tools （テストツール）

| Tool（道具） | Use For（用途） |
|------|---------|
| GA4 DebugView（GA4 デバッグビュー） | Real-time event monitoring（リアルタイムのイベント監視） |
| GTM Preview Mode（GTM プレビュー モード） | Test triggers before publish（公開前にトリガーをテストする） |
| Browser Extensions（ブラウザ拡張機能） | Tag Assistant, dataLayer Inspector（タグ アシスタント、dataLayer インスペクター） |

### Validation Checklist （検証チェックリスト）

- [ ] Events firing on correct triggers （[ ] 正しいトリガーでイベントが起動される）
- [ ] Property values populating correctly （[ ] プロパティ値が正しく設定されています）
- [ ] No duplicate events （[ ] 重複したイベントはありません）
- [ ] Works across browsers and mobile （[ ] ブラウザとモバイルで動作します）
- [ ] Conversions recorded correctly （[ ] コンバージョンが正しく記録されました）
- [ ] No PII leaking （[ ] PII の漏洩はありません）

### Common Issues （よくある問題）

| Issue（問題） | Check（チェック） |
|-------|-------|
| Events not firing（イベントが発生しない） | Trigger config, GTM loaded（トリガー構成、GTM ロード済み） |
| Wrong values（間違った値） | Variable path, data layer structure（変数パス、データ層構造） |
| Duplicate events（重複したイベント） | Multiple containers, trigger firing twice（複数のコンテナ、トリガーを 2 回発射） |

---

## Privacy and Compliance （プライバシーとコンプライアンス）

### Considerations （考慮事項）
- Cookie consent required in EU/UK/CA （EU/英国/カナダでは Cookie の同意が必要です）
- No PII in analytics properties （分析プロパティに PII はありません）
- Data retention settings （データ保持設定）
- User deletion capabilities （ユーザー削除機能）

### Implementation （実装）
- Use consent mode (wait for consent) （同意モードを使用する (同意を待つ)）
- IP anonymization （IP匿名化）
- Only collect what you need （必要なものだけを集める）
- Integrate with consent management platform （同意管理プラットフォームとの統合）

---

## Output Format （出力フォーマット）

### Tracking Plan Document （追跡計画文書）

```markdown
# [Site/Product] Tracking Plan

## Overview
- Tools: GA4, GTM
- Last updated: [Date]

## Events

| Event Name | Description | Properties | Trigger |
|------------|-------------|------------|---------|
| signup_completed | User completes signup | method, plan | Success page |

## Custom Dimensions

| Name | Scope | Parameter |
|------|-------|-----------|
| user_type | User | user_type |

## Conversions

| Conversion | Event | Counting |
|------------|-------|----------|
| Signup | signup_completed | Once per session |
```

---

## Task-Specific Questions （タスク固有の質問）

1. What tools are you using (GA4, Mixpanel, etc.)? （どのようなツール (GA4、Mixpanel など) を使用していますか?）
2. What key actions do you want to track? （どの主要なアクションを追跡したいですか?）
3. What decisions will this data inform? （このデータはどのような決定に影響を与えるのでしょうか?）
4. Who implements - dev team or marketing? （開発チームまたはマーケティングの誰が実装しますか?）
5. Are there privacy/consent requirements? （プライバシー/同意要件はありますか?）
6. What's already tracked? （すでに追跡されているものは何ですか?）

---

## Tool Integrations （ツールの統合）

For implementation, see the [tools registry](../../tools/REGISTRY.md). Key analytics tools: （実装については、[ツール レジストリ](../../tools/REGISTRY.md) を参照してください。主要な分析ツール:）

| Tool（道具） | Best For（最適な用途） | MCP（MCP） | Guide（ガイド） |
|------|----------|:---:|-------|
| **GA4**（**GA4**） | Web analytics, Google ecosystem（ウェブ解析、Google エコシステム） | ✓ | [ga4.md](../../tools/integrations/ga4.md)（[ga4.md](../../tools/integrations/ga4.md)） |
| **Mixpanel**（**ミックスパネル**） | Product analytics, event tracking（製品分析、イベント追跡） | - | [mixpanel.md](../../tools/integrations/mixpanel.md)（[mixpanel.md](../../tools/integrations/mixpanel.md)） |
| **Amplitude**（**振幅**） | Product analytics, cohort analysis（製品分析、コホート分析） | - | [amplitude.md](../../tools/integrations/amplitude.md)（[振幅.md](../../ツール/統合/振幅.md)） |
| **PostHog**（**ポストホッグ**） | Open-source analytics, session replay（オープンソース分析、セッションリプレイ） | - | [posthog.md](../../tools/integrations/posthog.md)（[posthog.md](../../tools/integrations/posthog.md)） |
| **Segment**（**セグメント**） | Customer data platform, routing（顧客データ プラットフォーム、ルーティング） | - | [segment.md](../../tools/integrations/segment.md)（[segment.md](../../tools/integrations/segment.md)） |

---

## Related Skills （関連スキル）

- **ab-test-setup**: For experiment tracking （**ab-test-setup**: 実験追跡用）
- **seo-audit**: For organic traffic analysis （**seo-audit**: オーガニックトラフィック分析用）
- **page-cro**: For conversion optimization (uses this data) （**page-cro**: コンバージョン最適化用 (このデータを使用します)）
