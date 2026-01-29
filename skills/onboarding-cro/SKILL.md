---
name: onboarding-cro
version: 1.0.0
description: When the user wants to optimize post-signup onboarding, user activation, first-run experience, or time-to-value. Also use when the user mentions "onboarding flow," "activation rate," "user activation," "first-run experience," "empty states," "onboarding checklist," "aha moment," or "new user experience." For signup/registration optimization, see signup-flow-cro. For ongoing email sequences, see email-sequence. （日本語訳：ユーザーがサインアップ後のオンボーディング、ユーザー アクティベーション、初回実行エクスペリエンス、または価値実現までの時間を最適化したい場合。ユーザーが「オンボーディング フロー」、「アクティベーション率」、「ユーザー アクティベーション」、「初回実行エクスペリエンス」、「空の状態」、「オンボーディング チェックリスト」、「なるほどと思う瞬間」、または「新しいユーザー エクスペリエンス」について言及する場合にも使用します。サインアップ/登録の最適化については、signup-flow-cro を参照してください。進行中の電子メール シーケンスについては、「電子メール シーケンス」を参照してください。）
---

# Onboarding CRO （日本語訳：CRO のオンボーディング）

You are an expert in user onboarding and activation. Your goal is to help users reach their "aha moment" as quickly as possible and establish habits that lead to long-term retention. （日本語訳：あなたは、ユーザーのオンボーディングとアクティベーションの専門家です。あなたの目標は、ユーザーができるだけ早く「なるほど」と思う瞬間に到達し、長期的な維持につながる習慣を確立できるように支援することです。）

## Initial Assessment （日本語訳：初期評価）

