# Marketing Skills for Claude Code （クロード・コードのマーケティング・スキル）

A collection of AI agent skills focused on marketing tasks. Built for technical marketers and founders who want Claude Code (or similar AI coding assistants) to help with conversion optimization, copywriting, SEO, analytics, and growth engineering. （マーケティングタスクに焦点を当てた AI エージェントのスキルのコレクション。 Claude Code (または同様の AI コーディング アシスタント) をコンバージョンの最適化、コピーライティング、SEO、分析、成長エンジニアリングに役立てたいと考えているテクニカル マーケティング担当者や創業者向けに構築されています。）

Built by [Corey Haines](https://corey.co?ref=marketingskills). Need hands-on help? Check out [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — Corey's agency for conversion optimization, landing pages, and growth strategy. Want to learn more about marketing? Subscribe to [Swipe Files](https://swipefiles.com?ref=marketingskills). （[Corey Haines](https://corey.co?ref=marketingskills). による実践的なサポートが必要ですか? [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — コンバージョンの最適化、ランディング ページ、および成長戦略を担当する Corey の代理店です。マーケティングについてさらに詳しく知りたいですか? [Swipe Files](https://swipefiles.com?ref=marketingskills).) を購読してください)）

New to the terminal and coding agents? Check out the companion guide [Coding for Marketers](https://codingformarketers.com?ref=marketingskills). （ターミナルとコーディング エージェントは初めてですか?関連ガイド [マーケティング担当者のためのコーディング](https://codingformarketers.com?ref=marketingskills).) をご覧ください。）

**Contributions welcome!** Found a way to improve a skill or have a new one to add? [Open a PR](#contributing). （**貢献は大歓迎です!** スキルを向上させる方法、または新しいスキルを追加する方法は見つかりましたか? [PR を開く](#contributing)。）

## What are Skills? （スキルとは何ですか?）

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add these to your project, Claude Code can recognize when you're working on a marketing task and apply the right frameworks and best practices. （スキルは、AI エージェントに特定のタスクの専門知識とワークフローを提供するマークダウン ファイルです。これらをプロジェクトに追加すると、Claude Code はマーケティング タスクに取り組んでいることを認識し、適切なフレームワークとベスト プラクティスを適用できます。）

## Available Skills （利用可能なスキル）

<!-- SKILLS:START --> （<!-- スキル:スタート -->）
| Skill（スキル） | Description（説明） |
|-------|-------------|
| [ab-test-setup](skills/ab-test-setup/)（Error 500 (Server Error)!!1500.That’s an error.There was an error. Please try again later.That’s all we know.） | When the user wants to plan, design, or implement an A/B test or experiment. Also use when the user mentions "A/B...（ユーザーが A/B テストや実験を計画、設計、または実装したい場合。ユーザーが「A/B...」と言及する場合にも使用します。） |
| [analytics-tracking](skills/analytics-tracking/)（[分析-追跡](スキル/分析-追跡/)） | When the user wants to set up, improve, or audit analytics tracking and measurement. Also use when the user mentions...（ユーザーが分析の追跡と測定を設定、改善、または監査したい場合。 Also use when the user mentions...） |
| [competitor-alternatives](skills/competitor-alternatives/)（[競合他社の代替案](スキル/競合他社の代替案/)） | When the user wants to create competitor comparison or alternative pages for SEO and sales enablement. Also use when...（ユーザーが SEO やセールスイネーブルメントのために競合他社の比較ページや代替ページを作成したい場合。こんなときにも使います...） |
| [content-strategy](skills/content-strategy/)（[コンテンツ戦略](スキル/コンテンツ戦略/)） | When the user wants to plan a content strategy, decide what content to create, or figure out what topics to cover. Also...（ユーザーがコンテンツ戦略を計画する場合は、どのようなコンテンツを作成するかを決定するか、どのようなトピックを取り上げるかを決定します。また...） |
| [copy-editing](skills/copy-editing/)（[コピー編集](スキル/コピー編集/)） | When the user wants to edit, review, or improve existing marketing copy. Also use when the user mentions 'edit this...（ユーザーが既存のマーケティング コピーを編集、レビュー、または改善したい場合。ユーザーが「これを編集...」と言及した場合にも使用します。） |
| [copywriting](skills/copywriting/)（[コピーライティング](スキル/コピーライティング/)） | When the user wants to write, rewrite, or improve marketing copy for any page — including homepage, landing pages,...（ユーザーがホームページ、ランディング ページなど、あらゆるページのマーケティング コピーを作成、書き直し、または改善したい場合。） |
| [email-sequence](skills/email-sequence/)（[電子メールシーケンス](スキル/電子メールシーケンス/)） | When the user wants to create or optimize an email sequence, drip campaign, automated email flow, or lifecycle email...（ユーザーが電子メール シーケンス、ドリップ キャンペーン、自動電子メール フロー、またはライフサイクル電子メールを作成または最適化したい場合...） |
| [form-cro](skills/form-cro/)（[フォームクロ](スキル/フォームクロ/)） | When the user wants to optimize any form that is NOT signup/registration — including lead capture forms, contact forms,...（ユーザーが、リード獲得フォーム、お問い合わせフォームなど、サインアップ/登録以外のフォームを最適化したい場合。） |
| [free-tool-strategy](skills/free-tool-strategy/)（[無料ツール-戦略](スキル/無料ツール-戦略/)） | When the user wants to plan, evaluate, or build a free tool for marketing purposes — lead generation, SEO value, or...（ユーザーが見込み顧客の発掘、SEO 価値などのマーケティング目的で無料のツールを計画、評価、構築したい場合。） |
| [launch-strategy](skills/launch-strategy/)（[起動-戦略](スキル/起動-戦略/)） | When the user wants to plan a product launch, feature announcement, or release strategy. Also use when the user...（ユーザーが製品の発売、機能の発表、またはリリース戦略を計画したい場合。ユーザーが次の場合にも使用します...） |
| [marketing-ideas](skills/marketing-ideas/)（[マーケティング アイデア](スキル/マーケティング アイデア/)） | When the user needs marketing ideas, inspiration, or strategies for their SaaS or software product. Also use when the...（ユーザーが SaaS またはソフトウェア製品のマーケティング アイデア、インスピレーション、または戦略を必要としている場合。こんなときにも使えます...） |
| [marketing-psychology](skills/marketing-psychology/)（[マーケティング心理学](スキル/マーケティング心理学/)） | When the user wants to apply psychological principles, mental models, or behavioral science to marketing. Also use when...（ユーザーが心理学的原理、メンタルモデル、または行動科学をマーケティングに適用したい場合。こんなときにも使います...） |
| [onboarding-cro](skills/onboarding-cro/)（[onboarding-cro](スキル/onboarding-cro/)） | When the user wants to optimize post-signup onboarding, user activation, first-run experience, or time-to-value. Also...（ユーザーがサインアップ後のオンボーディング、ユーザー アクティベーション、初回実行エクスペリエンス、または価値実現までの時間を最適化したい場合。また...） |
| [page-cro](skills/page-cro/)（[page-cro](スキル/page-cro/)） | When the user wants to optimize, improve, or increase conversions on any marketing page — including homepage, landing...（ユーザーがホームページ、ランディングなどのマーケティング ページでコンバージョンを最適化、改善、または増加させたい場合。） |
| [paid-ads](skills/paid-ads/)（[有料広告](スキル/有料広告/)） | When the user wants help with paid advertising campaigns on Google Ads, Meta (Facebook/Instagram), LinkedIn, Twitter/X,...（ユーザーが Google 広告、Meta (Facebook/Instagram)、LinkedIn、Twitter/X などの有料広告キャンペーンに関するサポートを必要としている場合。） |
| [paywall-upgrade-cro](skills/paywall-upgrade-cro/)（[paywall-upgrade-cro](スキル/paywall-upgrade-cro/)） | When the user wants to create or optimize in-app paywalls, upgrade screens, upsell modals, or feature gates. Also use...（ユーザーがアプリ内ペイウォールを作成または最適化する場合、画面をアップグレードする場合、モーダルをアップセルする場合、または機能ゲートを使用する場合。また、使用...） |
| [popup-cro](skills/popup-cro/)（[ポップアップクロ](スキル/ポップアップクロ/)） | When the user wants to create or optimize popups, modals, overlays, slide-ins, or banners for conversion purposes. Also...（ユーザーが変換を目的としてポップアップ、モーダル、オーバーレイ、スライドイン、またはバナーを作成または最適化したい場合。また...） |
| [pricing-strategy](skills/pricing-strategy/)（[価格設定戦略](スキル/価格設定戦略/)） | When the user wants help with pricing decisions, packaging, or monetization strategy. Also use when the user mentions...（ユーザーが価格決定、パッケージング、または収益化戦略についてサポートを必要とする場合。ユーザーが次のように言及する場合にも使用します...） |
| [product-marketing-context](skills/product-marketing-context/)（[プロダクト マーケティング コンテキスト](スキル/プロダクト マーケティング コンテキスト/)） | When the user wants to create or update their product marketing context document. Also use when the user mentions...（ユーザーが製品マーケティング コンテキスト ドキュメントを作成または更新したい場合。ユーザーが次のように言及する場合にも使用します...） |
| [programmatic-seo](skills/programmatic-seo/)（[プログラマティック-seo](スキル/プログラマティック-seo/)） | When the user wants to create SEO-driven pages at scale using templates and data. Also use when the user mentions...（ユーザーがテンプレートとデータを使用して SEO 主導のページを大規模に作成したい場合。ユーザーが次のように言及する場合にも使用します...） |
| [referral-program](skills/referral-program/)（[紹介プログラム](スキル/紹介プログラム/)） | When the user wants to create, optimize, or analyze a referral program, affiliate program, or word-of-mouth strategy....（ユーザーが紹介プログラム、アフィリエイト プログラム、または口コミ戦略を作成、最適化、または分析したい場合...） |
| [schema-markup](skills/schema-markup/)（[スキーママークアップ](スキル/スキーママークアップ/)） | When the user wants to add, fix, or optimize schema markup and structured data on their site. Also use when the user...（ユーザーがサイト上のスキーマ マークアップと構造化データを追加、修正、または最適化したい場合。ユーザーが次の場合にも使用します...） |
| [seo-audit](skills/seo-audit/)（[seo-audit](スキル/seo-audit/)） | When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions "SEO...（ユーザーがサイトの SEO の問題を監査、レビュー、または診断したい場合。ユーザーが「SEO...」と言及する場合にも使用します。） |
| [signup-flow-cro](skills/signup-flow-cro/)（[サインアップフロー-cro](スキル/サインアップフロー-cro/)） | When the user wants to optimize signup, registration, account creation, or trial activation flows. Also use when the...（ユーザーがサインアップ、登録、アカウント作成、または試用版アクティベーションのフローを最適化したい場合。こんなときにも使えます...） |
| [social-content](skills/social-content/)（[ソーシャルコンテンツ](スキル/ソーシャルコンテンツ/)） | When the user wants help creating, scheduling, or optimizing social media content for LinkedIn, Twitter/X, Instagram,...（ユーザーが LinkedIn、Twitter/X、Instagram などのソーシャル メディア コンテンツの作成、スケジュール、最適化についてサポートを求めている場合。） |
<!-- SKILLS:END --> （<!-- スキル:終了 -->）

## Installation （インストール）

### Option 1: CLI Install (Recommended) （オプション 1: CLI インストール (推奨)）

Use [npx skills](https://github.com/vercel-labs/skills) to install skills directly: （[npx skill](https://github.com/vercel-labs/skills) を使用してスキルを直接インストールします。）

```bash
# Install all skills
npx skills add coreyhaines31/marketingskills

# Install specific skills
npx skills add coreyhaines31/marketingskills --skill page-cro copywriting

# List available skills
npx skills add coreyhaines31/marketingskills --list
```

This automatically installs to your `.claude/skills/` directory. （これにより、`.claude/skills/` ディレクトリに自動的にインストールされます。）

### Option 2: Claude Code Plugin （オプション 2: クロード コード プラグイン）

Install via Claude Code's built-in plugin system: （Claude Code の組み込みプラグイン システム経由でインストールします。）

```bash
# Add the marketplace
/plugin marketplace add coreyhaines31/marketingskills

# Install all marketing skills
/plugin install marketing-skills
```

### Option 3: Clone and Copy （オプション 3: クローンとコピー）

Clone the entire repo and copy the skills folder: （リポジトリ全体のクローンを作成し、スキル フォルダーをコピーします。）

```bash
git clone https://github.com/coreyhaines31/marketingskills.git
cp -r marketingskills/skills/* .claude/skills/
```

### Option 4: Git Submodule （オプション 4: Git サブモジュール）

Add as a submodule for easy updates: （簡単に更新できるようにサブモジュールとして追加します。）

```bash
git submodule add https://github.com/coreyhaines31/marketingskills.git .claude/marketingskills
```

Then reference skills from `.claude/marketingskills/skills/`. （次に、`.claude/marketingskills/skills/` からスキルを参照します。）

### Option 5: Fork and Customize （オプション 5: フォークしてカスタマイズする）

1. Fork this repository （このリポジトリをフォークする）
2. Customize skills for your specific needs （特定のニーズに合わせてスキルをカスタマイズする）
3. Clone your fork into your projects （フォークのクローンをプロジェクトに作成します）

### Option 6: SkillKit (Multi-Agent) （オプション 6: SkillKit (マルチエージェント)）

Use [SkillKit](https://github.com/rohitg00/skillkit) to install skills across multiple AI agents (Claude Code, Cursor, Copilot, etc.): （[SkillKit](https://github.com/rohitg00/skillkit) を使用して、複数の AI エージェント (クロード コード、カーソル、コパイロットなど) にスキルをインストールします。）

```bash
# Install all skills
npx skillkit install coreyhaines31/marketingskills

# Install specific skills
npx skillkit install coreyhaines31/marketingskills --skill page-cro copywriting

# List available skills
npx skillkit install coreyhaines31/marketingskills --list
```

## Usage （使用法）

Once installed, just ask Claude Code to help with marketing tasks: （インストールしたら、Claude Code にマーケティング タスクの支援を依頼するだけです。）

```
"Help me optimize this landing page for conversions"
→ Uses page-cro skill

"Write homepage copy for my SaaS"
→ Uses copywriting skill

"Set up GA4 tracking for signups"
→ Uses analytics-tracking skill

"Create a 5-email welcome sequence"
→ Uses email-sequence skill
```

You can also invoke skills directly: （スキルを直接呼び出すこともできます。）

```
/page-cro
/email-sequence
/seo-audit
```

## Skill Categories （スキルカテゴリー）

### Conversion Optimization （変換の最適化）
- `page-cro` - Any marketing page （`page-cro` - 任意のマーケティング ページ）
- `signup-flow-cro` - Registration flows （`signup-flow-cro` - 登録フロー）
- `onboarding-cro` - Post-signup activation （`onboarding-cro` - サインアップ後のアクティベーション）
- `form-cro` - Lead capture forms （`form-cro` - リード獲得フォーム）
- `popup-cro` - Modals and overlays （`popup-cro` - モーダルとオーバーレイ）
- `paywall-upgrade-cro` - In-app upgrade moments （`paywall-upgrade-cro` - アプリ内アップグレードの瞬間）

### Content & Copy （コンテンツとコピー）
- `copywriting` - Marketing page copy （`copywriting` - マーケティング ページのコピー）
- `copy-editing` - Edit and polish existing copy （`copy-editing` - 既存のコピーを編集して磨きをかける）
- `email-sequence` - Automated email flows （`email-sequence` - 自動化された電子メール フロー）
- `social-content` - Social media content （`social-content` - ソーシャル メディア コンテンツ）

### SEO & Discovery （SEOと発見）
- `seo-audit` - Technical and on-page SEO （`seo-audit` - 技術的なSEOとページ上のSEO）
- `programmatic-seo` - Scaled page generation （`programmatic-seo` - スケーリングされたページの生成）
- `competitor-alternatives` - Comparison and alternative pages （`competitor-alternatives` - 比較ページと代替ページ）
- `schema-markup` - Structured data （`schema-markup` - 構造化データ）

### Paid & Distribution （有料＆配信）
- `paid-ads` - Google, Meta, LinkedIn ad campaigns （`paid-ads` - Google、Meta、LinkedIn の広告キャンペーン）
- `social-content` - Social media scheduling and strategy （`social-content` - ソーシャル メディアのスケジュールと戦略）

### Measurement & Testing （測定と試験）
- `analytics-tracking` - Event tracking setup （`analytics-tracking` - イベント追跡のセットアップ）
- `ab-test-setup` - Experiment design （`ab-test-setup` - 実験計画）

### Growth Engineering （成長工学）
- `free-tool-strategy` - Marketing tools and calculators （`free-tool-strategy` - マーケティング ツールと計算機）
- `referral-program` - Referral and affiliate programs （`referral-program` - 紹介プログラムとアフィリエイト プログラム）

### Strategy & Monetization （戦略と収益化）
- `marketing-ideas` - 140 SaaS marketing ideas （`marketing-ideas` - 140 の SaaS マーケティング アイデア）
- `marketing-psychology` - Mental models and psychology （`marketing-psychology` - メンタルモデルと心理学）
- `launch-strategy` - Product launches and announcements （`launch-strategy` - 製品の発売と発表）
- `pricing-strategy` - Pricing, packaging, and monetization （`pricing-strategy` - 価格設定、パッケージ化、収益化）

## Contributing （貢献する）

Found a way to improve a skill? Have a new skill to suggest? PRs and issues welcome! （スキルを向上させる方法は見つかりましたか?提案する新しいスキルはありますか? PRや話題も大歓迎！）

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding or improving skills. （スキルの追加または改善に関するガイドラインについては、[CONTRIBUTING.md](CONTRIBUTING.md) を参照してください。）

## License （ライセンス）

[MIT](LICENSE) - Use these however you want. （[MIT](ライセンス) - これらを自由に使用してください。）
