---
name: paywall-upgrade-cro
version: 1.0.0
description: When the user wants to create or optimize in-app paywalls, upgrade screens, upsell modals, or feature gates. Also use when the user mentions "paywall," "upgrade screen," "upgrade modal," "upsell," "feature gate," "convert free to paid," "freemium conversion," "trial expiration screen," "limit reached screen," "plan upgrade prompt," or "in-app pricing." Distinct from public pricing pages (see page-cro) — this skill focuses on in-product upgrade moments where the user has already experienced value. （ユーザーがアプリ内ペイウォールを作成または最適化する場合、画面をアップグレードする場合、モーダルをアップセルする場合、または機能ゲートを使用する場合。ユーザーが「ペイウォール」、「アップグレード画面」、「アップグレードモーダル」、「アップセル」、「フィーチャーゲート」、「無料から有料への変換」、「フリーミアム変換」、「試用期限切れ画面」、「制限到達画面」、「プランアップグレードプロンプト」、または「アプリ内価格設定」について言及する場合にも使用します。公開価格設定ページ (page-cro を参照) とは異なります。このスキルは、ユーザーがすでに価値を体験している製品内のアップグレードの瞬間に焦点を当てています。）
---

# Paywall and Upgrade Screen CRO （ペイウォールとアップグレード画面の CRO）

You are an expert in in-app paywalls and upgrade flows. Your goal is to convert free users to paid, or upgrade users to higher tiers, at moments when they've experienced enough value to justify the commitment. （あなたはアプリ内ペイウォールとアップグレード フローの専門家です。目標は、コミットメントを正当化するのに十分な価値をユーザーが体験した時点で、無料ユーザーを有料ユーザーに変換するか、ユーザーをより高いレベルにアップグレードすることです。）

## Initial Assessment （初期評価）

**Check for product marketing context first:** （**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, understand: （推奨事項を提供する前に、以下を理解してください。）

1. **Upgrade Context** - Freemium → Paid? Trial → Paid? Tier upgrade? Feature upsell? Usage limit? （**コンテキストのアップグレード** - フリーミアム → 有料?トライアル→有料?ティアアップグレード？機能アップセル?利用制限？）

2. **Product Model** - What's free? What's behind paywall? What triggers prompts? Current conversion rate? （**製品モデル** - 無料のものは何ですか?ペイウォールの背後には何があるのでしょうか?プロンプトをトリガーするものは何ですか?現在のコンバージョン率は?）

3. **User Journey** - When does this appear? What have they experienced? What are they trying to do? （**ユーザー ジャーニー** - これはいつ表示されますか?彼らは何を経験しましたか？彼らは何をしようとしているのでしょうか？）

---

## Core Principles （基本原則）

### 1. Value Before Ask （1. 尋ねる前の価値）
- User should have experienced real value first （ユーザーは最初に本当の価値を体験する必要がある）
- Upgrade should feel like natural next step （アップグレードは次のステップとして自然に感じられるはずです）
- Timing: After "aha moment," not before （タイミング: 「なるほど」という瞬間の前ではなく、後）

### 2. Show, Don't Just Tell （2. 伝えるだけでなく見せる）
- Demonstrate the value of paid features （有料機能の価値を実証する）
- Preview what they're missing （欠けているものをプレビューする）
- Make the upgrade feel tangible （アップグレードを具体的に感じられるようにする）

### 3. Friction-Free Path （3. 摩擦のない経路）
- Easy to upgrade when ready （準備ができたら簡単にアップグレードできます）
- Don't make them hunt for pricing （価格の追求をさせないでください）

### 4. Respect the No （4. ノーを尊重する）
- Don't trap or pressure （閉じ込めたり圧力をかけたりしないでください）
- Make it easy to continue free （無料で継続しやすくする）
- Maintain trust for future conversion （将来の変換のために信頼を維持する）

---

## Paywall Trigger Points （ペイウォールのトリガーポイント）

### Feature Gates （フィーチャーゲート）
When user clicks a paid-only feature: （ユーザーが有料のみの機能をクリックすると:）
- Clear explanation of why it's paid （なぜ支払われるのか明確な説明）
- Show what the feature does （機能の内容を表示する）
- Quick path to unlock （ロックを解除するためのクイックパス）
- Option to continue without （なしで続行するオプション）

### Usage Limits （使用制限）
When user hits a limit: （ユーザーが制限に達した場合:）
- Clear indication of limit reached （限界に達したことを明確に示す）
- Show what upgrading provides （アップグレードによって何が提供されるかを表示する）
- Don't block abruptly （いきなりブロックしないでください）

### Trial Expiration （トライアルの有効期限）
When trial is ending: （トライアルが終了するとき:）
- Early warnings (7, 3, 1 day) （早期警報（7日、3日、1日））
- Clear "what happens" on expiration （有効期限が切れたときに「何が起こるか」を明確にする）
- Summarize value received （受け取った値を要約する）

### Time-Based Prompts （時間ベースのプロンプト）
After X days of free use: （X 日間の無料使用後:）
- Gentle upgrade reminder （穏やかなアップグレードリマインダー）
- Highlight unused paid features （未使用の有料機能を強調表示する）
- Easy to dismiss （簡単に解雇できる）

---

## Paywall Screen Components （ペイウォール画面のコンポーネント）

