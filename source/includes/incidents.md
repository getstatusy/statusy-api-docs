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
    }
  ]
}
```

This endpoint returns the details of all incidents on your account.

### HTTP Request

`GET https://statusy.co/api/v1/APITOKEN/incident/all`

<aside class="notice">
If <code>solved_date</code> is set in the response this incident has been resolved.
</aside>

## Get an Incident

## Update an Incident
