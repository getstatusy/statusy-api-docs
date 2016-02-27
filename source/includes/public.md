# Public Data

## Service Status Enums

```
curl
 https://statusy.co/api/v1/public/status/enums

```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "status_enums": [
    {
      "1": "Fully Operational"
    },
    {
      "2": "Degraded Performance"
    },
    {
      "3": "Major Performance"
    }
  ]
}
```

This endpoint returns all possible enums for the service status.

### HTTP Request

`GET https://statusy.co/api/v1/public/status/enums`
