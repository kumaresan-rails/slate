---
title: API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='#'>Documentation Powered by Duplii</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Dupliii API! You can use our API to access Duplii API endpoints, which can get information on users, leads and other details in our database.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: 44160e5187a1adc599fab593ccae7400"
```

> Make sure to replace `44160e5187a1adc599fab593ccae7400` with your API key.

Duplii expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: 44160e5187a1adc599fab593ccae7400`

<aside class="notice">
You must replace <code>44160e5187a1adc599fab593ccae7400</code> with your personal API key.
</aside>

# Users

## Create User

```shell
curl "http://api.duplii.com/v1/users/create_user"
  -H "Authorization: 44160e5187a1adc599fab593ccae7400"
```

> The above command returns JSON structured like this:

```json
  {
    "status": 200,
    "response": "User details created successfully!"
  }
```

This endpoint creates a new user.

### HTTP Request

`POST http://api.duplii.com/v1/users/create_user`

### Query Parameters

Parameter | Mandatory | Description
--------- | ------- | -----------
email | true | Email address for the new user.
first_name | true | First name of the user.
last_name | true | Last name of the user.
password | true | Password of the user.


## Update User


```shell
curl "http://api.duplii.com/v1/users/update_user"
  -H "Authorization: 44160e5187a1adc599fab593ccae7400"
```

> The above command returns JSON structured like this:

```json
{
  "status": 200,
  "response": "User details updated successfully!"
}
```

This endpoint updates the given user details.


### HTTP Request

`POST http://api.duplii.com/v1/users/update_user`

### Query Parameters

Parameter | Mandatory | Description
--------- | --------- | -----------
email | true | Email address for the update user
first_name | false | First name of the user.
last_name | false | Last name of the user.
password | false | Password of the user.

# Update Call Balance

```shell
curl "http://api.duplii.com/v1/update_call_balance"
  -H "Authorization: 44160e5187a1adc599fab593ccae7400"
```

### HTTP Request

`POST http://api.duplii.com/v1/update_call_balance`