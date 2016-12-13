# Search List

Endpoint used for searching

## Resource

```
GET /search/list
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| site_lang     | string | yes      | en          |
| end_time      | string |          |             |
| frequency     | string |          |             |
| from_distance | string | optional |             |
| from_lat      | string | optional |             |
| from_lng      | string | optional |             |
| price_from    | string |          |             |
| price_to      | string |          |             |
| search_date   | string | optional |             |
| search_from   | string | optional |             |
| search_to     | string | optional |             |
| sort_by       | string | optional |             |
| proximity     | string | optional |             |
| start_time    | string |          |             |
| to_distance   | string |          |             |
| to_lat        | string | optional |             |
| to_lng        | string | optional |             |

<!--Comments : search_from or search_to, either any of the one is only required.
Comments : (to_lat & to_lng) or (from_lat & from_lng), either any of the one is only required.
-->

## Example

### Request
***

```curl

```

### Response
***

**Status-Code:** ```200 OK```

```json

```


### Error Responses
***

**Status-Code:** ```200 OK```


```json

```

**Status-Code:** ```200 OK```

```json

```
