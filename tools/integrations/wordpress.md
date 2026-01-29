# WordPress （ワードプレス）

Content management system for blogs and websites. （ブログやウェブサイトのコンテンツ管理システム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API (WP REST API)（REST API (WP REST API)） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | WP-CLI for server-side management（サーバー側管理用の WP-CLI） |
| SDK（SDK） | ✓ | Various client libraries（さまざまなクライアントライブラリ） |

## Authentication （認証）

- **Type**: Application Password, JWT, or OAuth （**タイプ**: アプリケーションパスワード、JWT、または OAuth）
- **Header**: `Authorization: Basic {base64(username:app_password)}` （**ヘッダー**: `Authorization: Basic {base64(username:app_password)}`）
- **Setup**: Users > Your Profile > Application Passwords （**セットアップ**: ユーザー > プロフィール > アプリケーション パスワード）

## Common Agent Operations （エージェントの共通操作）

### List posts （投稿を一覧表示する）

```bash
GET https://example.com/wp-json/wp/v2/posts?per_page=10

Authorization: Basic {base64(username:app_password)}
```

### Get post （投稿を取得する）

```bash
GET https://example.com/wp-json/wp/v2/posts/{post_id}

Authorization: Basic {base64(username:app_password)}
```

### Create post （投稿を作成する）

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

### Update post （投稿を更新）

```bash
PUT https://example.com/wp-json/wp/v2/posts/{post_id}

Authorization: Basic {base64(username:app_password)}

{
  "title": "Updated Title",
  "status": "publish"
}
```

### List pages （リストページ）

```bash
GET https://example.com/wp-json/wp/v2/pages?per_page=20

Authorization: Basic {base64(username:app_password)}
```

### List categories （リストカテゴリ）

```bash
GET https://example.com/wp-json/wp/v2/categories
```

### Create category （カテゴリの作成）

```bash
POST https://example.com/wp-json/wp/v2/categories

{
  "name": "Category Name",
  "slug": "category-name"
}
```

### Upload media （メディアをアップロードする）

```bash
POST https://example.com/wp-json/wp/v2/media

Authorization: Basic {base64(username:app_password)}
Content-Disposition: attachment; filename="image.jpg"
Content-Type: image/jpeg

[binary image data]
```

### List users （ユーザーのリストを表示する）

```bash
GET https://example.com/wp-json/wp/v2/users

Authorization: Basic {base64(username:app_password)}
```

## WP-CLI Commands （WP-CLI コマンド）

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

## Post Statuses （投稿ステータス）

- `publish` - Live on site （`publish` - オンサイトでライブ）
- `draft` - Not published （`draft` - 公開されていません）
- `pending` - Awaiting review （`pending` - レビュー待ち）
- `private` - Private post （`private` - プライベート投稿）
- `future` - Scheduled （`future` - スケジュール済み）
- `trash` - In trash （`trash` - ゴミ箱内）

## Common Endpoints （共通エンドポイント）

| Endpoint（終点） | Resource（リソース） |
|----------|----------|
| `/wp/v2/posts`（__コード0__） | Blog posts（ブログ投稿） |
| `/wp/v2/pages`（__コード0__） | Pages（ページ） |
| `/wp/v2/media`（__コード0__） | Images/files（画像/ファイル） |
| `/wp/v2/categories`（__コード0__） | Categories（カテゴリー） |
| `/wp/v2/tags`（__コード0__） | Tags（タグ） |
| `/wp/v2/users`（__コード0__） | Users（ユーザー） |
| `/wp/v2/comments`（__コード0__） | Comments（コメント） |

## When to Use （いつ使用するか）

- Blog content management （ブログのコンテンツ管理）
- Page updates （ページの更新）
- Media management （メディア管理）
- Site configuration （サイト構成）
- Plugin/theme management （プラグイン/テーマの管理）

## Rate Limits （レート制限）

- No default limits （デフォルトの制限なし）
- Server/host dependent （サーバー/ホストに依存）

## Relevant Skills （関連するスキル）

- content-strategy （コンテンツ戦略）
- seo-audit （SEO監査）
- programmatic-seo （プログラマティックSEO）
