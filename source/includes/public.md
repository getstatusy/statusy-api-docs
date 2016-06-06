# Public Data

## Public Status Page Status

```
curl
 https://app.statusy.co/api/v1/public/statuspage/STATUSPAGE_SUBDOMAIN

```

> The above command returns JSON structured like this:

```json
{
  "statuspage": {
    "id": "7",
    "name": "JustAStatusPage",
    "overall_status": "Fully Operational",
    "services": [
      {
        "description": "OneService",
        "status": "Fully Operational"
      },
      {
        "description": "TwoService",
        "status": "Fully Operational"
      },
      {
        "description": "ThreeService",
        "status": "Fully Operational"
      },
      {
        "description": "FourService",
        "status": "Fully Operational"
      }
    ],
    "subdomain": "justastatuspage"
  }
}
```

This endpoint returns the overall status and individual service statuses of a public status page.

### HTTP Request

`GET https://app.statusy.co/api/v1/public/statuspage/STATUSPAGE_SUBDOMAIN`

### URL Parameters

Parameter | Description
--------- | -----------
STATUSPAGE_SUBDOMAIN | The subdomain of the status page you want the status of.
