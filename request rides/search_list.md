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
| from_distance | string |          |             |
| from_lat      | string |          |             |
| from_lng      | string |          |             |
| price_from    | string |          |             |
| price_to      | string |          |             |
| search_date   | string |          |             |
| search_from   | string |          |             |
| search_to     | string |          |             |
| sort_by       | string |          |             |
| proximity     | string |          |             |
| start_time    | string |          |             |
| to_distance   | string |          |             |
| to_lat        | string |          |             |
| to_lng        | string |          |             |

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
