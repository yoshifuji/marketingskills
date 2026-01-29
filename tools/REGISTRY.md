# Marketing Tools Registry （日本語訳：マーケティングツールレジストリ）

Quick reference for AI agents to discover tool capabilities and integration methods. （日本語訳：AI エージェントがツールの機能と統合方法を発見するためのクイック リファレンス。）

## How to Use This Registry （日本語訳：このレジストリの使用方法）

1. **Find tools by category** - Browse sections below for tools in each domain （日本語訳：**カテゴリ別にツールを検索** - 各ドメインのツールについては、以下のセクションを参照してください）
2. **Check integration methods** - See what APIs, MCPs, CLIs, or SDKs are available （日本語訳：**統合方法を確認してください** - 利用可能な API、MCP、CLI、または SDK を確認してください）
3. **Read integration guides** - Detailed setup and common operations in `integrations/` （日本語訳：**統合ガイドを読む** - `integrations/` での詳細なセットアップと一般的な操作）

---

## Tool Index （日本語訳：ツールインデックス）

| Tool（日本語訳：道具） | Category（日本語訳：カテゴリ） | API（日本語訳：API） | MCP（日本語訳：MCP） | CLI（日本語訳：CLI） | SDK（日本語訳：SDK） | Guide（日本語訳：ガイド） |
|------|----------|:---:|:---:|:---:|:---:|-------|
| ga4（日本語訳：が4） | Analytics（日本語訳：分析） | ✓ | ✓ | - | ✓ | [ga4.md](integrations/ga4.md)（日本語訳：[ga4.md](統合/ga4.md)） |
| mixpanel（日本語訳：ミックスパネル） | Analytics（日本語訳：分析） | ✓ | - | - | ✓ | [mixpanel.md](integrations/mixpanel.md)（日本語訳：[mixpanel.md](integrations/mixpanel.md)） |
| amplitude（日本語訳：振幅） | Analytics（日本語訳：分析） | ✓ | - | - | ✓ | [amplitude.md](integrations/amplitude.md)（日本語訳：[振幅.md](積分/振幅.md)） |
| posthog（日本語訳：ポストホッグ） | Analytics（日本語訳：分析） | ✓ | - | ✓ | ✓ | [posthog.md](integrations/posthog.md)（日本語訳：[posthog.md](integrations/posthog.md)） |
| segment（日本語訳：セグメント） | Analytics（日本語訳：分析） | ✓ | - | - | ✓ | [segment.md](integrations/segment.md)（日本語訳：[segment.md](integrations/segment.md)） |
| adobe-analytics（日本語訳：アドビアナリティクス） | Analytics（日本語訳：分析） | ✓ | - | - | ✓ | [adobe-analytics.md](integrations/adobe-analytics.md)（日本語訳：[adobe-analytics.md](integrations/adobe-analytics.md)） |
| google-search-console（日本語訳：グーグルサーチコンソール） | SEO（日本語訳：SEO） | ✓ | - | - | ✓ | [google-search-console.md](integrations/google-search-console.md)（日本語訳：[google-search-console.md](integrations/google-search-console.md)） |
| semrush（日本語訳：セムラッシュ） | SEO（日本語訳：SEO） | ✓ | - | - | - | [semrush.md](integrations/semrush.md)（日本語訳：[semrush.md](integrations/semrush.md)） |
| ahrefs（日本語訳：ああレフ） | SEO（日本語訳：SEO） | ✓ | - | - | - | [ahrefs.md](integrations/ahrefs.md)（日本語訳：[ahrefs.md](integrations/ahrefs.md)） |
| hubspot（日本語訳：ハブスポット） | CRM（日本語訳：CRM） | ✓ | - | ✓ | ✓ | [hubspot.md](integrations/hubspot.md)（日本語訳：[hubspot.md](integrations/hubspot.md)） |
| salesforce（日本語訳：セールスフォース） | CRM（日本語訳：CRM） | ✓ | - | ✓ | ✓ | [salesforce.md](integrations/salesforce.md)（日本語訳：[セールスフォース.md](統合/セールスフォース.md)） |
| stripe（日本語訳：ストライプ） | Payments（日本語訳：支払い） | ✓ | ✓ | ✓ | ✓ | [stripe.md](integrations/stripe.md)（日本語訳：[ストライプ.md](統合/ストライプ.md)） |
| rewardful（日本語訳：やりがいのある） | Referral（日本語訳：紹介） | ✓ | - | - | - | [rewardful.md](integrations/rewardful.md)（日本語訳：[rewardful.md](integrations/rewardful.md)） |
| tolt（日本語訳：押し込まれた） | Referral（日本語訳：紹介） | ✓ | - | - | - | [tolt.md](integrations/tolt.md)（日本語訳：[tolt.md](統合/tolt.md)） |
| dub-co（日本語訳：ダブコ） | Links（日本語訳：リンク） | ✓ | - | - | ✓ | [dub-co.md](integrations/dub-co.md)（日本語訳：[dub-co.md](integrations/dub-co.md)） |
| mention-me（日本語訳：私に言及してください） | Referral（日本語訳：紹介） | ✓ | - | - | - | [mention-me.md](integrations/mention-me.md)（日本語訳：[mention-me.md](integrations/mention-me.md)） |
| mailchimp（日本語訳：メールチンパンジー） | Email（日本語訳：電子メール） | ✓ | ✓ | - | ✓ | [mailchimp.md](integrations/mailchimp.md)（日本語訳：[mailchimp.md](integrations/mailchimp.md)） |
| customer-io（日本語訳：顧客-IO） | Email（日本語訳：電子メール） | ✓ | - | - | ✓ | [customer-io.md](integrations/customer-io.md)（日本語訳：[customer-io.md](integrations/customer-io.md)） |
| sendgrid（日本語訳：センドグリッド） | Email（日本語訳：電子メール） | ✓ | - | - | ✓ | [sendgrid.md](integrations/sendgrid.md)（日本語訳：[sendgrid.md](integrations/sendgrid.md)） |
| resend（日本語訳：再送信する） | Email（日本語訳：電子メール） | ✓ | ✓ | - | ✓ | [resend.md](integrations/resend.md)（日本語訳：[resend.md](integrations/resend.md)） |
| kit（日本語訳：キット） | Email（日本語訳：電子メール） | ✓ | - | - | ✓ | [kit.md](integrations/kit.md)（日本語訳：[kit.md](統合/kit.md)） |
| google-ads（日本語訳：グーグル広告） | Ads（日本語訳：広告） | ✓ | ✓ | - | ✓ | [google-ads.md](integrations/google-ads.md)（日本語訳：[google-ads.md](integrations/google-ads.md)） |
| meta-ads（日本語訳：メタ広告） | Ads（日本語訳：広告） | ✓ | - | - | ✓ | [meta-ads.md](integrations/meta-ads.md)（日本語訳：[meta-ads.md](integrations/meta-ads.md)） |
| linkedin-ads（日本語訳：リンクされた広告） | Ads（日本語訳：広告） | ✓ | - | - | - | [linkedin-ads.md](integrations/linkedin-ads.md)（日本語訳：[linkedin-ads.md](integrations/linkedin-ads.md)） |
| tiktok-ads（日本語訳：ティックトック広告） | Ads（日本語訳：広告） | ✓ | - | - | ✓ | [tiktok-ads.md](integrations/tiktok-ads.md)（日本語訳：[tiktok-ads.md](integrations/tiktok-ads.md)） |
| zapier（日本語訳：ザピア） | Automation（日本語訳：オートメーション） | ✓ | ✓ | - | - | [zapier.md](integrations/zapier.md)（日本語訳：[zapier.md](integrations/zapier.md)） |
| shopify（日本語訳：買い物する） | Commerce（日本語訳：商業） | ✓ | - | ✓ | ✓ | [shopify.md](integrations/shopify.md)（日本語訳：[shopify.md](integrations/shopify.md)） |
| wordpress（日本語訳：ワードプレス） | CMS（日本語訳：CMS） | ✓ | - | ✓ | ✓ | [wordpress.md](integrations/wordpress.md)（日本語訳：[wordpress.md](integrations/wordpress.md)） |
| webflow（日本語訳：ウェブフロー） | CMS（日本語訳：CMS） | ✓ | - | ✓ | ✓ | [webflow.md](integrations/webflow.md)（日本語訳：[webflow.md](integrations/webflow.md)） |

