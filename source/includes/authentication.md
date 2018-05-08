# Authentication

```
curl -X POST
     -h "Content-Type:application/json"
     -d '{}'
     https://app.statusy.co/api/v1/APITOKEN/services
```

Statusy uses an in-line API token to authenticate each request you make to our
servers.

You can generate an unlimited use API token on the [profile page](https://app.statusy.co/dashboard/profile).

**Please note, your API token will be shown once for your security, be sure to note it
once it has been generated.**

If you lose your API token you should [delete it immediately](https://app.statusy.co/dashboard/profile/deactivate_api_token).
You can then [generate a new token](https://app.statusy.co/dashboardprofile/generate_api_token).

<aside class="notice">
Our examples use <code>APITOKEN</code> to indicate where you should add your API token.
</aside>
