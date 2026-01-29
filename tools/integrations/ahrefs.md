# Ahrefs （日本語訳：アーレフス）

SEO toolset for backlink analysis, keyword research, and competitive research. （日本語訳：バックリンク分析、キーワード調査、競合調査のための SEO ツールセット。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for Site Explorer, Keywords Explorer（日本語訳：サイト エクスプローラー、キーワード エクスプローラー用の REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | API-only（日本語訳：APIのみ） |

## Authentication （日本語訳：認証）

- **Type**: API Token （日本語訳：**タイプ**: API トークン）
- **Header**: `Authorization: Bearer {api_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {api_token}`）
- **Get token**: Account Settings > API in Ahrefs dashboard （日本語訳：**トークンの取得**: Ahrefs ダッシュボードの [アカウント設定] > [API]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Domain rating （日本語訳：ドメインの評価）

```bash
GET https://api.ahrefs.com/v3/site-explorer/domain-rating?target=example.com

Authorization: Bearer {api_token}
```

### Backlinks overview （日本語訳：バックリンクの概要）

```bash
GET https://api.ahrefs.com/v3/site-explorer/backlinks-stats?target=example.com&mode=domain

Authorization: Bearer {api_token}
```

### Referring domains （日本語訳：参照元ドメイン）

```bash
GET https://api.ahrefs.com/v3/site-explorer/refdomains?target=example.com&mode=domain&limit=100

Authorization: Bearer {api_token}
```

### Backlinks list （日本語訳：バックリンクリスト）

```bash
GET https://api.ahrefs.com/v3/site-explorer/backlinks?target=example.com&mode=domain&limit=100

Authorization: Bearer {api_token}
```

### Organic keywords （日本語訳：オーガニックキーワード）

```bash
GET https://api.ahrefs.com/v3/site-explorer/organic-keywords?target=example.com&mode=domain&country=us&limit=100

Authorization: Bearer {api_token}
```

### Top pages （日本語訳：トップページ）

```bash
GET https://api.ahrefs.com/v3/site-explorer/top-pages?target=example.com&mode=domain&country=us&limit=50

Authorization: Bearer {api_token}
```

### Keyword overview （日本語訳：キーワードの概要）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/overview?keywords=keyword1,keyword2&country=us

Authorization: Bearer {api_token}
```

### Keyword suggestions （日本語訳：キーワードの提案）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/matching-terms?keyword=seed+keyword&country=us&limit=100

Authorization: Bearer {api_token}
```

### SERP overview （日本語訳：SERPの概要）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/serp-overview?keyword=target+keyword&country=us

Authorization: Bearer {api_token}
```

## Key Metrics （日本語訳：主要な指標）

### Domain Metrics （日本語訳：ドメインメトリクス）
- `domain_rating` - Domain Rating (DR) （日本語訳：`domain_rating` - ドメイン評価 (DR)）
- `ahrefs_rank` - Ahrefs Rank （日本語訳：`ahrefs_rank` - Ahrefs ランク）
- `referring_domains` - Referring domains count （日本語訳：`referring_domains` - 参照元ドメインの数）
- `backlinks` - Total backlinks （日本語訳：`backlinks` - バックリンクの合計数）
- `organic_traffic` - Estimated organic traffic （日本語訳：`organic_traffic` - 推定オーガニックトラフィック）

### Keyword Metrics （日本語訳：キーワード指標）
- `volume` - Monthly search volume （日本語訳：`volume` - 月間検索ボリューム）
- `keyword_difficulty` - KD score (0-100) （日本語訳：`keyword_difficulty` - KD スコア (0-100)）
- `cpc` - Cost per click （日本語訳：`cpc` - クリックあたりのコスト）
- `clicks` - Estimated monthly clicks （日本語訳：`clicks` - 推定月間クリック数）
- `global_volume` - Global search volume （日本語訳：`global_volume` - グローバル検索ボリューム）

### Backlink Fields （日本語訳：バックリンクフィールド）
- `url_from` - Source URL （日本語訳：`url_from` - ソース URL）
- `url_to` - Target URL （日本語訳：`url_to` - ターゲット URL）
- `anchor` - Anchor text （日本語訳：`anchor` - アンカーテキスト）
- `domain_rating_source` - Source DR （日本語訳：`domain_rating_source` - ソース DR）
- `first_seen` - First discovery date （日本語訳：`first_seen` - 最初の発見日）

## Modes （日本語訳：モード）

- `domain` - Entire domain （日本語訳：`domain` - ドメイン全体）
- `subdomains` - Domain + subdomains （日本語訳：`subdomains` - ドメイン + サブドメイン）
- `prefix` - URL prefix （日本語訳：`prefix` - URL プレフィックス）
- `exact` - Exact URL （日本語訳：`exact` - 正確な URL）

## When to Use （日本語訳：いつ使用するか）

- Backlink analysis （日本語訳：バックリンク分析）
- Link building research （日本語訳：リンクビルディングの調査）
- Keyword research （日本語訳：キーワード調査）
- Competitive analysis （日本語訳：競合分析）
- Content gap analysis （日本語訳：コンテンツギャップ分析）
- Site audits （日本語訳：現場監査）

## Rate Limits （日本語訳：レート制限）

- Varies by plan （日本語訳：プランにより異なります）
- 500-5000 rows per request （日本語訳：リクエストあたり 500 ～ 5000 行）

## Relevant Skills （日本語訳：関連するスキル）

- seo-audit （日本語訳：SEO監査）
- content-strategy （日本語訳：コンテンツ戦略）
- competitor-alternatives （日本語訳：競合他社の代替品）