---

## By Category （日本語訳：カテゴリ別）

### Analytics （日本語訳：分析）

Track user behavior, measure conversions, and analyze marketing performance. （日本語訳：ユーザーの行動を追跡し、コンバージョンを測定し、マーケティングのパフォーマンスを分析します。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP Available（日本語訳：MCPが利用可能） |
|------|----------|:-------------:|
| **ga4**（日本語訳：**が4**） | Web analytics, Google ecosystem（日本語訳：ウェブ解析、Google エコシステム） | ✓ |
| **mixpanel**（日本語訳：**ミックスパネル**） | Product analytics, event tracking（日本語訳：製品分析、イベント追跡） | - |
| **amplitude**（日本語訳：**振幅**） | Product analytics, cohort analysis（日本語訳：製品分析、コホート分析） | - |
| **posthog**（日本語訳：**ポストホッグ**） | Open-source analytics, session replay（日本語訳：オープンソース分析、セッションリプレイ） | - |
| **segment**（日本語訳：**セグメント**） | Customer data platform, routing（日本語訳：顧客データ プラットフォーム、ルーティング） | - |
| **adobe-analytics**（日本語訳：**アドビアナリティクス**） | Enterprise analytics（日本語訳：エンタープライズ分析） | - |

**Agent recommendation**: Start with GA4 if using Google ecosystem. Use Mixpanel or Amplitude for deeper product analytics. （日本語訳：**エージェントの推奨事項**: Google エコシステムを使用している場合は、GA4 から始めてください。より詳細な製品分析には、Mixpanel または Amplitude を使用します。）

