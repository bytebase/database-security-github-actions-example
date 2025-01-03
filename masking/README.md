# Dynamic Data Masking

Docs: https://www.bytebase.com/docs/security/data-masking/overview/

Tutorials: [Data Masking with GitHub Actions](https://www.bytebase.com/docs/tutorials/github-action-data-masking-part1/)

## Workspace-level policies and settings

### Global masking rule

Docs: https://www.bytebase.com/docs/security/data-masking/global-masking-rule/

API: https://api.bytebase.com/#tag/orgpolicyservice/PATCH/v1/policies/{policy}

```bash
curl --request PATCH "${bytebase_url}/v1/policies/masking_rule?allow_missing=true&update_mask=payload" \
  --header 'Authorization: Bearer '${bytebase_token} \
  --data @global-masking-rule.json
```

### Data classification

Docs: https://www.bytebase.com/docs/security/data-masking/data-classification/

API: https://api.bytebase.com/#tag/settingservice/PATCH/v1/settings/{setting}

```bash
curl --request PATCH ${bytebase_url}/v1/settings/bb.workspace.data-classification \
  --header 'Authorization: Bearer '${bytebase_token} \
  --data @data-classification.json
```

### Masking algorithm

Docs: https://www.bytebase.com/docs/security/data-masking/masking-algorithm/

API: https://api.bytebase.com/#tag/settingservice/PATCH/v1/settings/{setting}

```bash
curl --request PATCH ${bytebase_url}/v1/settings/bb.workspace.masking-algorithm \
  --header 'Authorization: Bearer '${bytebase_token} \
  --data @masking-algorithm.json
```

### Semantic type

Docs: https://www.bytebase.com/docs/security/data-masking/semantic-types/

API: https://api.bytebase.com/#tag/settingservice/PATCH/v1/settings/{setting}

```bash
curl --request PATCH ${bytebase_url}/v1/settings/bb.workspace.semantic-types \
  --header 'Authorization: Bearer '${bytebase_token} \
  --data @semantic-type.json
```

## Project-level masking exception

Project-level masking exception to overrule the workspace-level setting.

https://github.com/bytebase/api-example/tree/main/data-security/masking/projects/project-sample

## Schema configuration

Configure metadata such as masking level, classification, semantic type at the table/column level.

https://github.com/bytebase/api-example/tree/main/data-security/masking/databases
