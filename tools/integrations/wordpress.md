# WordPress （日本語訳：ワードプレス）

Content management system for blogs and websites. （日本語訳：ブログやウェブサイトのコンテンツ管理システム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API (WP REST API)（日本語訳：REST API (WP REST API)） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | WP-CLI for server-side management（日本語訳：サーバー側管理用の WP-CLI） |
| SDK（日本語訳：SDK） | ✓ | Various client libraries（日本語訳：さまざまなクライアントライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: Application Password, JWT, or OAuth （日本語訳：**タイプ**: アプリケーションパスワード、JWT、または OAuth）
- **Header**: `Authorization: Basic {base64(username:app_password)}` （日本語訳：**ヘッダー**: `Authorization: Basic {base64(username:app_password)}`）
- **Setup**: Users > Your Profile > Application Passwords （日本語訳：**セットアップ**: ユーザー > プロフィール > アプリケーション パスワード）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### List posts （日本語訳：投稿を一覧表示する）

```bash
GET https://example.com/wp-json/wp/v2/posts?per_page=10

Authorization: Basic {base64(username:app_password)}
```

### Get post （日本語訳：投稿を取得する）

```bash
GET https://example.com/wp-json/wp/v2/posts/{post_id}

Authorization: Basic {base64(username:app_password)}
```

### Create post （日本語訳：投稿を作成する）

```bash
POST https://example.com/wp-json/wp/v2/posts

Authorization: Basic {base64(username:app_password)}

{
  "title": "Post Title",
  "content": "<p>Post content here</p>",
  "status": "draft",
  "categories": [1],
  "tags": [5, 6]
}
```

### Update post （日本語訳：投稿を更新）

```bash
PUT https://example.com/wp-json/wp/v2/posts/{post_id}

Authorization: Basic {base64(username:app_password)}

{
  "title": "Updated Title",
  "status": "publish"
}
```

### List pages （日本語訳：リストページ）

```bash
GET https://example.com/wp-json/wp/v2/pages?per_page=20

Authorization: Basic {base64(username:app_password)}
```

### List categories （日本語訳：リストカテゴリ）

```bash
GET https://example.com/wp-json/wp/v2/categories
```

### Create category （日本語訳：カテゴリの作成）

```bash
POST https://example.com/wp-json/wp/v2/categories

{
  "name": "Category Name",
  "slug": "category-name"
}
```

### Upload media （日本語訳：メディアをアップロードする）

```bash
POST https://example.com/wp-json/wp/v2/media

Authorization: Basic {base64(username:app_password)}
Content-Disposition: attachment; filename="image.jpg"
Content-Type: image/jpeg

[binary image data]
```

### List users （日本語訳：ユーザーのリストを表示する）

```bash
GET https://example.com/wp-json/wp/v2/users

Authorization: Basic {base64(username:app_password)}
```

## WP-CLI Commands （日本語訳：WP-CLI コマンド）

```bash
# List posts
wp post list --post_type=post --post_status=publish

# Create post
wp post create --post_title="Title" --post_content="Content" --post_status=publish

# Update post
wp post update 123 --post_title="New Title"

# Export database
wp db export backup.sql

# Search/replace in database
wp search-replace 'old-domain.com' 'new-domain.com'

# Install plugin
wp plugin install yoast-seo --activate

# Update plugins
wp plugin update --all
```

## Post Statuses （日本語訳：投稿ステータス）

- `publish` - Live on site （日本語訳：`publish` - オンサイトでライブ）
- `draft` - Not published （日本語訳：`draft` - 公開されていません）
- `pending` - Awaiting review （日本語訳：`pending` - レビュー待ち）
- `private` - Private post （日本語訳：`private` - プライベート投稿）
- `future` - Scheduled （日本語訳：`future` - スケジュール済み）
- `trash` - In trash （日本語訳：`trash` - ゴミ箱内）

## Common Endpoints （日本語訳：共通エンドポイント）

| Endpoint（日本語訳：終点） | Resource（日本語訳：リソース） |
|----------|----------|
| `/wp/v2/posts`（日本語訳：__コード0__） | Blog posts（日本語訳：ブログ投稿） |
| `/wp/v2/pages`（日本語訳：__コード0__） | Pages（日本語訳：ページ） |
| `/wp/v2/media`（日本語訳：__コード0__） | Images/files（日本語訳：画像/ファイル） |
| `/wp/v2/categories`（日本語訳：__コード0__） | Categories（日本語訳：カテゴリー） |
| `/wp/v2/tags`（日本語訳：__コード0__） | Tags（日本語訳：タグ） |
| `/wp/v2/users`（日本語訳：__コード0__） | Users（日本語訳：ユーザー） |
| `/wp/v2/comments`（日本語訳：__コード0__） | Comments（日本語訳：コメント） |

## When to Use （日本語訳：いつ使用するか）

- Blog content management （日本語訳：ブログのコンテンツ管理）
- Page updates （日本語訳：ページの更新）
- Media management （日本語訳：メディア管理）
- Site configuration （日本語訳：サイト構成）
- Plugin/theme management （日本語訳：プラグイン/テーマの管理）

## Rate Limits （日本語訳：レート制限）

- No default limits （日本語訳：デフォルトの制限なし）
- Server/host dependent （日本語訳：サーバー/ホストに依存）

## Relevant Skills （日本語訳：関連するスキル）

- content-strategy （日本語訳：コンテンツ戦略）
- seo-audit （日本語訳：SEO監査）
- programmatic-seo （日本語訳：プログラマティックSEO）
