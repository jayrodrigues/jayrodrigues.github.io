# License Verify

Common Function to check whether an user licence verified

## Resource

```
GET /users/lic_verify
```

## Parameters

| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| hash_key      | string | yes      |             |


## Example


### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/lic_verify?hash_key=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "status": 0
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "status": "Please send valid data."
}
```
