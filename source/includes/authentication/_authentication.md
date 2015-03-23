# Authentication

## Authentication object

> Example response:

```json
{
    "access_token": "ef4ace9dc2574925b8708d05fbb9da7z",
    "issued_at": 1425672574,
    "expires_in": 3600
}
```

### Attributes

Attribute | Type| Description | Always returned?
---|---|---|---
access_token | String | Randomly generated string to serve as authentication token for subsequent requests | yes
issued_at | Integer | Unix timestamp for when `access_token` was issued | yes
expires_in | Integer | Seconds until the `access_token` expires | yes