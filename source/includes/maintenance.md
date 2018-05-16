# Maintenance

## Get all Maintenance Instances

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/maintenance/all
```

> The above command returns JSON structured like this:

```json
{
  "maintenance": [
    {
      "created_date": "Mon, 16 Apr 2018 03:12:23 GMT",
      "created_date_iso": "2018-04-16T03:12:23.020710+00:00",
      "description": "This is a maintenance",
      "end_date": "Wed, 12 Dec 1990 11:11:00 GMT",
      "id": 7,
      "service_description": "API",
      "service_id": 1,
      "start_date": "Wed, 12 Dec 1990 00:12:00 GMT",
      "statuspage_subdomain": "test",
      "title": "This is a threaded maintenance",
      "updated_date": "Mon, 16 Apr 2018 03:12:23 GMT",
      "updated_date_iso": "2018-04-16T03:12:23.020736+00:00",
      "updates": [
        {
          "created_date": "Mon, 16 Apr 2018 03:12:47 GMT",
          "description": "this is a maintenance update",
          "id": 3,
          "updated_date": "Mon, 16 Apr 2018 03:12:47 GMT"
        },
      ],
      "url": "http://test.statusy.co/maintenance/7"
    },
    {
      "created_date": "Wed, 11 Apr 2018 03:26:52 GMT",
      "created_date_iso": "2018-04-11T03:26:52.148906+00:00",
      "description": "test",
      "end_date": "Wed, 11 Apr 2018 22:26:30 GMT",
      "id": 6,
      "service_description": "API",
      "service_id": 1,
      "start_date": "Tue, 10 Apr 2018 22:26:28 GMT",
      "statuspage_subdomain": "test",
      "title": "Testasdasdasd",
      "updated_date": "Wed, 11 Apr 2018 03:26:52 GMT",
      "updated_date_iso": "2018-04-11T03:26:52.148934+00:00",
      "url": "http://test.statusy.co/maintenance/6"
    },
    {
      "created_date": "Wed, 11 Apr 2018 03:23:54 GMT",
      "created_date_iso": "2018-04-11T03:23:54.728377+00:00",
      "description": "test",
      "end_date": "Wed, 12 Dec 1212 00:12:00 GMT",
      "id": 3,
      "service_description": "Database",
      "service_id": 3,
      "start_date": "Wed, 12 Dec 1212 00:12:00 GMT",
      "statuspage_subdomain": "test",
      "title": "test",
      "updated_date": "Wed, 11 Apr 2018 03:23:54 GMT",
      "updated_date_iso": "2018-04-11T03:23:54.728399+00:00",
      "url": "http://test.statusy.co/maintenance/3"
    },
    {
      "created_date": "Mon, 09 Apr 2018 04:33:32 GMT",
      "created_date_iso": "2018-04-09T04:33:32.053706+00:00",
      "description": "this is a description",
      "end_date": "Tue, 10 Apr 2018 13:01:00 GMT",
      "id": 2,
      "service_description": "Database",
      "service_id": 3,
      "start_date": "Mon, 09 Apr 2018 01:01:00 GMT",
      "statuspage_subdomain": "test",
      "title": "Test maintenance",
      "updated_date": "Mon, 09 Apr 2018 04:33:32 GMT",
      "updated_date_iso": "2018-04-09T04:33:32.053732+00:00",
      "updates": [
        {
          "created_date": "Mon, 09 Apr 2018 04:38:07 GMT",
          "description": "update",
          "id": 2,
          "updated_date": "Mon, 09 Apr 2018 04:38:07 GMT"
        }
      ],
      "url": "http://test.statusy.co/maintenance/2"
    }
  ]
}
```

This endpoint returns the details of all maintenances on your account.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/maintenance/all`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numberic ID of the status page this maintenance belongs to.

## Get an Maintenance Event

```
curl https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/maintenance/MAINTENANCE_ID
```

> The above command returns JSON structured like this:

```json
{
  "created_date": "Mon, 16 Apr 2018 03:12:23 GMT",
  "created_date_iso": "2018-04-16T03:12:23.020710+00:00",
  "description": "This is a maintenance",
  "end_date": "Wed, 12 Dec 1990 11:11:00 GMT",
  "id": 7,
  "service_description": "API",
  "service_id": 1,
  "start_date": "Wed, 12 Dec 1990 00:12:00 GMT",
  "statuspage_subdomain": "test",
  "title": "This is a threaded maintenance",
  "updated_date": "Mon, 16 Apr 2018 03:12:23 GMT",
  "updated_date_iso": "2018-04-16T03:12:23.020736+00:00",
  "updates": [
    {
      "created_date": "Mon, 16 Apr 2018 03:12:47 GMT",
      "description": "this is a maintenance update",
      "id": 3,
      "updated_date": "Mon, 16 Apr 2018 03:12:47 GMT"
    },
  ],
  "url": "http://test.statusy.co/maintenance/7"
}
```

This endpoint returns the details of the specified maintenance event.

### HTTP Request

`GET https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/maintenance/MAINTENANCE_ID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page this incident belongs to.
MAINTENANCE_ID | The numeric ID of the maintenance event you want to view.