### SEO （日本語訳：SEO）

Search engine optimization tools for keyword research, rank tracking, and site audits. （日本語訳：キーワード調査、ランク追跡、サイト監査のための検索エンジン最適化ツール。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | Notes（日本語訳：注意事項） |
|------|----------|-------|
| **google-search-console**（日本語訳：**グーグル検索コンソール**） | Free, authoritative search data（日本語訳：無料で信頼できる検索データ） | Direct from Google（日本語訳：Google から直接） |
| **semrush**（日本語訳：**セムラッシュ**） | Competitive analysis, keyword research（日本語訳：競合分析、キーワード調査） | Comprehensive（日本語訳：包括的な） |
| **ahrefs**（日本語訳：**アーレフ**） | Backlink analysis, content research（日本語訳：バックリンク分析、コンテンツ調査） | Best for links（日本語訳：リンクに最適） |

**Agent recommendation**: Google Search Console is essential (free). Add Semrush or Ahrefs for competitive research. （日本語訳：**エージェントの推奨事項**: Google Search Console は必須です (無料)。競合調査のために Semrush または Ahrefs を追加します。）

### CRM （日本語訳：CRM）

Customer relationship management and sales tools. （日本語訳：顧客関係管理および販売ツール。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | CLI Available（日本語訳：CLI が利用可能） |
|------|----------|:-------------:|
| **hubspot**（日本語訳：**ハブスポット**） | SMB, marketing + sales alignment（日本語訳：SMB、マーケティング + 営業連携） | ✓ |
| **salesforce**（日本語訳：**セールスフォース**） | Enterprise, complex sales processes（日本語訳：エンタープライズ向けの複雑な販売プロセス） | ✓ |

**Agent recommendation**: HubSpot for startups/SMBs, Salesforce for enterprise. （日本語訳：**エージェントの推奨事項**: スタートアップ/SMB には HubSpot、エンタープライズには Salesforce。）

### Payments （日本語訳：支払い）

Payment processing and subscription management. （日本語訳：支払い処理とサブスクリプション管理。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP Available（日本語訳：MCPが利用可能） |
|------|----------|:-------------:|
| **stripe**（日本語訳：**ストライプ**） | SaaS subscriptions, developer-friendly（日本語訳：SaaS サブスクリプション、開発者に優しい） | ✓ |

**Agent recommendation**: Stripe is the default for SaaS and developer-focused products. （日本語訳：**エージェントの推奨事項**: SaaS および開発者向け製品のデフォルトは Stripe です。）

