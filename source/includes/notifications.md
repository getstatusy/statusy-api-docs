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

### HTTP Request

`POST https://app.statusy.co/api/v1/APITOKEN/statuspage/STATUSPAGE_ID/subscriber/email/new`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
STATUSPAGE_ID | The numberic ID of the status page this incident belongs to.

### JSON Parameters

Parameter | Description
--------- | -----------
`email` | The email address notifications should be sent to
