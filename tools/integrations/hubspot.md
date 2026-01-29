# HubSpot （日本語訳：ハブスポット）

CRM platform for marketing, sales, and customer service. （日本語訳：マーケティング、販売、顧客サービスのための CRM プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API for CRM, Marketing, Sales（日本語訳：CRM、マーケティング、販売向けの REST API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | `hs` CLI for local development（日本語訳：`hs` ローカル開発用の CLI） |
| SDK（日本語訳：SDK） | ✓ | Official client libraries（日本語訳：公式クライアントライブラリ） |

## Authentication （日本語訳：認証）

- **Type**: Private App Token or OAuth 2.0 （日本語訳：**タイプ**: プライベート アプリ トークンまたは OAuth 2.0）
- **Header**: `Authorization: Bearer {access_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Get token**: Settings > Integrations > Private Apps （日本語訳：**トークンの取得**: [設定] > [統合] > [プライベート アプリ]）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Get contacts （日本語訳：連絡先を取得する）

```bash
GET https://api.hubapi.com/crm/v3/objects/contacts?limit=10

Authorization: Bearer {access_token}
```

### Search contacts （日本語訳：連絡先の検索）

```bash
POST https://api.hubapi.com/crm/v3/objects/contacts/search

{
  "filterGroups": [{
    "filters": [{
      "propertyName": "email",
      "operator": "EQ",
      "value": "user@example.com"
    }]
  }]
}
```

### Create contact （日本語訳：連絡先の作成）

```bash
POST https://api.hubapi.com/crm/v3/objects/contacts

{
  "properties": {
    "email": "user@example.com",
    "firstname": "John",
    "lastname": "Doe",
    "company": "Example Inc"
  }
}
```

### Update contact （日本語訳：連絡先を更新する）

```bash
PATCH https://api.hubapi.com/crm/v3/objects/contacts/{contact_id}

{
  "properties": {
    "lifecyclestage": "customer"
  }
}
```

### Get deals （日本語訳：お得な情報を入手）

```bash
GET https://api.hubapi.com/crm/v3/objects/deals?limit=10&properties=dealname,amount,dealstage

Authorization: Bearer {access_token}
```

### Create deal （日本語訳：取引の作成）

```bash
POST https://api.hubapi.com/crm/v3/objects/deals

{
  "properties": {
    "dealname": "New Deal",
    "amount": "10000",
    "dealstage": "appointmentscheduled",
    "pipeline": "default"
  }
}
```

### Associate contact with deal （日本語訳：連絡先を取引に関連付けます）

```bash
PUT https://api.hubapi.com/crm/v3/objects/deals/{deal_id}/associations/contacts/{contact_id}/deal_to_contact
```

### Get form submissions （日本語訳：フォームの送信を取得する）

```bash
GET https://api.hubapi.com/form-integrations/v1/submissions/forms/{form_guid}

Authorization: Bearer {access_token}
```

### Get marketing emails （日本語訳：マーケティングメールを受け取る）

```bash
GET https://api.hubapi.com/marketing/v3/emails?limit=10

Authorization: Bearer {access_token}
```

## CLI Commands （日本語訳：CLIコマンド）

```bash
# Install
npm install -g @hubspot/cli

# Initialize project
hs init

# Upload files
hs upload src dest

# Watch for changes
hs watch src dest

# List portals
hs accounts list
```

## Key Objects （日本語訳：主要なオブジェクト）

- **Contacts** - People in CRM （日本語訳：**連絡先** - CRM 担当者）
- **Companies** - Organizations （日本語訳：**会社** - 組織）
- **Deals** - Sales opportunities （日本語訳：**取引** - 販売機会）
- **Tickets** - Support tickets （日本語訳：**チケット** - サポート チケット）
- **Products** - Items for sale （日本語訳：**製品** - 販売商品）
- **Line Items** - Deal line items （日本語訳：**品目** - 取引品目）

## Common Properties （日本語訳：共通のプロパティ）

### Contact Properties （日本語訳：連絡先のプロパティ）
- `email` - Email address （日本語訳：`email` - メールアドレス）
- `firstname`, `lastname` - Name （日本語訳：`firstname`、`lastname` - 名前）
- `lifecyclestage` - Funnel stage （日本語訳：`lifecyclestage` - ファネルステージ）
- `hs_lead_status` - Lead status （日本語訳：`hs_lead_status` - リードのステータス）

### Deal Properties （日本語訳：取引のプロパティ）
- `dealname` - Deal name （日本語訳：`dealname` - 取引名）
- `amount` - Deal value （日本語訳：`amount` - 取引値）
- `dealstage` - Pipeline stage （日本語訳：`dealstage` - パイプラインステージ）
- `closedate` - Expected close （日本語訳：`closedate` - 終了予定）

## When to Use （日本語訳：いつ使用するか）

- Managing contacts and leads （日本語訳：連絡先とリードの管理）
- Tracking sales deals （日本語訳：販売取引の追跡）
- Marketing automation （日本語訳：マーケティングオートメーション）
- Form submissions （日本語訳：フォームの送信）
- Email campaigns （日本語訳：メールキャンペーン）
- Customer service tickets （日本語訳：カスタマーサービスチケット）

## Rate Limits （日本語訳：レート制限）

- 100 requests per 10 seconds （日本語訳：10 秒あたり 100 リクエスト）
- Higher limits on enterprise plans （日本語訳：エンタープライズプランの制限の引き上げ）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- analytics-tracking （日本語訳：分析追跡）
- referral-program （日本語訳：紹介プログラム）