### Referral & Affiliate （日本語訳：紹介とアフィリエイト）

Tools for referral programs, affiliate tracking, and partner management. （日本語訳：紹介プログラム、アフィリエイト追跡、パートナー管理のためのツール。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | Stripe Integration（日本語訳：ストライプの統合） |
|------|----------|:------------------:|
| **rewardful**（日本語訳：**やりがいのある**） | Stripe-native affiliate programs（日本語訳：Stripe ネイティブのアフィリエイト プログラム） | ✓ |
| **tolt**（日本語訳：**押す**） | SaaS affiliate programs（日本語訳：SaaS アフィリエイト プログラム） | ✓ |
| **mention-me**（日本語訳：**メンションしてください**） | Enterprise referral programs（日本語訳：企業紹介プログラム） | ✓ |
| **dub-co**（日本語訳：**ダブ何**） | Link tracking, attribution（日本語訳：リンク追跡、帰属） | - |

**Agent recommendation**: Rewardful or Tolt for Stripe-based SaaS. Dub.co for link attribution. （日本語訳：**エージェントの推奨事項**: Stripe ベースの SaaS の場合は、やりがいがあるか、非常に有益です。リンクの帰属については Dub.co 。）

### Email （日本語訳：電子メール）

Email marketing, transactional email, and automation platforms. （日本語訳：電子メール マーケティング、トランザクション電子メール、および自動化プラットフォーム。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP Available（日本語訳：MCPが利用可能） |
|------|----------|:-------------:|
| **mailchimp**（日本語訳：**メールチンパンジー**） | SMB email marketing（日本語訳：SMB電子メールマーケティング） | ✓ |
| **customer-io**（日本語訳：**顧客-IO**） | Behavior-based messaging（日本語訳：行動ベースのメッセージング） | - |
| **sendgrid**（日本語訳：**センドグリッド**） | Transactional email at scale（日本語訳：大規模なトランザクションメール） | - |
| **resend**（日本語訳：**再送信**） | Developer-friendly transactional（日本語訳：開発者にとって使いやすいトランザクション） | ✓ |
| **kit**（日本語訳：**キット**） | Creator/newsletter focused（日本語訳：クリエイター/ニュースレター中心） | - |

**Agent recommendation**: Resend for transactional (dev-friendly). Customer.io for advanced automation. Kit for creators. （日本語訳：**エージェントの推奨事項**: トランザクション用に再送信します (開発者向け)。高度な自動化のための Customer.io。クリエイター向けキット。）

### Advertising （日本語訳：広告）

Paid advertising platforms and campaign management. （日本語訳：有料広告プラットフォームとキャンペーン管理。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP Available（日本語訳：MCPが利用可能） |
|------|----------|:-------------:|
| **google-ads**（日本語訳：**Google 広告**） | Search intent, high-intent traffic（日本語訳：検索目的、高目的トラフィ​​ック） | ✓ |
| **meta-ads**（日本語訳：**メタ広告**） | Demand gen, visual products, B2C（日本語訳：需要創出、ビジュアルプロダクト、B2C） | - |
| **linkedin-ads**（日本語訳：**リンクされた広告**） | B2B, job title targeting（日本語訳：B2B、役職ターゲティング） | - |
| **tiktok-ads**（日本語訳：**tiktok広告**） | Younger demographics, video（日本語訳：若年層、ビデオ） | - |

**Agent recommendation**: Google Ads for search intent. Meta for demand generation. LinkedIn for B2B. （日本語訳：**エージェントの推奨事項**: 検索目的の Google 広告。需要創出のためのメタ。 B2B 向けの LinkedIn。）

### Automation （日本語訳：オートメーション）

Workflow automation and integration platforms. （日本語訳：ワークフローの自動化と統合プラットフォーム。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | MCP Available（日本語訳：MCPが利用可能） |
|------|----------|:-------------:|
| **zapier**（日本語訳：**ザピア**） | No-code integrations（日本語訳：コード不要の統合） | ✓ |

**Agent recommendation**: Zapier for connecting tools without code. （日本語訳：**エージェントの推奨事項**: コードなしでツールを接続するための Zapier。）

