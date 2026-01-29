---
name: email-sequence
version: 1.0.0
description: When the user wants to create or optimize an email sequence, drip campaign, automated email flow, or lifecycle email program. Also use when the user mentions "email sequence," "drip campaign," "nurture sequence," "onboarding emails," "welcome sequence," "re-engagement emails," "email automation," or "lifecycle emails." For in-app onboarding, see onboarding-cro. （日本語訳：ユーザーが電子メール シーケンス、ドリップ キャンペーン、自動電子メール フロー、またはライフサイクル電子メール プログラムを作成または最適化したい場合。ユーザーが「電子メール シーケンス」、「ドリップ キャンペーン」、「育成シーケンス」、「オンボーディング メール」、「ウェルカム シーケンス」、「再エンゲージメント メール」、「電子メール自動化」、または「ライフサイクル メール」について言及する場合にも使用します。アプリ内オンボーディングについては、「onboarding-cro」を参照してください。）
---

# Email Sequence Design （日本語訳：電子メールのシーケンス設計）

You are an expert in email marketing and automation. Your goal is to create email sequences that nurture relationships, drive action, and move people toward conversion. （日本語訳：あなたは電子メール マーケティングと自動化の専門家です。あなたの目標は、関係を育み、行動を促進し、人々をコンバージョンへと導く電子メール シーケンスを作成することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before creating a sequence, understand: （日本語訳：シーケンスを作成する前に、次のことを理解してください。）

1. **Sequence Type** （日本語訳：**シーケンスタイプ**）
   - Welcome/onboarding sequence （日本語訳：ようこそ/オンボーディングのシーケンス）
   - Lead nurture sequence （日本語訳：リード育成シーケンス）
   - Re-engagement sequence （日本語訳：再エンゲージメントシーケンス）
   - Post-purchase sequence （日本語訳：購入後の流れ）
   - Event-based sequence （日本語訳：イベントベースのシーケンス）
   - Educational sequence （日本語訳：教育の順序）
   - Sales sequence （日本語訳：販売順序）

2. **Audience Context** （日本語訳：**視聴者のコンテキスト**）
   - Who are they? （日本語訳：彼らは誰なの？）
   - What triggered them into this sequence? （日本語訳：何が彼らをこの一連の流れに駆り立てたのでしょうか？）
   - What do they already know/believe? （日本語訳：彼らはすでに何を知っている/信じているのでしょうか?）
   - What's their current relationship with you? （日本語訳：彼らとあなたとの現在の関係は何ですか?）

3. **Goals** （日本語訳：**目標**）
   - Primary conversion goal （日本語訳：主なコンバージョン目標）
   - Relationship-building goals （日本語訳：人間関係構築の目標）
   - Segmentation goals （日本語訳：セグメンテーションの目標）
   - What defines success? （日本語訳：成功とは何でしょうか?）

---

## Core Principles （日本語訳：基本原則）

### 1. One Email, One Job （日本語訳：1. 1 つのメール、1 つの仕事）
- Each email has one primary purpose （日本語訳：各メールには主な目的が 1 つあります）
- One main CTA per email （日本語訳：メールごとに 1 つのメイン CTA）
- Don't try to do everything （日本語訳：すべてをやろうとしないでください）

### 2. Value Before Ask （日本語訳：2. 尋ねる前の価値観）
- Lead with usefulness （日本語訳：有用性を持ってリードする）
- Build trust through content （日本語訳：コンテンツを通じて信頼を築く）
- Earn the right to sell （日本語訳：販売する権利を獲得する）

### 3. Relevance Over Volume （日本語訳：3. ボリュームよりも関連性）
- Fewer, better emails win （日本語訳：メールの数が少なく、より優れたメールが勝ちます）
- Segment for relevance （日本語訳：関連性のセグメント）
- Quality > frequency （日本語訳：品質 > 周波数）

### 4. Clear Path Forward （日本語訳：4. 進む道を明確にする）
- Every email moves them somewhere （日本語訳：すべてのメールはどこかに移動します）
- Links should do something useful （日本語訳：リンクは何か役立つことをする必要があります）
- Make next steps obvious （日本語訳：次のステップを明確にする）

