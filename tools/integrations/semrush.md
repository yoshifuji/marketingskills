# SEMrush （SEMrush）

SEO and competitive analysis platform for keyword research and site audits. （キーワード調査とサイト監査のための SEO および競合分析プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | Analytics API, Projects API（分析API、プロジェクトAPI） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | - | Not available（利用不可） |
| SDK（SDK） | - | API-only（APIのみ） |

## Authentication （認証）

- **Type**: API Key （**タイプ**: API キー）
- **Parameter**: `key={api_key}` in query string （**パラメータ**: クエリ文字列内の `key={api_key}`）
- **Get key**: My Profile > API in SEMrush dashboard （**キーの取得**: SEMrush ダッシュボードの [マイ プロフィール] > [API]）

## Common Agent Operations （エージェントの共通操作）

### Domain overview （ドメインの概要）

```bash
GET https://api.semrush.com/?type=domain_ranks&key={api_key}&export_columns=Db,Dn,Rk,Or,Ot,Oc,Ad,At,Ac&domain=example.com
```

### Organic keywords （オーガニックキーワード）

```bash
GET https://api.semrush.com/?type=domain_organic&key={api_key}&export_columns=Ph,Po,Pp,Pd,Nq,Cp,Ur,Tr,Tc,Co,Nr&domain=example.com&database=us&display_limit=100
```

### Keyword overview （キーワードの概要）

```bash
GET https://api.semrush.com/?type=phrase_all&key={api_key}&export_columns=Ph,Nq,Cp,Co,Nr&phrase=keyword&database=us
```

### Related keywords （関連キーワード）

```bash
GET https://api.semrush.com/?type=phrase_related&key={api_key}&export_columns=Ph,Nq,Cp,Co,Nr,Td&phrase=keyword&database=us&display_limit=50
```

### Keyword difficulty （キーワードの難易度）

```bash
GET https://api.semrush.com/?type=phrase_kdi&key={api_key}&export_columns=Ph,Kd&phrase=keyword&database=us
```

### Backlinks overview （バックリンクの概要）

```bash
GET https://api.semrush.com/?type=backlinks_overview&key={api_key}&target=example.com&target_type=root_domain
```

### Backlinks list （バックリンクリスト）

```bash
GET https://api.semrush.com/?type=backlinks&key={api_key}&target=example.com&target_type=root_domain&export_columns=source_url,source_title,target_url,anchor&display_limit=100
```

### Competitors （競合他社）

```bash
GET https://api.semrush.com/?type=domain_organic_organic&key={api_key}&export_columns=Dn,Cr,Np,Or,Ot,Oc,Ad&domain=example.com&database=us&display_limit=20
```

## Response Format （応答フォーマット）

Responses are CSV by default. Add `&export_escape=1` for proper escaping. （デフォルトでは、応答は CSV です。適切にエスケープするために `&export_escape=1` を追加します。）

## Export Columns （列のエクスポート）

### Domain Report （ドメインレポート）
- `Db` - Database （`Db` - データベース）
- `Dn` - Domain （`Dn` - ドメイン）
- `Rk` - Rank （`Rk` - ランク）
- `Or` - Organic keywords （`Or` - オーガニックキーワード）
- `Ot` - Organic traffic （`Ot` - オーガニックトラフィック）
- `Oc` - Organic cost （`Oc` - オーガニックコスト）

### Keyword Report （キーワードレポート）
- `Ph` - Phrase/keyword （`Ph` - フレーズ/キーワード）
- `Nq` - Search volume （`Nq` - 検索ボリューム）
- `Cp` - CPC （`Cp` - CPC）
- `Co` - Competition （`Co` - 競争）
- `Kd` - Keyword difficulty （`Kd` - キーワードの難易度）
- `Nr` - Number of results （`Nr` - 結果の数）

### Backlinks （バックリンク）
- `source_url` - Linking page （`source_url` - リンクページ）
- `target_url` - Target page （`target_url` - ターゲットページ）
- `anchor` - Anchor text （`anchor` - アンカーテキスト）
- `source_title` - Page title （`source_title` - ページのタイトル）

## Databases （データベース）

Use country code: `us`, `uk`, `de`, `fr`, `ca`, `au`, etc. （国コードを使用します: `us`、`uk`、`de`、`fr`、`ca`、`au` など。）

## When to Use （いつ使用するか）

- Keyword research （キーワード調査）
- Competitive analysis （競合分析）
- Backlink analysis （バックリンク分析）
- Site audits （現場監査）
- Rank tracking （ランク追跡）
- Content gap analysis （コンテンツギャップ分析）

## Rate Limits （レート制限）

- Varies by plan (10-30K units/day) （プランにより異なります（10～30,000ユニット/日））
- Each API call costs units （各 API 呼び出しには単位がかかります）

## Relevant Skills （関連するスキル）

- seo-audit （SEO監査）
- programmatic-seo （プログラマティックSEO）
- content-strategy （コンテンツ戦略）
- competitor-alternatives （競合他社の代替品）