### Commerce & CMS （日本語訳：コマースとCMS）

E-commerce platforms and content management systems. （日本語訳：電子商取引プラットフォームとコンテンツ管理システム。）

| Tool（日本語訳：道具） | Best For（日本語訳：最適な用途） | CLI Available（日本語訳：CLI が利用可能） |
|------|----------|:-------------:|
| **shopify**（日本語訳：**ショッピング**） | E-commerce, product sales（日本語訳：Eコマース、物販） | ✓ |
| **wordpress**（日本語訳：**ワードプレス**） | Blogs, content sites（日本語訳：ブログ、コンテンツ サイト） | ✓ |
| **webflow**（日本語訳：**ウェブフロー**） | Design-focused marketing sites（日本語訳：デザイン重視のマーケティングサイト） | ✓ |

**Agent recommendation**: Shopify for e-commerce. Webflow for marketing sites. WordPress for blogs. （日本語訳：**エージェントの推奨事項**: 電子商取引には Shopify。マーケティング サイト向けの Webflow。ブログ用のWordPress。）

---

## MCP-Enabled Tools （日本語訳：MCP 対応ツール）

These tools have Model Context Protocol servers available, enabling direct agent interaction: （日本語訳：これらのツールにはモデル コンテキスト プロトコル サーバーが用意されており、エージェントとの直接対話が可能になります。）

- **ga4** - Google Analytics 4 data access （日本語訳：**ga4** - Google アナリティクス 4 データ アクセス）
- **stripe** - Payment and subscription management （日本語訳：**ストライプ** - 支払いとサブスクリプションの管理）
- **mailchimp** - Email campaign management （日本語訳：**mailchimp** - 電子メール キャンペーン管理）
- **google-ads** - Ad campaign management （日本語訳：**google-ads** - 広告キャンペーン管理）
- **resend** - Transactional email sending （日本語訳：**再送信** - トランザクション電子メールの送信）
- **zapier** - Workflow automation （日本語訳：**zapier** - ワークフローの自動化）

To use MCP tools, ensure the appropriate MCP server is configured in your environment. （日本語訳：MCP ツールを使用するには、環境内に適切な MCP サーバーが構成されていることを確認してください。）

---

## Quick Start by Use Case （日本語訳：ユースケース別のクイックスタート）

### Setting up analytics tracking （日本語訳：分析トラッキングの設定）
1. Read [ga4.md](integrations/ga4.md) for web analytics （日本語訳：Web 分析については [ga4.md](integrations/ga4.md) を参照してください。）
2. Read [segment.md](integrations/segment.md) if routing to multiple tools （日本語訳：複数のツールにルーティングする場合は、[segment.md](integrations/segment.md) を読み取ります。）

### Launching a referral program （日本語訳：紹介プログラムの開始）
1. Read [rewardful.md](integrations/rewardful.md) or [tolt.md](integrations/tolt.md) for Stripe-based programs （日本語訳：Stripe ベースのプログラムの場合は、[rewardful.md](integrations/rewardful.md) または [tolt.md](integrations/tolt.md) を参照してください。）
2. Read [dub-co.md](integrations/dub-co.md) for link tracking （日本語訳：リンク追跡については [dub-co.md](integrations/dub-co.md) を参照してください。）

### Setting up email automation （日本語訳：電子メールの自動化を設定する）
1. Read [customer-io.md](integrations/customer-io.md) for behavior-based automation （日本語訳：動作ベースの自動化については、[customer-io.md](integrations/customer-io.md) を参照してください。）
2. Read [resend.md](integrations/resend.md) for transactional email （日本語訳：トランザクション電子メールについては、[resend.md](integrations/resend.md) を参照してください。）

### Running paid ads （日本語訳：有料広告の掲載）
1. Read [google-ads.md](integrations/google-ads.md) for search campaigns （日本語訳：検索キャンペーンについては [google-ads.md](integrations/google-ads.md) をご覧ください。）
2. Read [meta-ads.md](integrations/meta-ads.md) for social campaigns （日本語訳：ソーシャル キャンペーンについては [meta-ads.md](integrations/meta-ads.md) を参照してください。）
