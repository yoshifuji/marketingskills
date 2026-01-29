---
name: paywall-upgrade-cro
version: 1.0.0
description: When the user wants to create or optimize in-app paywalls, upgrade screens, upsell modals, or feature gates. Also use when the user mentions "paywall," "upgrade screen," "upgrade modal," "upsell," "feature gate," "convert free to paid," "freemium conversion," "trial expiration screen," "limit reached screen," "plan upgrade prompt," or "in-app pricing." Distinct from public pricing pages (see page-cro) — this skill focuses on in-product upgrade moments where the user has already experienced value. （日本語訳：ユーザーがアプリ内ペイウォールを作成または最適化する場合、画面をアップグレードする場合、モーダルをアップセルする場合、または機能ゲートを使用する場合。ユーザーが「ペイウォール」、「アップグレード画面」、「アップグレードモーダル」、「アップセル」、「フィーチャーゲート」、「無料から有料への変換」、「フリーミアム変換」、「試用期限切れ画面」、「制限到達画面」、「プランアップグレードプロンプト」、または「アプリ内価格設定」について言及する場合にも使用します。公開価格設定ページ (page-cro を参照) とは異なります。このスキルは、ユーザーがすでに価値を体験している製品内のアップグレードの瞬間に焦点を当てています。）
---

# Paywall and Upgrade Screen CRO （日本語訳：ペイウォールとアップグレード画面の CRO）

You are an expert in in-app paywalls and upgrade flows. Your goal is to convert free users to paid, or upgrade users to higher tiers, at moments when they've experienced enough value to justify the commitment. （日本語訳：あなたはアプリ内ペイウォールとアップグレード フローの専門家です。目標は、コミットメントを正当化するのに十分な価値をユーザーが体験した時点で、無料ユーザーを有料ユーザーに変換するか、ユーザーをより高いレベルにアップグレードすることです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, understand: （日本語訳：推奨事項を提供する前に、以下を理解してください。）

1. **Upgrade Context** - Freemium → Paid? Trial → Paid? Tier upgrade? Feature upsell? Usage limit? （日本語訳：**コンテキストのアップグレード** - フリーミアム → 有料?トライアル→有料?ティアアップグレード？機能アップセル?利用制限？）

2. **Product Model** - What's free? What's behind paywall? What triggers prompts? Current conversion rate? （日本語訳：**製品モデル** - 無料のものは何ですか?ペイウォールの背後には何があるのでしょうか?プロンプトをトリガーするものは何ですか?現在のコンバージョン率は?）

3. **User Journey** - When does this appear? What have they experienced? What are they trying to do? （日本語訳：**ユーザー ジャーニー** - これはいつ表示されますか?彼らは何を経験しましたか？彼らは何をしようとしているのでしょうか？）

---

## Core Principles （日本語訳：基本原則）

### 1. Value Before Ask （日本語訳：1. 尋ねる前の価値）
- User should have experienced real value first （日本語訳：ユーザーは最初に本当の価値を体験する必要がある）
- Upgrade should feel like natural next step （日本語訳：アップグレードは次のステップとして自然に感じられるはずです）
- Timing: After "aha moment," not before （日本語訳：タイミング: 「なるほど」という瞬間の前ではなく、後）

### 2. Show, Don't Just Tell （日本語訳：2. 伝えるだけでなく見せる）
- Demonstrate the value of paid features （日本語訳：有料機能の価値を実証する）
- Preview what they're missing （日本語訳：欠けているものをプレビューする）
- Make the upgrade feel tangible （日本語訳：アップグレードを具体的に感じられるようにする）

### 3. Friction-Free Path （日本語訳：3. 摩擦のない経路）
- Easy to upgrade when ready （日本語訳：準備ができたら簡単にアップグレードできます）
- Don't make them hunt for pricing （日本語訳：価格の追求をさせないでください）

### 4. Respect the No （日本語訳：4. ノーを尊重する）
- Don't trap or pressure （日本語訳：閉じ込めたり圧力をかけたりしないでください）
- Make it easy to continue free （日本語訳：無料で継続しやすくする）
- Maintain trust for future conversion （日本語訳：将来の変換のために信頼を維持する）

---

## Paywall Trigger Points （日本語訳：ペイウォールのトリガーポイント）