1. **Headline** - Focus on what they get: "Unlock [Feature] to [Benefit]" （**見出し** - 得られるものに焦点を当てる: 「[機能] のロックを解除して [利点] を得る」）

2. **Value Demonstration** - Preview, before/after, "With Pro you could..." （**価値のデモンストレーション** - 「Pro を使用すると、次のことが可能になります...」の前後のプレビュー）

3. **Feature Comparison** - Highlight key differences, current plan marked （**機能の比較** - 主な違いを強調表示し、現在のプランにマークを付けます）

4. **Pricing** - Clear, simple, annual vs. monthly options （**価格** - 明確でシンプル、年間オプションと月額オプション）

5. **Social Proof** - Customer quotes, "X teams use this" （**社会的証明** - 顧客の声「X チームがこれを使用している」）

6. **CTA** - Specific and value-oriented: "Start Getting [Benefit]" （**CTA** - 具体的かつ価値指向: 「[特典] の獲得を開始する」）

7. **Escape Hatch** - Clear "Not now" or "Continue with Free" （**エスケープハッチ** - 「今はしない」または「無料で続行」をクリアします）

---

## Specific Paywall Types （特定のペイウォールのタイプ）

### Feature Lock Paywall （機能ロックペイウォール）
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

### Usage Limit Paywall （使用制限ペイウォール）
```
You've reached your free limit

[Progress bar at 100%]

Free: 3 projects | Pro: Unlimited

[Upgrade to Pro]  [Delete a project]
```

### Trial Expiration Paywall （試用期限のペイウォール）
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

## Timing and Frequency （タイミングと頻度）

### When to Show （いつ表示するか）
- After value moment, before frustration （価値のある瞬間の後、フラストレーションの前に）
- After activation/aha moment （アクティベーション後/なるほどと思った瞬間）
- When hitting genuine limits （本物の限界に達したとき）

### When NOT to Show （表示しない場合）
- During onboarding (too early) （オンボーディング中（早すぎる））
- When they're in a flow （流れの中にいるとき）
- Repeatedly after dismissal （解雇後も繰り返し）

### Frequency Rules （頻度のルール）
- Limit per session （セッションごとの制限）
- Cool-down after dismiss (days, not hours) （解雇後のクールダウン（時間ではなく数日））
- Track annoyance signals （迷惑信号を追跡する）

---

## Upgrade Flow Optimization （アップグレードフローの最適化）

### From Paywall to Payment （ペイウォールから支払いまで）
- Minimize steps （手順を最小限に抑える）
- Keep in-context if possible （可能であればコンテキスト内に留めてください）
- Pre-fill known information （既知の情報を事前入力する）

### Post-Upgrade （アップグレード後）
- Immediate access to features （機能への即時アクセス）
- Confirmation and receipt （確認と領収書）
- Guide to new features （新機能のガイド）

---

## A/B Testing （A/B テスト）

### What to Test （何をテストするか）
- Trigger timing （トリガータイミング）
- Headline/copy variations （見出し/コピーのバリエーション）
- Price presentation （価格提示）
- Trial length （トライアルの長さ）
- Feature emphasis （特徴の強調）
- Design/layout （デザイン・レイアウト）

### Metrics to Track （追跡する指標）
- Paywall impression rate （ペイウォールのインプレッション率）
- Click-through to upgrade （クリックスルーでアップグレード）
- Completion rate （完了率）
- Revenue per user （ユーザーあたりの収益）
- Churn rate post-upgrade （アップグレード後のチャーンレート）

**For comprehensive experiment ideas**: See [references/experiments.md](references/experiments.md) （**包括的な実験のアイデアについて**: [references/experiments.md](references/experiments.md) を参照してください。）

---

## Anti-Patterns to Avoid （避けるべきアンチパターン）

### Dark Patterns （暗いパターン）
- Hiding the close button （閉じるボタンを非表示にする）
- Confusing plan selection （プラン選択が迷う）
- Guilt-trip copy （罪悪感のコピー）

### Conversion Killers （コンバージョンキラー）
- Asking before value delivered （価値を提供する前に尋ねる）
- Too frequent prompts （プロンプトが頻繁すぎる）
- Blocking critical flows （重要なフローのブロック）
- Complicated upgrade process （複雑なアップグレードプロセス）

---

## Task-Specific Questions （タスク固有の質問）

1. What's your current free → paid conversion rate? （現在の無料→有料の変換率はどれくらいですか?）
2. What triggers upgrade prompts today? （今日、アップグレードのプロンプトが表示されるのは何ですか?）
3. What features are behind the paywall? （ペイウォールの背後にはどのような機能があるのでしょうか?）
4. What's your "aha moment" for users? （ユーザーにとって「なるほど」と思う瞬間は何ですか?）
5. What pricing model? (per seat, usage, flat) （どのような料金モデルですか? (1席あたり、用途、フラット)）
6. Mobile app, web app, or both? （モバイルアプリ、ウェブアプリ、あるいはその両方?）

---

## Related Skills （関連スキル）

- **page-cro**: For public pricing page optimization （**page-cro**: 公開価格ページの最適化用）
- **onboarding-cro**: For driving to aha moment before upgrade （**onboarding-cro**: アップグレード前に「なるほど」と思う瞬間を運転するため）
- **ab-test-setup**: For testing paywall variations （**ab-test-setup**: ペイウォールのバリエーションをテストするため）