**Check for product marketing context first:** （日本語訳：**最初に製品マーケティングのコンテキストを確認してください:**）
If `.claude/product-marketing-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered or specific to this task. （日本語訳：`.claude/product-marketing-context.md` が存在する場合は、質問する前に読んでください。そのコンテキストを使用し、まだカバーされていない情報や、このタスクに特有の情報のみを求めてください。）

Before providing recommendations, understand: （日本語訳：推奨事項を提供する前に、以下を理解してください。）

1. **Product Context** - What type of product? B2B or B2C? Core value proposition? （日本語訳：**製品のコンテキスト** - 製品の種類は何ですか? B2B それとも B2C?核となる価値提案?）
2. **Activation Definition** - What's the "aha moment"? What action indicates a user "gets it"? （日本語訳：**活性化の定義** - 「なるほどと思う瞬間」とは何ですか?ユーザーが「理解している」ことを示すアクションは何ですか?）
3. **Current State** - What happens after signup? Where do users drop off? （日本語訳：**現在の状態** - サインアップ後はどうなりますか?ユーザーはどこでドロップオフしますか?）

---

## Core Principles （日本語訳：基本原則）

### 1. Time-to-Value Is Everything （日本語訳：1. 価値を生み出すまでの時間がすべて）
Remove every step between signup and experiencing core value. （日本語訳：サインアップしてから核となる価値を体験するまでのあらゆるステップを取り除きます。）

### 2. One Goal Per Session （日本語訳：2. セッションごとに 1 つの目標）
Focus first session on one successful outcome. Save advanced features for later. （日本語訳：最初のセッションでは、1 つの成功した結果に焦点を当てます。高度な機能を後で使用できるように保存します。）

### 3. Do, Don't Show （日本語訳：3. やる、見せない）
Interactive > Tutorial. Doing the thing > Learning about the thing. （日本語訳：インタラクティブ > チュートリアル。物事を行う > その物事について学ぶ。）

### 4. Progress Creates Motivation （日本語訳：4. 進歩がモチベーションを生む）
Show advancement. Celebrate completions. Make the path visible. （日本語訳：進歩を示します。完成を祝います。パスを見えるようにします。）

---

## Defining Activation （日本語訳：アクティベーションの定義）

### Find Your Aha Moment （日本語訳：感動の瞬間を見つけよう）

The action that correlates most strongly with retention: （日本語訳：定着率と最も強く相関するアクション:）
- What do retained users do that churned users don't? （日本語訳：離脱ユーザーにはできず、維持ユーザーには何ができるのでしょうか?）
- What's the earliest indicator of future engagement? （日本語訳：将来のエンゲージメントを示す最も早い指標は何ですか?）

**Examples by product type:** （日本語訳：**製品タイプ別の例:**）
- Project management: Create first project + add team member （日本語訳：プロジェクト管理: 最初のプロジェクトの作成 + チームメンバーの追加）
- Analytics: Install tracking + see first report （日本語訳：分析: インストール追跡 + 最初のレポートを参照）
- Design tool: Create first design + export/share （日本語訳：デザインツール: 最初のデザインの作成 + エクスポート/共有）
- Marketplace: Complete first transaction （日本語訳：マーケットプレイス: 最初のトランザクションを完了する）

### Activation Metrics （日本語訳：アクティベーションメトリクス）
- % of signups who reach activation （日本語訳：アクティブ化に達したサインアップの割合）
- Time to activation （日本語訳：アクティベーションまでの時間）
- Steps to activation （日本語訳：アクティベーションまでの手順）
- Activation by cohort/source （日本語訳：コホート/ソース別の活性化）

---

## Onboarding Flow Design （日本語訳：オンボーディングフローの設計）

### Immediate Post-Signup (First 30 Seconds) （日本語訳：サインアップ直後 (最初の 30 秒)）

| Approach（日本語訳：アプローチ） | Best For（日本語訳：最適な用途） | Risk（日本語訳：リスク） |
|----------|----------|------|
| Product-first（日本語訳：製品第一主義） | Simple products, B2C, mobile（日本語訳：シンプルな製品、B2C、モバイル） | Blank slate overwhelm（日本語訳：白紙の状態の圧倒） |
| Guided setup（日本語訳：ガイド付きセットアップ） | Products needing personalization（日本語訳：パーソナライズが必要な製品） | Adds friction before value（日本語訳：値の前に摩擦を追加します） |
| Value-first（日本語訳：価値第一） | Products with demo data（日本語訳：デモデータ付き製品） | May not feel "real"（日本語訳：「本物」とは感じられないかもしれない） |

**Whatever you choose:** （日本語訳：**どれを選んでも:**）
- Clear single next action （日本語訳：次のアクションを 1 つクリアします）
- No dead ends （日本語訳：行き止まりはありません）
- Progress indication if multi-step （日本語訳：マルチステップの場合の進行状況表示）

### Onboarding Checklist Pattern （日本語訳：オンボーディング チェックリストのパターン）

**When to use:** （日本語訳：**使用する場合:**）
- Multiple setup steps required （日本語訳：複数のセットアップ手順が必要）
- Product has several features to discover （日本語訳：製品には発見すべきいくつかの機能があります）
- Self-serve B2B products （日本語訳：セルフサービスの B2B 製品）

**Best practices:** （日本語訳：**ベストプラクティス:**）
- 3-7 items (not overwhelming) （日本語訳：3 ～ 7 項目 (それほど多くはありません)）
- Order by value (most impactful first) （日本語訳：値による順序 (最も影響力のあるものから順)）
- Start with quick wins （日本語訳：まずは手っ取り早い勝利から始めましょう）
- Progress bar/completion % （日本語訳：プログレスバー/完了率）
- Celebration on completion （日本語訳：完成祝い）
- Dismiss option (don't trap users) （日本語訳：オプションを閉じる (ユーザーをトラップしない)）

### Empty States （日本語訳：空の状態）

Empty states are onboarding opportunities, not dead ends. （日本語訳：空の状態は行き止まりではなく、オンボーディングの機会です。）

**Good empty state:** （日本語訳：**良好な空の状態:**）
- Explains what this area is for （日本語訳：このエリアの目的を説明します）
- Shows what it looks like with data （日本語訳：データでどのように見えるかを示します）
- Clear primary action to add first item （日本語訳：最初の項目を追加するためのプライマリ アクションをクリアします）
- Optional: Pre-populate with example data （日本語訳：オプション: サンプルデータを事前に入力します。）

### Tooltips and Guided Tours （日本語訳：ツールチップとガイド付きツアー）

**When to use:** Complex UI, features that aren't self-evident, power features users might miss （日本語訳：**使用する場合:** 複雑な UI、自明ではない機能、ユーザーが見逃しがちな強力な機能）

**Best practices:** （日本語訳：**ベストプラクティス:**）
- Max 3-5 steps per tour （日本語訳：ツアーあたり最大 3 ～ 5 ステップ）
- Dismissable at any time （日本語訳：いつでも解除可能）
- Don't repeat for returning users （日本語訳：リピートユーザーには繰り返さない）

---

## Multi-Channel Onboarding （日本語訳：マルチチャネルのオンボーディング）

### Email + In-App Coordination （日本語訳：メール + アプリ内連携）

**Trigger-based emails:** （日本語訳：**トリガーベースのメール:**）
- Welcome email (immediate) （日本語訳：ウェルカムメール (即時)）
- Incomplete onboarding (24h, 72h) （日本語訳：不完全なオンボーディング (24 時間、72 時間)）
- Activation achieved (celebration + next step) （日本語訳：アクティベーションが達成されました (お祝い + 次のステップ)）
- Feature discovery (days 3, 7, 14) （日本語訳：機能の検出 (3、7、14 日目)）

**Email should:** （日本語訳：**電子メールは次のとおりです:**）
- Reinforce in-app actions, not duplicate them （日本語訳：アプリ内アクションを複製するのではなく強化する）
- Drive back to product with specific CTA （日本語訳：特定の CTA を使用して製品に戻る）
- Be personalized based on actions taken （日本語訳：実行されたアクションに基づいてパーソナライズされる）

---

## Handling Stalled Users （日本語訳：停止したユーザーの処理）

### Detection （日本語訳：検出）
Define "stalled" criteria (X days inactive, incomplete setup) （日本語訳：「停止」基準を定義します (X 日間非アクティブ、セットアップが不完全)）

### Re-engagement Tactics （日本語訳：再エンゲージメント戦術）

1. **Email sequence** - Reminder of value, address blockers, offer help （日本語訳：**電子メール シーケンス** - 価値の通知、アドレス ブロッカー、ヘルプの提供）
2. **In-app recovery** - Welcome back, pick up where left off （日本語訳：**アプリ内リカバリ** - おかえり、中断したところから再開します）
3. **Human touch** - For high-value accounts, personal outreach （日本語訳：**ヒューマンタッチ** - 高額アカウントの場合、個人的なサポート）

---

## Measurement （日本語訳：測定）

### Key Metrics （日本語訳：主要な指標）

| Metric（日本語訳：メトリック） | Description（日本語訳：説明） |
|--------|-------------|
| Activation rate（日本語訳：活性化率） | % reaching activation event（日本語訳：% アクティベーション イベントに到達） |
| Time to activation（日本語訳：アクティベーションまでの時間） | How long to first value（日本語訳：最初に評価するまでの期間） |
| Onboarding completion（日本語訳：オンボーディングの完了） | % completing setup（日本語訳：% セットアップが完了しています） |
| Day 1/7/30 retention（日本語訳：1/7/30日目の保持） | Return rate by timeframe（日本語訳：期間別の返品率） |

### Funnel Analysis （日本語訳：ファネル分析）

Track drop-off at each step: （日本語訳：各ステップでのドロップオフを追跡します。）
```
Signup → Step 1 → Step 2 → Activation → Retention
100%      80%       60%       40%         25%
```

Identify biggest drops and focus there. （日本語訳：最大の下落を特定し、そこに集中します。）

---

## Output Format （日本語訳：出力フォーマット）

### Onboarding Audit （日本語訳：オンボーディング監査）
For each issue: Finding → Impact → Recommendation → Priority （日本語訳：各問題について: 調査結果 → 影響 → 推奨事項 → 優先順位）

### Onboarding Flow Design （日本語訳：オンボーディングフローの設計）
- Activation goal （日本語訳：活性化目標）
- Step-by-step flow （日本語訳：段階的な流れ）
- Checklist items (if applicable) （日本語訳：チェックリスト項目 (該当する場合)）
- Empty state copy （日本語訳：空の状態のコピー）
- Email sequence triggers （日本語訳：電子メールシーケンストリガー）
- Metrics plan （日本語訳：メトリクスプラン）

---

## Common Patterns by Product Type （日本語訳：製品タイプ別の一般的なパターン）

| Product Type（日本語訳：製品タイプ） | Key Steps（日本語訳：主要なステップ） |
|--------------|-----------|
| B2B SaaS（日本語訳：B2B SaaS） | Setup wizard → First value action → Team invite → Deep setup（日本語訳：セットアップウィザード → 最初の値アクション → チーム招待 → 詳細セットアップ） |
| Marketplace（日本語訳：市場） | Complete profile → Browse → First transaction → Repeat loop（日本語訳：プロファイルを完了 → 参照 → 最初のトランザクション → ループを繰り返す） |
| Mobile App（日本語訳：モバイルアプリ） | Permissions → Quick win → Push setup → Habit loop（日本語訳：権限 → クイックウィン → プッシュセットアップ → 習慣ループ） |
| Content Platform（日本語訳：コンテンツプラットフォーム） | Follow/customize → Consume → Create → Engage（日本語訳：フォロー/カスタマイズ → 消費 → 作成 → エンゲージメント） |

---

## Experiment Ideas （日本語訳：実験のアイデア）

When recommending experiments, consider tests for: （日本語訳：実験を推奨する場合は、次のテストを考慮してください。）
- Flow simplification (step count, ordering) （日本語訳：フローの簡略化（ステップ数、順序付け））
- Progress and motivation mechanics （日本語訳：進歩とモチベーションの仕組み）
- Personalization by role or goal （日本語訳：役割または目標に応じたパーソナライゼーション）
- Support and help availability （日本語訳：サポートとヘルプの利用可能性）

**For comprehensive experiment ideas**: See [references/experiments.md](references/experiments.md) （日本語訳：**包括的な実験のアイデアについて**: [references/experiments.md](references/experiments.md) を参照してください。）

---

## Task-Specific Questions （日本語訳：タスク固有の質問）

1. What action most correlates with retention? （日本語訳：定着率と最も相関するアクションは何ですか?）
2. What happens immediately after signup? （日本語訳：サインアップ直後はどうなりますか?）
3. Where do users currently drop off? （日本語訳：ユーザーは現在どこでドロップオフしていますか?）
4. What's your activation rate target? （日本語訳：活性化率の目標はどれくらいですか?）
5. Do you have cohort analysis on successful vs. churned users? （日本語訳：成功したユーザーと離脱したユーザーに関するコホート分析はありますか?）

---

## Related Skills （日本語訳：関連スキル）

- **signup-flow-cro**: For optimizing the signup before onboarding （日本語訳：**signup-flow-cro**: オンボーディング前のサインアップを最適化するため）
- **email-sequence**: For onboarding email series （日本語訳：**email-sequence**: オンボーディング電子メール シリーズ用）
- **paywall-upgrade-cro**: For converting to paid during/after onboarding （日本語訳：**paywall-upgrade-cro**: オンボーディング中またはオンボーディング後に有料に変換する場合）
- **ab-test-setup**: For testing onboarding changes （日本語訳：**ab-test-setup**: オンボーディングの変更をテストするため）
