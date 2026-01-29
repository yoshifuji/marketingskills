# AGENTS.md （日本語訳：エージェント.md）

Guidelines for AI agents working in this repository. （日本語訳：このリポジトリで動作する AI エージェントのガイドライン。）

## Repository Overview （日本語訳：リポジトリの概要）

This repository contains **Agent Skills** for AI agents following the [Agent Skills specification](https://agentskills.io/specification.md). It also serves as a **Claude Code plugin marketplace** via `.claude-plugin/marketplace.json`. （日本語訳：このリポジトリには、[エージェント スキル仕様](https://agentskills.io/specification.md).) に準拠した AI エージェント用の **エージェント スキル** が含まれています。また、`.claude-plugin/marketplace.json` を介して **クロード コード プラグイン マーケットプレイス**としても機能します。）

- **Name**: Marketing Skills （日本語訳：**名前**: マーケティング スキル）
- **GitHub**: [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) （日本語訳：**GitHub**: [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)）
- **Creator**: Corey Haines （日本語訳：**クリエイター**: コーリー・ヘインズ）
- **License**: MIT （日本語訳：**ライセンス**: MIT）

## Repository Structure （日本語訳：リポジトリ構造）

```
marketingskills/
├── .claude-plugin/
│   └── marketplace.json   # Claude Code plugin marketplace manifest
├── skills/                # Agent Skills
│   └── skill-name/
│       └── SKILL.md       # Required skill file
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## Build / Lint / Test Commands （日本語訳：ビルド / lint / テスト コマンド）

**Not applicable** - This is a content-only repository with no executable code. （日本語訳：**該当なし** - これは、実行可能コードを含まないコンテンツのみのリポジトリです。）

Verify manually: （日本語訳：手動で確認します。）
- YAML frontmatter is valid （日本語訳：YAML フロントマターは有効です）
- `name` field matches directory name exactly （日本語訳：`name` フィールドはディレクトリ名と正確に一致します）
- `name` is 1-64 chars, lowercase alphanumeric and hyphens only （日本語訳：`name` は 1 ～ 64 文字、小文字の英数字およびハイフンのみです）
- `description` is 1-1024 characters （日本語訳：`description` は 1 ～ 1024 文字です）

## Agent Skills Specification （日本語訳：エージェントのスキル仕様）

Skills follow the [Agent Skills spec](https://agentskills.io/specification.md). （日本語訳：スキルは [エージェント スキル仕様](https://agentskills.io/specification.md).) に従います。）

### Required Frontmatter （日本語訳：必須のフロントマター）

```yaml
---
name: skill-name
description: What this skill does and when to use it. Include trigger phrases.
---
```

### Frontmatter Field Constraints （日本語訳：フロントマターフィールドの制約）

| Field（日本語訳：分野）         | Required（日本語訳：必須） | Constraints（日本語訳：制約）                                                      |
|---------------|----------|------------------------------------------------------------------|
| `name`（日本語訳：__コード0__）        | Yes（日本語訳：はい）      | 1-64 chars, lowercase `a-z`, numbers, hyphens. Must match dir.（日本語訳：1 ～ 64 文字、小文字の `a-z`、数字、ハイフン。ディレクトリと一致する必要があります。）   |
| `description`（日本語訳：__コード0__） | Yes（日本語訳：はい）      | 1-1024 chars. Describe what it does and when to use it.（日本語訳：1 ～ 1024 文字。それが何をするのか、いつ使用するのかを説明します。）          |
| `license`（日本語訳：__コード0__）     | No（日本語訳：いいえ）       | License name (default: MIT)（日本語訳：ライセンス名 (デフォルト: MIT)）                                      |
| `metadata`（日本語訳：__コード0__）    | No（日本語訳：いいえ）       | Key-value pairs (author, version, etc.)（日本語訳：キーと値のペア (作成者、バージョンなど)）                          |

### Name Field Rules （日本語訳：名前フィールドのルール）

- Lowercase letters, numbers, and hyphens only （日本語訳：小文字、数字、ハイフンのみ）
- Cannot start or end with hyphen （日本語訳：ハイフンで開始または終了することはできません）
- No consecutive hyphens (`--`) （日本語訳：連続したハイフンは使用できません (`--`)）
- Must match parent directory name exactly （日本語訳：親ディレクトリ名と正確に一致する必要があります）

**Valid**: `page-cro`, `email-sequence`, `ab-test-setup` （日本語訳：**有効**: `page-cro`、`email-sequence`、`ab-test-setup`）
**Invalid**: `Page-CRO`, `-page`, `page--cro` （日本語訳：**無効**: `Page-CRO`、`-page`、`page--cro`）

### Optional Skill Directories （日本語訳：オプションのスキルディレクトリ）

```
skills/skill-name/
├── SKILL.md        # Required - main instructions (<500 lines)
├── references/     # Optional - detailed docs loaded on demand
├── scripts/        # Optional - executable code
└── assets/         # Optional - templates, data files
```

## Writing Style Guidelines （日本語訳：書き方のガイドライン）

### Structure （日本語訳：構造）

- Keep `SKILL.md` under 500 lines (move details to `references/`) （日本語訳：`SKILL.md` を 500 行以下に保つ (詳細を `references/` に移動)）
- Use H2 (`##`) for main sections, H3 (`###`) for subsections （日本語訳：メインセクションには H2 (`##`)、サブセクションには H3 (`###`) を使用します。）
- Use bullet points and numbered lists liberally （日本語訳：箇条書きと番号付きリストを自由に使用する）
- Short paragraphs (2-4 sentences max) （日本語訳：短い段落 (最大 2 ～ 4 文)）

### Tone （日本語訳：トーン）

- Direct and instructional （日本語訳：直接的かつ指導的）
- Second person ("You are a conversion rate optimization expert") （日本語訳：2 人目 (「あなたはコンバージョン率最適化の専門家です」)）
- Professional but approachable （日本語訳：プロフェッショナルだけど親しみやすい）

### Formatting （日本語訳：書式設定）

- Bold (`**text**`) for key terms （日本語訳：重要な用語には太字 (`**text**`)）
- Code blocks for examples and templates （日本語訳：例とテンプレートのコードブロック）
- Tables for reference data （日本語訳：参考データの表）
- No excessive emojis （日本語訳：過剰な絵文字は禁止）

### Clarity Principles （日本語訳：明確さの原則）

- Clarity over cleverness （日本語訳：賢さよりも明晰さ）
- Specific over vague （日本語訳：漠然としたものよりも具体的なもの）
- Active voice over passive （日本語訳：パッシブよりもアクティブな音声）
- One idea per section （日本語訳：セクションごとに 1 つのアイデア）

### Description Field Best Practices （日本語訳：説明フィールドのベストプラクティス）

The `description` is critical for skill discovery. Include: （日本語訳：`description` はスキルの発見に重要です。含む：）
1. What the skill does （日本語訳：スキルが何をするのか）
2. When to use it (trigger phrases) （日本語訳：いつ使用するか (トリガーフレーズ)）
3. Related skills for scope boundaries （日本語訳：スコープ境界に関連するスキル）

```yaml
description: When the user wants to optimize conversions on any marketing page. Use when the user says "CRO," "conversion rate optimization," "this page isn't converting." For signup flows, see signup-flow-cro.
```

## Claude Code Plugin （日本語訳：クロードコードプラグイン）

This repo also serves as a plugin marketplace. The manifest at `.claude-plugin/marketplace.json` lists all skills for installation via: （日本語訳：このリポジトリはプラグイン マーケットプレイスとしても機能します。 `.claude-plugin/marketplace.json` のマニフェストには、次の方法でインストールできるすべてのスキルがリストされています。）

```bash
/plugin marketplace add coreyhaines31/marketingskills
/plugin install marketing-skills
```

See [Claude Code plugins documentation](https://code.claude.com/docs/en/plugins.md) for details. （日本語訳：詳細については、[Claude Code プラグインのドキュメント](https://code.claude.com/docs/en/plugins.md)) を参照してください。）

## Git Workflow （日本語訳：Git ワークフロー）

### Branch Naming （日本語訳：ブランチのネーミング）

- New skills: `feature/skill-name` （日本語訳：新しいスキル: `feature/skill-name`）
- Improvements: `fix/skill-name-description` （日本語訳：改善点: `fix/skill-name-description`）
- Documentation: `docs/description` （日本語訳：ドキュメント: `docs/description`）

### Commit Messages （日本語訳：コミットメッセージ）

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification: （日本語訳：[従来のコミット](https://www.conventionalcommits.org/) 仕様:）

- `feat: add skill-name skill` （日本語訳：__コード0__）
- `fix: improve clarity in page-cro` （日本語訳：__コード0__）
- `docs: update README` （日本語訳：__コード0__）

### Pull Request Checklist （日本語訳：プルリクエストのチェックリスト）

- [ ] `name` matches directory name exactly （日本語訳：[ ] `name` はディレクトリ名と完全に一致します）
- [ ] `name` follows naming rules (lowercase, hyphens, no `--`) （日本語訳：[ ] `name` は命名規則に従います (小文字、ハイフン、`--` は不可)）
- [ ] `description` is 1-1024 chars with trigger phrases （日本語訳：[ ] `description` はトリガー フレーズを含む 1 ～ 1024 文字です）
- [ ] `SKILL.md` is under 500 lines （日本語訳：[ ] `SKILL.md` は 500 行未満です）
- [ ] No sensitive data or credentials （日本語訳：[ ] 機密データや認証情報はありません）

## Tool Integrations （日本語訳：ツールの統合）

This repository includes a tools registry for agent-compatible marketing tools. （日本語訳：このリポジトリには、エージェント互換のマーケティング ツールのツール レジストリが含まれています。）

- **Tool discovery**: Read `tools/REGISTRY.md` to see available tools and their capabilities （日本語訳：**ツールの検出**: `tools/REGISTRY.md` を読んで、利用可能なツールとその機能を確認してください。）
- **Integration details**: See `tools/integrations/{tool}.md` for API endpoints, auth, and common operations （日本語訳：**統合の詳細**: API エンドポイント、認証、および一般的な操作については、`tools/integrations/{tool}.md` を参照してください。）
- **MCP-enabled tools**: ga4, stripe, mailchimp, google-ads, resend, zapier （日本語訳：**MCP 対応ツール**: ga4、stripe、mailchimp、google-ads、resend、zapier）

### Registry Structure （日本語訳：レジストリ構造）

```
tools/
├── REGISTRY.md              # Index of all tools with capabilities
└── integrations/            # Detailed integration guides
    ├── ga4.md
    ├── stripe.md
    ├── rewardful.md
    └── ...
```

### When to Use Tools （日本語訳：ツールを使用する場合）

Skills reference relevant tools for implementation. For example: （日本語訳：スキルは、実装に関連するツールを参照します。例えば：）
- `referral-program` skill → rewardful, tolt, dub-co, mention-me guides （日本語訳：`referral-program` スキル → やりがいのある、トルト、ダブコ、メンションミーガイド）
- `analytics-tracking` skill → ga4, mixpanel, segment guides （日本語訳：`analytics-tracking` スキル → ga4、ミックスパネル、セグメントガイド）
- `email-sequence` skill → customer-io, mailchimp, resend guides （日本語訳：`email-sequence` スキル → customer-io、mailchimp、再送信ガイド）
- `paid-ads` skill → google-ads, meta-ads, linkedin-ads guides （日本語訳：`paid-ads` スキル → Google 広告、メタ広告、linkedin 広告ガイド）

## Checking for Updates （日本語訳：アップデートの確認）

When using any skill from this repository: （日本語訳：このリポジトリのスキルを使用する場合:）

1. **Once per session**, on first skill use, check for updates: （日本語訳：**セッションごとに 1 回**、最初のスキル使用時に更新を確認します。）
   - Fetch `VERSIONS.md` from GitHub: https://raw.githubusercontent.com/coreyhaines31/marketingskills/main/VERSIONS.md （日本語訳：GitHub から `VERSIONS.md` を取得します: https://raw.githubusercontent.com/coreyhaines31/marketingskills/main/VERSIONS.md）
   - Compare versions against local skill files （日本語訳：ローカルスキルファイルとバージョンを比較する）

2. **Only prompt if meaningful**: （日本語訳：**意味のある場合のみプロンプトを表示**:）
   - 2 or more skills have updates, OR （日本語訳：2 つ以上のスキルに更新がある、または）
   - Any skill has a major version bump (e.g., 1.x to 2.x) （日本語訳：どのスキルにもメジャー バージョンのバンプがあります (例: 1.x から 2.x)。）

3. **Non-blocking notification** at end of response: （日本語訳：**応答の最後にノンブロッキング通知**:）
   ```
   ---
   Skills update available: X marketing skills have updates.
   Say "update skills" to update automatically, or run `git pull` in your marketingskills folder.
   ```

4. **If user says "update skills"**: （日本語訳：**ユーザーが「スキルを更新する」と言った場合**:）
   - Run `git pull` in the marketingskills directory （日本語訳：Marketingskills ディレクトリで `git pull` を実行します）
   - Confirm what was updated （日本語訳：何が更新されたかを確認する）

## Skill Categories （日本語訳：スキルカテゴリー）

See `README.md` for the current list of skills organized by category. When adding new skills, follow the naming patterns of existing skills in that category. （日本語訳：カテゴリ別に整理されたスキルの現在のリストについては、`README.md` を参照してください。新しいスキルを追加するときは、そのカテゴリ内の既存のスキルの命名パターンに従ってください。）
