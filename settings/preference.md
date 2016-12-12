# Settings - Preference

Endpoint to update the users Preferences in Settings.

## Resource

```
GET /settings/preference
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/preference?login_hash=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "pref_data": {
    "id": "206",
    "hash_key": "a8493b00f0f5bce773c7e58241cf945e",
    "user_id": "351",
    "chatting": "0",
    "smoking": "0",
    "food": "0",
    "pets": "0",
    "music": "0",
    "women_only": "0",
    "handicapped": "0",
    "children": "0"
  },
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Please send valid data.",
  "status": "",
  "pref_data": {}
}
```
