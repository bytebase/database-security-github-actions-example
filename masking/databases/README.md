## Database catalog for semantic type and classification

Docs:
  - Semantic type: https://www.bytebase.com/docs/security/data-masking/semantic-types/
  - Classification: https://www.bytebase.com/docs/security/data-masking/data-classification/#manual-classification

API: https://api.bytebase.com/#tag/databasecatalogservice/PATCH/v1/instances/%7Binstance%7D/databases/{database}/catalog

```bash
cd prod-sample-instance/hr_prod
curl --request PATCH ${bytebase_url}/v1/instances/prod-sample-instance/databases/hr_prod/catalog \
  --header 'Authorization: Bearer '${bytebase_token} \
  --data @database-catalog.json
```
