# Salesforce （日本語訳：セールスフォース）

Enterprise CRM platform for sales, service, and marketing. （日本語訳：販売、サービス、マーケティングのためのエンタープライズ CRM プラットフォーム。）

## Capabilities （日本語訳：能力）

| Integration（日本語訳：統合） | Available（日本語訳：利用可能） | Notes（日本語訳：注意事項） |
|-------------|-----------|-------|
| API（日本語訳：API） | ✓ | REST API, SOAP API, Bulk API（日本語訳：REST API、SOAP API、バルク API） |
| MCP（日本語訳：MCP） | - | Not available（日本語訳：利用不可） |
| CLI（日本語訳：CLI） | ✓ | Salesforce CLI (`sf`)（日本語訳：Salesforce CLI (`sf`)） |
| SDK（日本語訳：SDK） | ✓ | JSforce, simple-salesforce, etc.（日本語訳：JSforce、simple-salesforceなど） |

## Authentication （日本語訳：認証）

- **Type**: OAuth 2.0 (Web Server Flow or JWT Bearer) （日本語訳：**タイプ**: OAuth 2.0 (Web サーバー フローまたは JWT ベアラー)）
- **Header**: `Authorization: Bearer {access_token}` （日本語訳：**ヘッダー**: `Authorization: Bearer {access_token}`）
- **Instance URL**: Use instance_url from auth response （日本語訳：**インスタンス URL**: 認証応答からのinstance_urlを使用します。）

## Common Agent Operations （日本語訳：エージェントの共通操作）

### Query records (SOQL) （日本語訳：クエリレコード (SOQL)）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/query?q=SELECT+Id,Name,Email+FROM+Contact+LIMIT+10

Authorization: Bearer {access_token}
```

### Get record by ID （日本語訳：IDでレコードを取得）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/{record_id}

Authorization: Bearer {access_token}
```

### Create record （日本語訳：レコードの作成）

```bash
POST https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact

{
  "FirstName": "John",
  "LastName": "Doe",
  "Email": "john@example.com",
  "AccountId": "{account_id}"
}
```

### Update record （日本語訳：更新記録）

```bash
PATCH https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/{record_id}

{
  "Title": "Senior Developer"
}
```

### Search records (SOSL) （日本語訳：レコードの検索 (SOSL)）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/search?q=FIND+{searchTerm}+IN+ALL+FIELDS+RETURNING+Contact(Id,Name,Email)

Authorization: Bearer {access_token}
```

### Get opportunities （日本語訳：機会を得る）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/query?q=SELECT+Id,Name,Amount,StageName,CloseDate+FROM+Opportunity+WHERE+IsClosed=false

Authorization: Bearer {access_token}
```

### Describe object （日本語訳：オブジェクトの説明）

```bash
GET https://{instance}.salesforce.com/services/data/v59.0/sobjects/Contact/describe

Authorization: Bearer {access_token}
```

## CLI Commands （日本語訳：CLIコマンド）

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

## SOQL Examples （日本語訳：SOQL の例）

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

## Key Objects （日本語訳：主要なオブジェクト）

- **Lead** - Potential customer （日本語訳：**リード** - 潜在的な顧客）
- **Contact** - Person at account （日本語訳：**連絡先** - アカウント担当者）
- **Account** - Company/organization （日本語訳：**アカウント** - 会社/組織）
- **Opportunity** - Sales deal （日本語訳：**機会** - 販売取引）
- **Case** - Support ticket （日本語訳：**ケース** - サポート チケット）
- **Campaign** - Marketing campaign （日本語訳：**キャンペーン** - マーケティング キャンペーン）

## When to Use （日本語訳：いつ使用するか）

- Enterprise CRM operations （日本語訳：エンタープライズ CRM 運用）
- Complex sales processes （日本語訳：複雑な販売プロセス）
- Multi-object relationships （日本語訳：複数オブジェクトの関係）
- Custom object management （日本語訳：カスタムオブジェクト管理）
- Marketing campaign tracking （日本語訳：マーケティングキャンペーンの追跡）

## Rate Limits （日本語訳：レート制限）

- 15,000 API calls per 24 hours (Enterprise) （日本語訳：24 時間あたり 15,000 API コール (エンタープライズ)）
- Higher limits available （日本語訳：より高い制限も利用可能）

## Relevant Skills （日本語訳：関連するスキル）

- email-sequence （日本語訳：電子メールシーケンス）
- analytics-tracking （日本語訳：分析追跡）
- paid-ads （日本語訳：有料広告）
