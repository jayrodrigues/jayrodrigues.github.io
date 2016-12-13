# Social Login



## Resource

```
GET /users/social_login
```

## Parameters

| URI Parameter | Type   | Required | Description                                          |
|:--------------|:-------|:---------|:-----------------------------------------------------|
| site_lang     | string | yes      | en / fr                                              |
| first_name    | string | yes      |                                                      |
| last_name     | string | yes      |                                                      |
| gender        | int    | yes      | 0 = male / 1 = female                                |
| email         | string | yes      |                                                      |
| profile_img   | string | yes      | Required when signing up via social logins           |
| identifier    | string | yes      | Required when signing up via social logins           |
| provider      | string | yes      | provider(0 = Direct Login, 1 = Facebook, 2 = Google) |




## Example


### Request
***

```curl
curl -v -u 1971800d4d82861d8f2c1651fea4d212:api_token \
    -H "Content-Type: application/json" \
    -d '{"client":{"name":"Very Big Company","wid":777}}' \
    -X POST https://www.toggl.com/api/v8/clients
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
    "data": {
        "id":1239455,
        "wid":777,
        "name":"Very Big Company",
        "at":"2013-02-26T08:45:28+00:00"
    }
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
    "data": {
        "id":1239455,
        "wid":777,
        "name":"Very Big Company",
        "at":"2013-02-26T08:45:28+00:00",
        "notes": "Contact: John Jacob Jingleheimer Schmidt"
    }
}
```
