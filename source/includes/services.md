# Services

## Get all Services

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/all
```

> The above command returns JSON structured like this:

```json
{
  "services": [
    {
      "id": 1,
      "account_id": 1,
      "description": "Service",
      "status_enum": 1
    },
    {
      "id": 2,
      "account_id": 1,
      "description": "Another Service",
      "status_enum": 1
    },
    {
      "id": 3,
      "account_id": 1,
      "description": "Yet Another Service",
      "status_enum": 1
    }
  ]
}
```

This endpoint returns the details of all services on your account.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/all`

## Get a Service

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID
```

> The above command returns JSON structured like this:

```json
{
  "account_id": 1,
  "description": "Website",
  "status_enum": 1
}
```

This endpoint returns the details of a specific service.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to get
STATUSPAGE_ID | The numeric ID of the status page the service belongs to

## Create a Service

```
curl
 -X POST
 -H "Content-Type:application/json"
 -d '{"description": "Website"}'
 https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service
```

> The above command returns JSON structured like this:

```json
{
  "service_id": 6,
  "status": "success"
}
```

This endpoint allows for the creation of a new service.

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page the service belongs to

### JSON Parameters

Parameter | Description
--------- | -----------
`description` | The description is the title of the service, for example "Website" or "Database".

## Update a Service

```
curl
 -X PUT
 -H "Content-Type:application/json"
 -d '{"description": "Son of Website"}'
 https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID

```

> The above command returns JSON structured like this:

```json
{
  "status": "success"
}
```

This endpoint allows you to update the description of a particular service.

### HTTP Request

`PUT https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to update
STATUSPAGE_ID | The numeric ID of the status page the service belongs to

### JSON Parameters

Parameter | Description
--------- | -----------
`description` | The description is the title of the service, for example "Website" or "Database".

## Delete a Service

```
curl
 -X DELETE
 -H "Content-Type:application/json"
 https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID

```

> The above command returns JSON structured like this:

```json
{
  "status": "success"
}
```

This endpoint allows you to delete an existing service.

### HTTP Request

`DELETE https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to delete
STATUSPAGE_ID | The numeric ID of the status page the service belongs to
