# HubSpot （ハブスポット）

CRM platform for marketing, sales, and customer service. （マーケティング、販売、顧客サービスのための CRM プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API for CRM, Marketing, Sales（CRM、マーケティング、販売向けの REST API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | `hs` CLI for local development（`hs` ローカル開発用の CLI） |
| SDK（SDK） | ✓ | Official client libraries（公式クライアントライブラリ） |

## Authentication （認証）

- **Type**: Private App Token or OAuth 2.0 （**タイプ**: プライベート アプリ トークンまたは OAuth 2.0）
- **Header**: `Authorization: Bearer {access_token}` （**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Get token**: Settings > Integrations > Private Apps （**トークンの取得**: [設定] > [統合] > [プライベート アプリ]）

## Common Agent Operations （エージェントの共通操作）

### Get contacts （連絡先を取得する）

```bash
GET https://api.hubapi.com/crm/v3/objects/contacts?limit=10

Authorization: Bearer {access_token}
```

### Search contacts （連絡先の検索）

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

### Create contact （連絡先の作成）

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

### Update contact （連絡先を更新する）

```bash
PATCH https://api.hubapi.com/crm/v3/objects/contacts/{contact_id}

{
  "properties": {
    "lifecyclestage": "customer"
  }
}
```

### Get deals （お得な情報を入手）

```bash
GET https://api.hubapi.com/crm/v3/objects/deals?limit=10&properties=dealname,amount,dealstage

Authorization: Bearer {access_token}
```

### Create deal （取引の作成）

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

### Associate contact with deal （連絡先を取引に関連付けます）

```bash
PUT https://api.hubapi.com/crm/v3/objects/deals/{deal_id}/associations/contacts/{contact_id}/deal_to_contact
```

### Get form submissions （フォームの送信を取得する）

```bash
GET https://api.hubapi.com/form-integrations/v1/submissions/forms/{form_guid}

Authorization: Bearer {access_token}
```

### Get marketing emails （マーケティングメールを受け取る）

```bash
GET https://api.hubapi.com/marketing/v3/emails?limit=10

Authorization: Bearer {access_token}
```

## CLI Commands （CLIコマンド）

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

## Key Objects （主要なオブジェクト）

- **Contacts** - People in CRM （**連絡先** - CRM 担当者）
- **Companies** - Organizations （**会社** - 組織）
- **Deals** - Sales opportunities （**取引** - 販売機会）
- **Tickets** - Support tickets （**チケット** - サポート チケット）
- **Products** - Items for sale （**製品** - 販売商品）
- **Line Items** - Deal line items （**品目** - 取引品目）

## Common Properties （共通のプロパティ）

### Contact Properties （連絡先のプロパティ）
- `email` - Email address （`email` - メールアドレス）
- `firstname`, `lastname` - Name （`firstname`、`lastname` - 名前）
- `lifecyclestage` - Funnel stage （`lifecyclestage` - ファネルステージ）
- `hs_lead_status` - Lead status （`hs_lead_status` - リードのステータス）

### Deal Properties （取引のプロパティ）
- `dealname` - Deal name （`dealname` - 取引名）
- `amount` - Deal value （`amount` - 取引値）
- `dealstage` - Pipeline stage （`dealstage` - パイプラインステージ）
- `closedate` - Expected close （`closedate` - 終了予定）

## When to Use （いつ使用するか）

- Managing contacts and leads （連絡先とリードの管理）
- Tracking sales deals （販売取引の追跡）
- Marketing automation （マーケティングオートメーション）
- Form submissions （フォームの送信）
- Email campaigns （メールキャンペーン）
- Customer service tickets （カスタマーサービスチケット）

## Rate Limits （レート制限）

- 100 requests per 10 seconds （10 秒あたり 100 リクエスト）
- Higher limits on enterprise plans （エンタープライズプランの制限の引き上げ）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- analytics-tracking （分析追跡）
- referral-program （紹介プログラム）
