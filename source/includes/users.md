# Users

## Get details of User making request

```
curl
https://app.statusy.co/api/v1/APITOKEN/me
```

> The above command returns JSON structured like this:

```json
{
  "created_date": "Mon, 19 Feb 1958 02:00:13 GMT",
  "email": "ddraper@example.com",
  "first_name": "Don",
  "is_confirmed": true,
  "last_name": "Draper"
}
```

This endpoint returns the details of the user making the request.

### HTTP Request

`GET
https://app.statusy.co/api/v1/APITOKEN/me`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