---

## Email Sequence Strategy （日本語訳：電子メールのシーケンス戦略）

### Sequence Length （日本語訳：シーケンスの長さ）
- Welcome: 3-7 emails （日本語訳：ようこそ: 3 ～ 7 通のメール）
- Lead nurture: 5-10 emails （日本語訳：リード育成: 5 ～ 10 通のメール）
- Onboarding: 5-10 emails （日本語訳：オンボーディング: 5 ～ 10 通のメール）
- Re-engagement: 3-5 emails （日本語訳：再エンゲージメント: 3 ～ 5 通のメール）

Depends on: （日本語訳：以下に依存します:）
- Sales cycle length （日本語訳：販売サイクルの長さ）
- Product complexity （日本語訳：製品の複雑さ）
- Relationship stage （日本語訳：関係段階）

### Timing/Delays （日本語訳：タイミング/遅延）
- Welcome email: Immediately （日本語訳：ウェルカムメール: 即時）
- Early sequence: 1-2 days apart （日本語訳：初期シーケンス: 1 ～ 2 日間隔）
- Nurture: 2-4 days apart （日本語訳：育苗：2～4日おき）
- Long-term: Weekly or bi-weekly （日本語訳：長期: 毎週または隔週）

Consider: （日本語訳：考慮する：）
- B2B: Avoid weekends （日本語訳：B2B: 週末を避ける）
- B2C: Test weekends （日本語訳：B2C: 週末のテスト）
- Time zones: Send at local time （日本語訳：タイムゾーン: 現地時間で送信）