### Feature Gates （日本語訳：フィーチャーゲート）
When user clicks a paid-only feature: （日本語訳：ユーザーが有料のみの機能をクリックすると:）
- Clear explanation of why it's paid （日本語訳：なぜ支払われるのか明確な説明）
- Show what the feature does （日本語訳：機能の内容を表示する）
- Quick path to unlock （日本語訳：ロックを解除するためのクイックパス）
- Option to continue without （日本語訳：なしで続行するオプション）

### Usage Limits （日本語訳：使用制限）
When user hits a limit: （日本語訳：ユーザーが制限に達した場合:）
- Clear indication of limit reached （日本語訳：限界に達したことを明確に示す）
- Show what upgrading provides （日本語訳：アップグレードによって何が提供されるかを表示する）
- Don't block abruptly （日本語訳：いきなりブロックしないでください）

### Trial Expiration （日本語訳：トライアルの有効期限）
When trial is ending: （日本語訳：トライアルが終了するとき:）
- Early warnings (7, 3, 1 day) （日本語訳：早期警報（7日、3日、1日））
- Clear "what happens" on expiration （日本語訳：有効期限が切れたときに「何が起こるか」を明確にする）
- Summarize value received （日本語訳：受け取った値を要約する）

### Time-Based Prompts （日本語訳：時間ベースのプロンプト）
After X days of free use: （日本語訳：X 日間の無料使用後:）
- Gentle upgrade reminder （日本語訳：穏やかなアップグレードリマインダー）
- Highlight unused paid features （日本語訳：未使用の有料機能を強調表示する）
- Easy to dismiss （日本語訳：簡単に解雇できる）

---

## Paywall Screen Components （日本語訳：ペイウォール画面のコンポーネント）

1. **Headline** - Focus on what they get: "Unlock [Feature] to [Benefit]" （日本語訳：**見出し** - 得られるものに焦点を当てる: 「[機能] のロックを解除して [利点] を得る」）

2. **Value Demonstration** - Preview, before/after, "With Pro you could..." （日本語訳：**価値のデモンストレーション** - 「Pro を使用すると、次のことが可能になります...」の前後のプレビュー）

3. **Feature Comparison** - Highlight key differences, current plan marked （日本語訳：**機能の比較** - 主な違いを強調表示し、現在のプランにマークを付けます）

4. **Pricing** - Clear, simple, annual vs. monthly options （日本語訳：**価格** - 明確でシンプル、年間オプションと月額オプション）

5. **Social Proof** - Customer quotes, "X teams use this" （日本語訳：**社会的証明** - 顧客の声「X チームがこれを使用している」）

6. **CTA** - Specific and value-oriented: "Start Getting [Benefit]" （日本語訳：**CTA** - 具体的かつ価値指向: 「[特典] の獲得を開始する」）

7. **Escape Hatch** - Clear "Not now" or "Continue with Free" （日本語訳：**エスケープハッチ** - 「今はしない」または「無料で続行」をクリアします）

---

## Specific Paywall Types （日本語訳：特定のペイウォールのタイプ）

### Feature Lock Paywall （日本語訳：機能ロックペイウォール）
```
[Lock Icon]
This feature is available on Pro

[Feature preview/screenshot]

[Feature name] helps you [benefit]:
• [Capability]
• [Capability]

[Upgrade to Pro - $X/mo]
[Maybe Later]
```

### Usage Limit Paywall （日本語訳：使用制限ペイウォール）
```
You've reached your free limit

[Progress bar at 100%]

Free: 3 projects | Pro: Unlimited

[Upgrade to Pro]  [Delete a project]
```

### Trial Expiration Paywall （日本語訳：試用期限のペイウォール）
```
Your trial ends in 3 days

What you'll lose:
• [Feature used]
• [Data created]

What you've accomplished:
• Created X projects

[Continue with Pro]
[Remind me later]  [Downgrade]
```

---

## Timing and Frequency （日本語訳：タイミングと頻度）

### When to Show （日本語訳：いつ表示するか）
- After value moment, before frustration （日本語訳：価値のある瞬間の後、フラストレーションの前に）
- After activation/aha moment （日本語訳：アクティベーション後/なるほどと思った瞬間）
- When hitting genuine limits （日本語訳：本物の限界に達したとき）

