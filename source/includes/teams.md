# Teams

## Get all Users on a Team

```
curl
https://app.statusy.co/api/v1/APITOKEN/team
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "message": "team members successfully pulled",
  "team": [
    {
      "id": 1,
      "email": "demo@email.com",
    },
  ]
}
```

This endpoint returns the details of all users who are part of your team.

### HTTP Request

`GET
https://app.statusy.co/api/v1/APITOKEN/team`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

## Invite User to a Team

```
curl
 -X POST
 -H "Content-Type:application/json"
 -d '{"email": "demo@email.com"}'
 https://app.statusy.co/api/v1/APITOKEN/team
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "message": "user successfully invited"
}
```

This endpoint allows you to invite a user to your team. After making the above call, the user will receive an email to complete the sign up process.

### HTTP Request

`POST
https://app.statusy.co/api/v1/APITOKEN/team`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token

### JSON Parameters

Parameter | Description
--------- | -----------
`email` | The email address of the person you wish to add to your team

## Remove User from a Team

```
curl
 -X DELETE
 https://app.statusy.co/api/v1/APITOKEN/team/USERID
```

> The above command returns JSON structured like this:

```json
{
  "status": "success",
  "message": "user successfully deleted"
}
```

This endpoint allows you to remove a user from your team.

### HTTP Request

`DELETE
https://app.statusy.co/api/v1/APITOKEN/team/USERID`

### URL Parameters

Parameter | Description
--------- | -----------
APITOKEN | Your API token
USERID | The ID of the user you want to remove