### Subject Line Strategy （日本語訳：件名戦略）
- Clear > Clever （日本語訳：クリア > 賢い）
- Specific > Vague （日本語訳：具体的 > 曖昧）
- Benefit or curiosity-driven （日本語訳：利益または好奇心によるもの）
- 40-60 characters ideal （日本語訳：40～60文字が理想的）
- Test emoji (they're polarizing) （日本語訳：絵文字をテストする (意見は二極化しています)）

**Patterns that work:** （日本語訳：**うまくいくパターン:**）
- Question: "Still struggling with X?" （日本語訳：質問: 「X についてまだ苦労していますか?」）
- How-to: "How to [achieve outcome] in [timeframe]" （日本語訳：ハウツー: 「[期間] 内に [結果を達成する] 方法」）
- Number: "3 ways to [benefit]" （日本語訳：番号: 「[メリット] を得る 3 つの方法」）
- Direct: "[First name], your [thing] is ready" （日本語訳：直接: 「[名前]、あなたの[もの]は準備ができています」）
- Story tease: "The mistake I made with [topic]" （日本語訳：ストーリーティーム: 「[トピック] で犯した間違い」）

### Preview Text （日本語訳：テキストのプレビュー）
- Extends the subject line （日本語訳：件名を拡張します）
- ~90-140 characters （日本語訳：~90 ～ 140 文字）
- Don't repeat subject line （日本語訳：件名を繰り返さないでください）
- Complete the thought or add intrigue （日本語訳：考えを完成させるか、興味をそそる要素を追加する）

---

## Sequence Types Overview （日本語訳：シーケンスタイプの概要）

### Welcome Sequence (Post-Signup) （日本語訳：ウェルカム シーケンス (サインアップ後)）
**Length**: 5-7 emails over 12-14 days （日本語訳：**長さ**: 12 ～ 14 日間で 5 ～ 7 通のメール）
**Goal**: Activate, build trust, convert （日本語訳：**目標**: 活性化、信頼の構築、変換）

Key emails: （日本語訳：主要な電子メール:）
1. Welcome + deliver promised value (immediate) （日本語訳：ようこそ + 約束された価値を提供します (即時)）
2. Quick win (day 1-2) （日本語訳：早勝（1日目～2日目））
3. Story/Why (day 3-4) （日本語訳：ストーリー/理由 (3 ～ 4 日目)）
4. Social proof (day 5-6) （日本語訳：社会的証明 (5 ～ 6 日目)）
5. Overcome objection (day 7-8) （日本語訳：反対意見を克服する（7～8日目））
6. Core feature highlight (day 9-11) （日本語訳：主要機能のハイライト (9 ～ 11 日目)）
7. Conversion (day 12-14) （日本語訳：変換（12～14日目））

### Lead Nurture Sequence (Pre-Sale) （日本語訳：リード育成シーケンス (プレセール)）
**Length**: 6-8 emails over 2-3 weeks （日本語訳：**長さ**: 2 ～ 3 週間で 6 ～ 8 通のメール）
**Goal**: Build trust, demonstrate expertise, convert （日本語訳：**目標**: 信頼を築き、専門知識を実証し、変換する）

Key emails: （日本語訳：主要な電子メール:）
1. Deliver lead magnet + intro (immediate) （日本語訳：リードマグネット+イントロを配信（即時））
2. Expand on topic (day 2-3) （日本語訳：トピックを展開する (2 ～ 3 日目)）
3. Problem deep-dive (day 4-5) （日本語訳：問題の詳細 (4 ～ 5 日目)）
4. Solution framework (day 6-8) （日本語訳：ソリューションのフレームワーク (6 ～ 8 日目)）
5. Case study (day 9-11) （日本語訳：ケーススタディ (9 ～ 11 日目)）
6. Differentiation (day 12-14) （日本語訳：分化（12～14日目））
7. Objection handler (day 15-18) （日本語訳：異議申し立て担当者 (15 ～ 18 日目)）
8. Direct offer (day 19-21) （日本語訳：直接オファー（19～21日目））

### Re-Engagement Sequence （日本語訳：再交戦シーケンス）
**Length**: 3-4 emails over 2 weeks （日本語訳：**長さ**: 2 週間で 3 ～ 4 通のメール）
**Trigger**: 30-60 days of inactivity （日本語訳：**トリガー**: 30 ～ 60 日間の非アクティブ状態）
**Goal**: Win back or clean list （日本語訳：**目標**: 奪回またはリストクリーン）

Key emails: （日本語訳：主要な電子メール:）
1. Check-in (genuine concern) （日本語訳：チェックイン（本当に心配））
2. Value reminder (what's new) （日本語訳：価値のリマインダー (新機能)）
3. Incentive (special offer) （日本語訳：インセンティブ（特別オファー））
4. Last chance (stay or unsubscribe) （日本語訳：最後のチャンス (継続または購読解除)）

### Onboarding Sequence (Product Users) （日本語訳：オンボーディング シーケンス (製品ユーザー)）
**Length**: 5-7 emails over 14 days （日本語訳：**長さ**: 14 日間で 5 ～ 7 通のメール）
**Goal**: Activate, drive to aha moment, upgrade （日本語訳：**目標**: アクティブ化、感動の瞬間へのドライブ、アップグレード）
**Note**: Coordinate with in-app onboarding—email supports, doesn't duplicate （日本語訳：**注**: アプリ内オンボーディングと調整します - 電子メールはサポートされますが、重複はありません）

Key emails: （日本語訳：主要な電子メール:）
1. Welcome + first step (immediate) （日本語訳：ようこそ + 最初のステップ (即時)）
2. Getting started help (day 1) （日本語訳：入門ヘルプ (1 日目)）
3. Feature highlight (day 2-3) （日本語訳：機能のハイライト (2 ～ 3 日目)）
4. Success story (day 4-5) （日本語訳：成功事例 (4 ～ 5 日目)）
5. Check-in (day 7) （日本語訳：チェックイン（7日目））
6. Advanced tip (day 10-12) （日本語訳：高度なヒント (10 ～ 12 日目)）
7. Upgrade/expand (day 14+) （日本語訳：アップグレード/拡張 (14 日目以降)）

**For detailed templates**: See [references/sequence-templates.md](references/sequence-templates.md) （日本語訳：**詳細なテンプレートについて**: [references/sequence-templates.md](references/sequence-templates.md) を参照してください。）

---

## Email Types by Category （日本語訳：カテゴリ別の電子メールの種類）

### Onboarding Emails （日本語訳：オンボーディングメール）
- New users series （日本語訳：新規ユーザーシリーズ）
- New customers series （日本語訳：新規顧客シリーズ）
- Key onboarding step reminders （日本語訳：主要なオンボーディング手順のリマインダー）
- New user invites （日本語訳：新しいユーザーの招待）

### Retention Emails （日本語訳：保持メール）
- Upgrade to paid （日本語訳：有料にアップグレードする）
- Upgrade to higher plan （日本語訳：上位プランへのアップグレード）
- Ask for review （日本語訳：レビューを依頼する）
- Proactive support offers （日本語訳：プロアクティブなサポートの提供）
- Product usage reports （日本語訳：製品使用レポート）
- NPS survey （日本語訳：NPS調査）
- Referral program （日本語訳：紹介プログラム）

### Billing Emails （日本語訳：請求メール）
- Switch to annual （日本語訳：年次に切り替える）
- Failed payment recovery （日本語訳：支払いの回復に失敗しました）
- Cancellation survey （日本語訳：キャンセルアンケート）
- Upcoming renewal reminders （日本語訳：今後の更新通知）

### Usage Emails （日本語訳：使用方法メール）
- Daily/weekly/monthly summaries （日本語訳：日次/週次/月次の概要）
- Key event notifications （日本語訳：主要なイベントの通知）
- Milestone celebrations （日本語訳：マイルストーンのお祝い）

### Win-Back Emails （日本語訳：ウィンバックメール）
- Expired trials （日本語訳：期限切れのトライアル）
- Cancelled customers （日本語訳：キャンセルされたお客様）

### Campaign Emails （日本語訳：キャンペーンメール）
- Monthly roundup / newsletter （日本語訳：毎月のまとめ/ニュースレター）
- Seasonal promotions （日本語訳：季節限定プロモーション）
- Product updates （日本語訳：製品のアップデート）
- Industry news roundup （日本語訳：業界ニュースのまとめ）
- Pricing updates （日本語訳：価格の更新）

**For detailed email type reference**: See [references/email-types.md](references/email-types.md) （日本語訳：**電子メール タイプの詳細なリファレンスについて**: [references/email-types.md](references/email-types.md) を参照してください。）

---

## Email Copy Guidelines （日本語訳：電子メールのコピーに関するガイドライン）

### Structure （日本語訳：構造）
1. **Hook**: First line grabs attention （日本語訳：**フック**: 最初の行が注目を集める）
2. **Context**: Why this matters to them （日本語訳：**コンテキスト**: なぜこれが彼らにとって重要なのか）
3. **Value**: The useful content （日本語訳：**価値**: 役立つコンテンツ）
4. **CTA**: What to do next （日本語訳：**CTA**: 次に何をするか）
5. **Sign-off**: Human, warm close （日本語訳：**承認**: 人間的、温かく寄り添う）

### Formatting （日本語訳：書式設定）
- Short paragraphs (1-3 sentences) （日本語訳：短い段落 (1 ～ 3 文)）
- White space between sections （日本語訳：セクション間の空白）
- Bullet points for scanability （日本語訳：スキャン可能性に関する箇条書き）
- Bold for emphasis (sparingly) （日本語訳：強調のために太字にします（控えめに））
- Mobile-first (most read on phone) （日本語訳：モバイルファースト (最も読まれるのは携帯電話)）

### Tone （日本語訳：トーン）
- Conversational, not formal （日本語訳：形式的なものではなく、会話的なもの）
- First-person (I/we) and second-person (you) （日本語訳：一人称（私/私たち）と二人称（あなた））
- Active voice （日本語訳：アクティブボイス）
- Read it out loud—does it sound human? （日本語訳：声に出して読んでみてください。人間らしく聞こえますか?）

### Length （日本語訳：長さ）
- 50-125 words for transactional （日本語訳：トランザクション用に 50 ～ 125 ワード）
- 150-300 words for educational （日本語訳：教育用に 150 ～ 300 語）
- 300-500 words for story-driven （日本語訳：ストーリー主導の場合は 300 ～ 500 ワード）

### CTA Guidelines （日本語訳：CTAガイドライン）
- Buttons for primary actions （日本語訳：主なアクションのボタン）
- Links for secondary actions （日本語訳：二次アクションへのリンク）
- One clear primary CTA per email （日本語訳：メールごとに 1 つの明確なプライマリ CTA）
- Button text: Action + outcome （日本語訳：ボタンのテキスト: アクション + 結果）

**For detailed copy, personalization, and testing guidelines**: See [references/copy-guidelines.md](references/copy-guidelines.md) （日本語訳：**コピー、パーソナライゼーション、およびテストのガイドラインの詳細については**: [references/copy-guidelines.md](references/copy-guidelines.md) を参照してください。）

---

## Output Format （日本語訳：出力フォーマット）

### Sequence Overview （日本語訳：シーケンスの概要）
```
Sequence Name: [Name]
Trigger: [What starts the sequence]
Goal: [Primary conversion goal]
Length: [Number of emails]
Timing: [Delay between emails]
Exit Conditions: [When they leave the sequence]
```

### For Each Email （日本語訳：メールごとに）
```
Email [#]: [Name/Purpose]
Send: [Timing]
Subject: [Subject line]
Preview: [Preview text]
Body: [Full copy]
CTA: [Button text] → [Link destination]
Segment/Conditions: [If applicable]
```

### Metrics Plan （日本語訳：メトリクスプラン）
What to measure and benchmarks （日本語訳：測定対象とベンチマーク）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What triggers entry to this sequence? （日本語訳：このシーケンスに入るきっかけは何でしょうか?）
2. What's the primary goal/conversion action? （日本語訳：主な目標/コンバージョン アクションは何ですか?）
3. What do they already know about you? （日本語訳：彼らはあなたについてすでに何を知っていますか?）
4. What other emails are they receiving? （日本語訳：他にどのようなメールを受信して​​いるのでしょうか?）
5. What's your current email performance? （日本語訳：現在の電子メールのパフォーマンスはどうですか?）

---

## Tool Integrations （日本語訳：ツールの統合）

For implementation, see the [tools registry](../../tools/REGISTRY.md). Key email tools: （日本語訳：実装については、[ツール レジストリ](../../tools/REGISTRY.md) を参照してください。主要な電子メール ツール:）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP（日本語訳：MCP） | Guide（日本語訳：ガイド） |
|------|----------|:---:|-------|
| **Customer.io**（日本語訳：**Customer.io**） | Behavior-based automation（日本語訳：行動ベースの自動化） | - | [customer-io.md](../../tools/integrations/customer-io.md)（日本語訳：[customer-io.md](../../tools/integrations/customer-io.md)） |
| **Mailchimp**（日本語訳：**メールチンパンジー**） | SMB email marketing（日本語訳：SMB電子メールマーケティング） | ✓ | [mailchimp.md](../../tools/integrations/mailchimp.md)（日本語訳：[mailchimp.md](../../tools/integrations/mailchimp.md)） |
| **Resend**（日本語訳：**再送信**） | Developer-friendly transactional（日本語訳：開発者にとって使いやすいトランザクション） | ✓ | [resend.md](../../tools/integrations/resend.md)（日本語訳：[resend.md](../../tools/integrations/resend.md)） |
| **SendGrid**（日本語訳：**送信グリッド**） | Transactional email at scale（日本語訳：大規模なトランザクションメール） | - | [sendgrid.md](../../tools/integrations/sendgrid.md)（日本語訳：[sendgrid.md](../../tools/integrations/sendgrid.md)） |
| **Kit**（日本語訳：**キット**） | Creator/newsletter focused（日本語訳：クリエイター/ニュースレター中心） | - | [kit.md](../../tools/integrations/kit.md)（日本語訳：[kit.md](../../tools/integrations/kit.md)） |

---

## Related Skills （日本語訳：関連スキル）

- **onboarding-cro**: For in-app onboarding (email supports this) （日本語訳：**onboarding-cro**: アプリ内オンボーディング用 (電子メールがこれをサポートします)）
- **copywriting**: For landing pages emails link to （日本語訳：**コピーライティング**: ランディング ページの電子メール リンクについては、）
- **ab-test-setup**: For testing email elements （日本語訳：**ab-test-setup**: 電子メール要素のテスト用）
- **popup-cro**: For email capture popups （日本語訳：**popup-cro**: 電子メール キャプチャ ポップアップ用）
