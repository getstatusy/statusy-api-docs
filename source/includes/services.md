# Services

## Get all Services

## Get a Service

```
curl https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID
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

`GET https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to get

## Create a Service

```
curl
 -X POST
 -H "Content-Type:application/json"
 -d '{"description": "Website"}'
 https://statusy.co/api/v1/APITOKEN/service
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

`POST https://statusy.co/api/v1/APITOKEN/service`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

## Update a Service

```
curl
 -X PUT
 -H "Content-Type:application/json"
 -d '{"description": "Son of Website"}'
 https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID

```

> The above command returns JSON structured like this:

```json
{
  "status": "success"
}
```

This endpoint allows you to update the description of a particular service.

### HTTP Request

`PUT https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to update

## Delete a Service

```
curl
 -X DELETE
 -H "Content-Type:application/json"
 https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID

```

> The above command returns JSON structured like this:

```json
{
  "status": "success"
}
```

This endpoint allows you to delete an existing service.

### HTTP Request

`DELETE https://statusy.co/api/v1/APITOKEN/service/SERVICE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
SERVICE_ID | The numeric ID of the service you want to delete
