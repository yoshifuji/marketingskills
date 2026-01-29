# Salesforce （セールスフォース）

Enterprise CRM platform for sales, service, and marketing. （販売、サービス、マーケティングのためのエンタープライズ CRM プラットフォーム。）

## Capabilities （能力）

| Integration（統合） | Available（利用可能） | Notes（注意事項） |
|-------------|-----------|-------|
| API（API） | ✓ | REST API, SOAP API, Bulk API（REST API、SOAP API、バルク API） |
| MCP（MCP） | - | Not available（利用不可） |
| CLI（CLI） | ✓ | Salesforce CLI (`sf`)（Salesforce CLI (`sf`)） |
| SDK（SDK） | ✓ | JSforce, simple-salesforce, etc.（JSforce、simple-salesforceなど） |

## Authentication （認証）

- **Type**: OAuth 2.0 (Web Server Flow or JWT Bearer) （**タイプ**: OAuth 2.0 (Web サーバー フローまたは JWT ベアラー)）
- **Header**: `Authorization: Bearer {access_token}` （**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Instance URL**: Use instance_url from auth response （**インスタンス URL**: 認証応答からのinstance_urlを使用します。）

## Common Agent Operations （エージェントの共通操作）

### Query records (SOQL) （クエリレコード (SOQL)）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/query?q=SELECT+Id,Name,Email+FROM+Contact+LIMIT+10

Authorization: Bearer {access_token}
```

### Get record by ID （IDでレコードを取得）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/{record_id}

Authorization: Bearer {access_token}
```

### Create record （レコードの作成）

```bash
POST https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact

{
  "FirstName": "John",
  "LastName": "Doe",
  "Email": "john@example.com",
  "AccountId": "{account_id}"
}
```

### Update record （更新記録）

```bash
PATCH https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/{record_id}

{
  "Title": "Senior Developer"
}
```

### Search records (SOSL) （レコードの検索 (SOSL)）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/search?q=FIND+{searchTerm}+IN+ALL+FIELDS+RETURNING+Contact(Id,Name,Email)

Authorization: Bearer {access_token}
```

### Get opportunities （機会を得る）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/query?q=SELECT+Id,Name,Amount,StageName,CloseDate+FROM+Opportunity+WHERE+IsClosed=false

Authorization: Bearer {access_token}
```

### Describe object （オブジェクトの説明）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/describe

Authorization: Bearer {access_token}
```

## CLI Commands （CLIコマンド）

```bash
# Authenticate
sf org login web

# Query records
sf data query --query "SELECT Id, Name FROM Account LIMIT 10"

# Create record
sf data create record --sobject Account --values "Name='New Account'"

# Deploy metadata
sf project deploy start

# Run Apex
sf apex run --file script.apex
```

## SOQL Examples （SOQL の例）

```sql
-- Get contacts with accounts
SELECT Id, Name, Email, Account.Name
FROM Contact
WHERE Account.Industry = 'Technology'

-- Get opportunities by stage
SELECT StageName, COUNT(Id)
FROM Opportunity
GROUP BY StageName

-- Get recent leads
SELECT Id, Name, Company, Status
FROM Lead
WHERE CreatedDate = LAST_N_DAYS:30
ORDER BY CreatedDate DESC
```

## Key Objects （主要なオブジェクト）

- **Lead** - Potential customer （**リード** - 潜在的な顧客）
- **Contact** - Person at account （**連絡先** - アカウント担当者）
- **Account** - Company/organization （**アカウント** - 会社/組織）
- **Opportunity** - Sales deal （**機会** - 販売取引）
- **Case** - Support ticket （**ケース** - サポート チケット）
- **Campaign** - Marketing campaign （**キャンペーン** - マーケティング キャンペーン）

## When to Use （いつ使用するか）

- Enterprise CRM operations （エンタープライズ CRM 運用）
- Complex sales processes （複雑な販売プロセス）
- Multi-object relationships （複数オブジェクトの関係）
- Custom object management （カスタムオブジェクト管理）
- Marketing campaign tracking （マーケティングキャンペーンの追跡）

## Rate Limits （レート制限）

- 15,000 API calls per 24 hours (Enterprise) （24 時間あたり 15,000 API コール (エンタープライズ)）
- Higher limits available （より高い制限も利用可能）

## Relevant Skills （関連するスキル）

- email-sequence （電子メールシーケンス）
- analytics-tracking （分析追跡）
- paid-ads （有料広告）
