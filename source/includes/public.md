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
    "incidents": [
      {
        "created_date": "Tue, 20 Feb 2018 04:28:50 GMT",
        "created_date_iso": "2018-02-20T04:28:50.294807+00:00",
        "description": "test",
        "id": 4,
        "service_description": "API",
        "service_id": 1,
        "solved_date": null,
        "status": "Degraded Performance",
        "status_enum": 2,
        "statuspage_subdomain": "test",
        "title": "test",
        "updated_date": "Tue, 20 Feb 2018 04:28:50 GMT",
        "updated_date_iso": "2018-02-20T04:28:50.294832+00:00",
        "url": "http://justastatuspage.statusy.co/incident/4"
      },
    ],
    "maintenance": [
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
            "description": "Foo",
            "id": 2,
            "updated_date": "Mon, 09 Apr 2018 04:38:07 GMT"
          }
        ],
        "url": "http://justastatuspage.statusy.co/maintenance/2"
      },
    ],
    "services": [
      {
        "description": "OneService",
        "status": "Fully Operational",
        "status_obj": {
          "color": "#13BA74",
          "id": 1,
          "name": "Fully Operational",
          "text_color": "#FFFFFF",
          "weight": 1
        },
        "service_obj": {
          "description": "Test",
          "id": 8,
          "status": {
            "color": "#13BA74",
            "id": 1,
            "name": "Fully Operational",
            "text_color": "#FFFFFF",
            "weight": 1
          },
          "status_page_id": 1,
          "subservices": []
        }
      },
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
