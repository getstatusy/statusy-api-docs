# Status Pages

## Get Status Page

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGEID
```

> The above command returns JSON structured like this:

```json
{
  "google_analytics_token": null,
  "id": 10,
  "incidents": [],
  "is_active": true,
  "name": "AStatusPage",
  "services": [
    17,
    10,
    11,
    12,
    13,
    14,
    15,
    16
  ],
  "subdomain": "AStatusPage",
  "updated_date": "Fri, 27 May 2016 03:48:22 GMT"
}
```

This endpoint returns an object with the details of the request status page.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGEID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGEID | The ID of the status page you want to get

## Get all Status Pages

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspages
```

> The above command returns JSON structured like this:

```json
{
  "statuspages": [
    {
      "google_analytics_token": null,
      "id": 10,
      "incidents": [],
      "is_active": true,
      "name": "AStatusPage",
      "services": [
        17,
        10,
        11,
        12,
        13,
        14,
        15,
        16
      ],
      "subdomain": "AStatusPage",
      "updated_date": "Fri, 27 May 2016 03:48:22 GMT"
    },
    {
      "google_analytics_token": null,
      "id": 11,
      "incidents": [],
      "is_active": true,
      "name": "AnotherStatusPage",
      "services": [
        18
      ],
      "subdomain": "AnotherStatusPage",
      "updated_date": "Fri, 27 May 2016 03:54:52 GMT"
    }
  ]
}
```

This endpoint returns an array of all the status pages on your account.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspages`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

## Get all Statuses

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/statuses
```

> The above command returns JSON structured like this:

```json
{
  "statuses": [
    {
      "color": "#22A722",
      "id": 48,
      "name": "Fully Operational",
      "weight": 1
    },
    {
      "color": "#F58F0D",
      "id": 49,
      "name": "Degraded Performance",
      "weight": 2
    },
    {
      "color": "#FF0000",
      "id": 50,
      "name": "Major Outage",
      "weight": 3
    }
  ]
}
```

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/statuses`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The ID of the status page you want to view statuses for
