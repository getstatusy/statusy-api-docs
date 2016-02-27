# Incidents

## Get all Incidents

```
curl https://statusy.co/api/v1/APITOKEN/incident/all
```

> The above command returns JSON structured like this:

```json
{
  "incidents": [
    {
      "created_date": "Fri, 26 Feb 2016 03:36:32 GMT",
      "description": "It is super broken!",
      "id": 1,
      "service_id": 2,
      "solved_date": "Fri, 26 Feb 2016 04:20:39 GMT",
      "title": "Oh man, fire, everywhere!",
      "updated_date": "Fri, 26 Feb 2016 03:36:32 GMT"
    },
    {
      "created_date": "Fri, 26 Feb 2016 03:36:32 GMT",
      "description": "It is super SUPER broken!",
      "id": 2,
      "service_id": 3,
      "solved_date": "Fri, 26 Feb 2016 04:20:39 GMT",
      "title": "Abandon ship!",
      "updated_date": "Fri, 26 Feb 2016 03:36:32 GMT"
    }
  ]
}
```

This endpoint returns the details of all incidents on your account.

### HTTP Request

`GET https://statusy.co/api/v1/APITOKEN/incident/all`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

<aside class="notice">
If <code>solved_date</code> is set in the response this incident has been resolved.
</aside>

## Get an Incident

```
curl https://statusy.co/api/v1/APITOKEN/incident
```

> The above command returns JSON structured like this:

```json
{
  "created_date": "Fri, 26 Feb 2016 03:36:32 GMT",
  "description": "It is super broken!",
  "id": 1,
  "service_id": 2,
  "solved_date": "Fri, 26 Feb 2016 04:20:39 GMT",
  "title": "Oh man, fire, everywhere!",
  "updated_date": "Fri, 26 Feb 2016 03:36:32 GMT"
}
```

This endpoint returns the details of all incidents on your account.

### HTTP Request

`GET https://statusy.co/api/v1/APITOKEN/incident`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

<aside class="notice">
If <code>solved_date</code> is set in the response this incident has been resolved.
</aside>


## Create an Incident

```
curl
 -X POST
 -H "Content-Type:application/json"
 -d '{"service_id": 2, "title": "Something broke!", "description": "Smoke, fire, everywhere!", "status": 2}'
 https://statusy.co/api/v1/APITOKEN/incident
```

> The above command returns JSON structured like this:

```json
{
  "incident_id": 2,
  "status": "success"
}
```

This endpoint allows you to create a new incident.

### HTTP Request

`POST https://statusy.co/api/v1/APITOKEN/incident`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

### JSON Parameters

Parameter | Description
--------- | -----------
`service_id` | The numeric ID of the service this incident is related to
`title` | The title of this incident
`description` | A long text description of the incident. Tell your users what is happening here.
`status` | This is a status enum representing the status of the service given this incident.

## Update an Incident

```
curl
 -X POST
 -H "Content-Type:application/json"
 -d '{"service_id": 2, "title": "Something broke!", "description": "Smoke, fire, everywhere!", "status": 2}'
 https://statusy.co/api/v1/APITOKEN/incident/INCIDENT_ID
```

> The above command returns JSON structured like this:

```json
{
  "incident_id": 1,
  "incident_update_id": 3,
  "status": "success"
}
```

This endpoint allows you to add an update to an existing incident.

### HTTP Request

`POST https://statusy.co/api/v1/APITOKEN/incident/INCIDENT_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
INCIDENT_ID | The numeric ID of the incident you want to add an update to.

### JSON Parameters

Parameter | Description
--------- | -----------
`service_id` | The numeric ID of the service this incident is related to
`title` | The title of this incident
`description` | A long text description of the incident. Tell your users what is happening here.
`status` | This is a status enum representing the status of the service given this incident.

<aside class="notice">
If <code>status</code> is provided and it is equal to 1 (enum for all good) this incident will be marked
as resolved. If you provide any other status code, the status will be updated to reflect the new status.
</aside>
