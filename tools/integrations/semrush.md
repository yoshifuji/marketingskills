# SEMrush （日本語訳：SEMrush）

SEO and competitive analysis platform for keyword research and site audits. （日本語訳：キーワード調査とサイト監査のための SEO および競合分析プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | Analytics API, Projects API（日本語訳：分析API、プロジェクトAPI） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | - | Not available（日本語訳：利用不可） |
| SDK（日本語訳：SDK） | - | API-only（日本語訳：APIのみ） |

## Authentication （日本語訳：認証）

- **Type**: API Key （日本語訳：**タイプ**: API キー）
- **Parameter**: `key={api_key}` in query string （日本語訳：**パラメータ**: クエリ文字列内の `key={api_key}`）
- **Get key**: My Profile > API in SEMrush dashboard （日本語訳：**キーの取得**: SEMrush ダッシュボードの [マイ プロフィール] > [API]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Domain overview （日本語訳：ドメインの概要）

```bash
GET https://api.semrush.com/?type=domain_ranks&key={api_key}&export_columns=Db,Dn,Rk,Or,Ot,Oc,Ad,At,Ac&domain=example.com
```

### Organic keywords （日本語訳：オーガニックキーワード）

```bash
GET https://api.semrush.com/?type=domain_organic&key={api_key}&export_columns=Ph,Po,Pp,Pd,Nq,Cp,Ur,Tr,Tc,Co,Nr&domain=example.com&database=us&display_limit=100
```

### Keyword overview （日本語訳：キーワードの概要）

```bash
GET https://api.semrush.com/?type=phrase_all&key={api_key}&export_columns=Ph,Nq,Cp,Co,Nr&phrase=keyword&database=us
```

### Related keywords （日本語訳：関連キーワード）

```bash
GET https://api.semrush.com/?type=phrase_related&key={api_key}&export_columns=Ph,Nq,Cp,Co,Nr,Td&phrase=keyword&database=us&display_limit=50
```

### Keyword difficulty （日本語訳：キーワードの難易度）

```bash
GET https://api.semrush.com/?type=phrase_kdi&key={api_key}&export_columns=Ph,Kd&phrase=keyword&database=us
```

### Backlinks overview （日本語訳：バックリンクの概要）

```bash
GET https://api.semrush.com/?type=backlinks_overview&key={api_key}&target=example.com&target_type=root_domain
```

### Backlinks list （日本語訳：バックリンクリスト）

```bash
GET https://api.semrush.com/?type=backlinks&key={api_key}&target=example.com&target_type=root_domain&export_columns=source_url,source_title,target_url,anchor&display_limit=100
```

### Competitors （日本語訳：競合他社）

```bash
GET https://api.semrush.com/?type=domain_organic_organic&key={api_key}&export_columns=Dn,Cr,Np,Or,Ot,Oc,Ad&domain=example.com&database=us&display_limit=20
```

## Response Format （日本語訳：応答フォーマット）

Responses are CSV by default. Add `&export_escape=1` for proper escaping. （日本語訳：デフォルトでは、応答は CSV です。適切にエスケープするために `&export_escape=1` を追加します。）

## Export Columns （日本語訳：列のエクスポート）

### Domain Report （日本語訳：ドメインレポート）
- `Db` - Database （日本語訳：`Db` - データベース）
- `Dn` - Domain （日本語訳：`Dn` - ドメイン）
- `Rk` - Rank （日本語訳：`Rk` - ランク）
- `Or` - Organic keywords （日本語訳：`Or` - オーガニックキーワード）
- `Ot` - Organic traffic （日本語訳：`Ot` - オーガニックトラフィック）
- `Oc` - Organic cost （日本語訳：`Oc` - オーガニックコスト）

### Keyword Report （日本語訳：キーワードレポート）
- `Ph` - Phrase/keyword （日本語訳：`Ph` - フレーズ/キーワード）
- `Nq` - Search volume （日本語訳：`Nq` - 検索ボリューム）
- `Cp` - CPC （日本語訳：`Cp` - CPC）
- `Co` - Competition （日本語訳：`Co` - 競争）
- `Kd` - Keyword difficulty （日本語訳：`Kd` - キーワードの難易度）
- `Nr` - Number of results （日本語訳：`Nr` - 結果の数）

### Backlinks （日本語訳：バックリンク）
- `source_url` - Linking page （日本語訳：`source_url` - リンクページ）
- `target_url` - Target page （日本語訳：`target_url` - ターゲットページ）
- `anchor` - Anchor text （日本語訳：`anchor` - アンカーテキスト）
- `source_title` - Page title （日本語訳：`source_title` - ページのタイトル）

## Databases （日本語訳：データベース）

Use country code: `us`, `uk`, `de`, `fr`, `ca`, `au`, etc. （日本語訳：国コードを使用します: `us`、`uk`、`de`、`fr`、`ca`、`au` など。）

## When to Use （日本語訳：いつ使用するか）

- Keyword research （日本語訳：キーワード調査）
- Competitive analysis （日本語訳：競合分析）
- Backlink analysis （日本語訳：バックリンク分析）
- Site audits （日本語訳：現場監査）
- Rank tracking （日本語訳：ランク追跡）
- Content gap analysis （日本語訳：コンテンツギャップ分析）

## Rate Limits （日本語訳：レート制限）

- Varies by plan (10-30K units/day) （日本語訳：プランにより異なります（10～30,000ユニット/日））
- Each API call costs units （日本語訳：各 API 呼び出しには単位がかかります）

## Relevant Skills （日本語訳：関連するスキル）

- seo-audit （日本語訳：SEO監査）
- programmatic-seo （日本語訳：プログラマティックSEO）
- content-strategy （日本語訳：コンテンツ戦略）
- competitor-alternatives （日本語訳：競合他社の代替品）
