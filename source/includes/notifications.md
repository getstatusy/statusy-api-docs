# Notifications

## Add Email Subscriber

```
curl
  -X POST
  -H "Content-Type: application/json"
  -d '{"email":"anemail@adomain.com"}'
  https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/new
```

> The above command returns JSON structured like this:

```json
{
  "email": "anemail@adomain.com",
  "notification_id": 21,
  "status": "success"
}
```

This endpoint allows you to add a new email subscriber to your status page. The email you provide will receive email notifications when the status of your service(s) has changed.

You can optionally specify the `service_id` or the `service_id` AND the `subservice_id` to the request to subscribe a user to the specified service or
service/subservice pair.

If you do not provide `service_id` or `subservice_id`, the user will be subscribed to _all_ services.

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/new`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page this subscriber should be added to

### JSON Parameters

Parameter | Description
--------- | -----------
`email` | The email address notifications should be sent to
`service_id` | (Optional) The ID of a service to subscribe this user to
`subservice_id` | (Optional) The ID of a subservice to subscribe this user to, `service_id` is also required if `subservice_id` is present

## Remove Email Subscriber

```
curl
  -X POST
  -H "Content-Type: application/json"
  -d '{"email":"anemail@adomain.com"}'
  https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/delete
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "message": "subscriber removed"
}
```

This endpoint allows you to remove an existing email subscriber from your status page.

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/delete`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page this subscriber belongs to

### JSON Parameters

Parameter | Description
--------- | -----------
`email` | The email address of subscriber to remove

## Add SMS Subscriber

```
curl
  -X POST
  -H "Content-Type: application/json"
  -d '{"phone":"5555555555"}'
  https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/sms/new
```

> The above command returns JSON structured like this:

```json
{
  "phone": "5555555555",
  "notification_id": 21,
  "status": "success"
}
```

This endpoint allows you to add a new SMS subscriber to your status page. The email you provide will receive SMS notifications when the status of your service(s) has changed.

You can optionally specify the `service_id` or the `service_id` AND the `subservice_id` to the request to subscribe a user to the specified service or
service/subservice pair.

If you do not provide `service_id` or `subservice_id`, the user will be subscribed to _all_ services.

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/sms/new`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page this subscriber should be added to

### JSON Parameters

Parameter | Description
--------- | -----------
`phone` | The phone number notifications should be sent to
`service_id` | (Optional) The ID of a service to subscribe this user to
`subservice_id` | (Optional) The ID of a subservice to subscribe this user to, `service_id` is also required if `subservice_id` is present

## Remove SMS Subscriber

```
curl
  -X POST
  -H "Content-Type: application/json"
  -d '{"phone":"5555555555"}'
  https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/sms/delete
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "message": "subscriber removed"
}
```

This endpoint allows you to remove an existing email subscriber from your status page.

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/delete`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numeric ID of the status page this subscriber belongs to

### JSON Parameters

Parameter | Description
--------- | -----------
`phone` | The phone number notifications should be sent to