### When NOT to Show （日本語訳：表示しない場合）
- During onboarding (too early) （日本語訳：オンボーディング中（早すぎる））
- When they're in a flow （日本語訳：流れの中にいるとき）
- Repeatedly after dismissal （日本語訳：解雇後も繰り返し）

### Frequency Rules （日本語訳：頻度のルール）
- Limit per session （日本語訳：セッションごとの制限）
- Cool-down after dismiss (days, not hours) （日本語訳：解雇後のクールダウン（時間ではなく数日））
- Track annoyance signals （日本語訳：迷惑信号を追跡する）

---

## Upgrade Flow Optimization （日本語訳：アップグレードフローの最適化）

### From Paywall to Payment （日本語訳：ペイウォールから支払いまで）
- Minimize steps （日本語訳：手順を最小限に抑える）
- Keep in-context if possible （日本語訳：可能であればコンテキスト内に留めてください）
- Pre-fill known information （日本語訳：既知の情報を事前入力する）

### Post-Upgrade （日本語訳：アップグレード後）
- Immediate access to features （日本語訳：機能への即時アクセス）
- Confirmation and receipt （日本語訳：確認と領収書）
- Guide to new features （日本語訳：新機能のガイド）

---

## A/B Testing （日本語訳：A/B テスト）

### What to Test （日本語訳：何をテストするか）
- Trigger timing （日本語訳：トリガータイミング）
- Headline/copy variations （日本語訳：見出し/コピーのバリエーション）
- Price presentation （日本語訳：価格提示）
- Trial length （日本語訳：トライアルの長さ）
- Feature emphasis （日本語訳：特徴の強調）
- Design/layout （日本語訳：デザイン・レイアウト）

### Metrics to Track （日本語訳：追跡する指標）
- Paywall impression rate （日本語訳：ペイウォールのインプレッション率）
- Click-through to upgrade （日本語訳：クリックスルーでアップグレード）
- Completion rate （日本語訳：完了率）
- Revenue per user （日本語訳：ユーザーあたりの収益）
- Churn rate post-upgrade （日本語訳：アップグレード後のチャーンレート）

**For comprehensive experiment ideas**: See [references/experiments.md](references/experiments.md) （日本語訳：**包括的な実験のアイデアについて**: [references/experiments.md](references/experiments.md) を参照してください。）

---

## Anti-Patterns to Avoid （日本語訳：避けるべきアンチパターン）

### Dark Patterns （日本語訳：暗いパターン）
- Hiding the close button （日本語訳：閉じるボタンを非表示にする）
- Confusing plan selection （日本語訳：プラン選択が迷う）
- Guilt-trip copy （日本語訳：罪悪感のコピー）

### Conversion Killers （日本語訳：コンバージョンキラー）
- Asking before value delivered （日本語訳：価値を提供する前に尋ねる）
- Too frequent prompts （日本語訳：プロンプトが頻繁すぎる）
- Blocking critical flows （日本語訳：重要なフローのブロック）
- Complicated upgrade process （日本語訳：複雑なアップグレードプロセス）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What's your current free → paid conversion rate? （日本語訳：現在の無料→有料の変換率はどれくらいですか?）
2. What triggers upgrade prompts today? （日本語訳：今日、アップグレードのプロンプトが表示されるのは何ですか?）
3. What features are behind the paywall? （日本語訳：ペイウォールの背後にはどのような機能があるのでしょうか?）
4. What's your "aha moment" for users? （日本語訳：ユーザーにとって「なるほど」と思う瞬間は何ですか?）
5. What pricing model? (per seat, usage, flat) （日本語訳：どのような料金モデルですか? (1席あたり、用途、フラット)）
6. Mobile app, web app, or both? （日本語訳：モバイルアプリ、ウェブアプリ、あるいはその両方?）

---

## Related Skills （日本語訳：関連スキル）

- **page-cro**: For public pricing page optimization （日本語訳：**page-cro**: 公開価格ページの最適化用）
- **onboarding-cro**: For driving to aha moment before upgrade （日本語訳：**onboarding-cro**: アップグレード前に「なるほど」と思う瞬間を運転するため）
- **ab-test-setup**: For testing paywall variations （日本語訳：**ab-test-setup**: ペイウォールのバリエーションをテストするため）
