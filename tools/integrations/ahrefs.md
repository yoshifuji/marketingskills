# Ahrefs （アーレフス）

SEO toolset for backlink analysis, keyword research, and competitive research. （バックリンク分析、キーワード調査、競合調査のための SEO ツールセット。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for Site Explorer, Keywords Explorer（サイト エクスプローラー、キーワード エクスプローラー用の REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | API-only（APIのみ） |

## Authentication （認証）

- **Type**: API Token （**タイプ**: API トークン）
- **Header**: `Authorization: Bearer {api_token}` （**ヘッダー**: `Authorization: Bearer {api_token}`）
- **Get token**: Account Settings > API in Ahrefs dashboard （**トークンの取得**: Ahrefs ダッシュボードの [アカウント設定] > [API]）

## Common Agent Operations （エージェントの共通操作）

### Domain rating （ドメインの評価）

```bash
GET https://api.ahrefs.com/v3/site-explorer/domain-rating?target=example.com

Authorization: Bearer {api_token}
```

### Backlinks overview （バックリンクの概要）

```bash
GET https://api.ahrefs.com/v3/site-explorer/backlinks-stats?target=example.com&mode=domain

Authorization: Bearer {api_token}
```

### Referring domains （参照元ドメイン）

```bash
GET https://api.ahrefs.com/v3/site-explorer/refdomains?target=example.com&mode=domain&limit=100

Authorization: Bearer {api_token}
```

### Backlinks list （バックリンクリスト）

```bash
GET https://api.ahrefs.com/v3/site-explorer/backlinks?target=example.com&mode=domain&limit=100

Authorization: Bearer {api_token}
```

### Organic keywords （オーガニックキーワード）

```bash
GET https://api.ahrefs.com/v3/site-explorer/organic-keywords?target=example.com&mode=domain&country=us&limit=100

Authorization: Bearer {api_token}
```

### Top pages （トップページ）

```bash
GET https://api.ahrefs.com/v3/site-explorer/top-pages?target=example.com&mode=domain&country=us&limit=50

Authorization: Bearer {api_token}
```

### Keyword overview （キーワードの概要）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/overview?keywords=keyword1,keyword2&country=us

Authorization: Bearer {api_token}
```

### Keyword suggestions （キーワードの提案）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/matching-terms?keyword=seed+keyword&country=us&limit=100

Authorization: Bearer {api_token}
```

### SERP overview （SERPの概要）

```bash
GET https://api.ahrefs.com/v3/keywords-explorer/serp-overview?keyword=target+keyword&country=us

Authorization: Bearer {api_token}
```

## Key Metrics （主要な指標）

### Domain Metrics （ドメインメトリクス）
- `domain_rating` - Domain Rating (DR) （`domain_rating` - ドメイン評価 (DR)）
- `ahrefs_rank` - Ahrefs Rank （`ahrefs_rank` - Ahrefs ランク）
- `referring_domains` - Referring domains count （`referring_domains` - 参照元ドメインの数）
- `backlinks` - Total backlinks （`backlinks` - バックリンクの合計数）
- `organic_traffic` - Estimated organic traffic （`organic_traffic` - 推定オーガニックトラフィック）

### Keyword Metrics （キーワード指標）
- `volume` - Monthly search volume （`volume` - 月間検索ボリューム）
- `keyword_difficulty` - KD score (0-100) （`keyword_difficulty` - KD スコア (0-100)）
- `cpc` - Cost per click （`cpc` - クリックあたりのコスト）
- `clicks` - Estimated monthly clicks （`clicks` - 推定月間クリック数）
- `global_volume` - Global search volume （`global_volume` - グローバル検索ボリューム）

### Backlink Fields （バックリンクフィールド）
- `url_from` - Source URL （`url_from` - ソース URL）
- `url_to` - Target URL （`url_to` - ターゲット URL）
- `anchor` - Anchor text （`anchor` - アンカーテキスト）
- `domain_rating_source` - Source DR （`domain_rating_source` - ソース DR）
- `first_seen` - First discovery date （`first_seen` - 最初の発見日）

## Modes （モード）

- `domain` - Entire domain （`domain` - ドメイン全体）
- `subdomains` - Domain + subdomains （`subdomains` - ドメイン + サブドメイン）
- `prefix` - URL prefix （`prefix` - URL プレフィックス）
- `exact` - Exact URL （`exact` - 正確な URL）

## When to Use （いつ使用するか）

- Backlink analysis （バックリンク分析）
- Link building research （リンクビルディングの調査）
- Keyword research （キーワード調査）
- Competitive analysis （競合分析）
- Content gap analysis （コンテンツギャップ分析）
- Site audits （現場監査）

## Rate Limits （レート制限）

- Varies by plan （プランにより異なります）
- 500-5000 rows per request （リクエストあたり 500 ～ 5000 行）

## Relevant Skills （関連するスキル）

- seo-audit （SEO監査）
- content-strategy （コンテンツ戦略）
- competitor-alternatives （競合他社の代替品）
