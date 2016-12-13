# Ride Details

Retrieving details about a specific ride.

## Resource

```
GET /ride/ride_detail
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| site_lang     | string | yes      | en          |
| login_hash    | string | yes      |             |
| ride_hash     | string | yes      |             |

<!--Comments : search_from or search_to, either any of the one is only required.
Comments : (to_lat & to_lng) or (from_lat & from_lng), either any of the one is only required.
-->

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/ride/ride_detail?ride_hash=ca229fb61265f4dea8aa56243a248886&site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "rides": {
    "rides": [
      {
        "id": "46",
        "hash_key": "e92d798afa0718a6c2f30414b5bfcb23",
        "app_domain": "1",
        "user_id": "200",
        "frequency": "2",
        "flexibility": "00:15:00",
        "detour": "0",
        "round_trip": "1",
        "departure_time": "2016-03-23 11:08:00",
        "return_time": "2018-03-23 11:08:00",
        "departure_days": "1.2.3.4.5",
        "return_days": "1.2.3.4.5",
        "map_data": {
          "start": {
            "lng": "-65.0708682",
            "lat": "47.2553011",
            "address": "Neguac, NB, Canada"
          },
          "end": {
            "lng": "-64.9628356",
            "lat": "47.7897598",
            "address": "Caraquet, NB, Canada"
          },
          "waypoints": [
            {
              "location": "390 Murray Ave, Bathurst, NB E2A 1T3, Canada",
              "stopover": true
            }
          ],
          "stopovers": [
            {
              "lng": "-65.6497037",
              "lat": "47.6186509",
              "address": "390 Murray Ave, Bathurst, NB E2A 1T3, Canada",
              "en": "390 Murray Ave, Bathurst, NB E2A 1T3, Canada",
              "fr": "390 Rue Murray, Bathurst, NB E2A 1T3, Canada"
            }
          ]
        },
        "veh_id": "0",
        "seats_offered": "1",
        "luggage_per_seat": "0",
        "chatting": "0",
        "smoking": "0",
        "food": "0",
        "pets": "0",
        "music": "0",
        "women_only": "0",
        "handicapped": "0",
        "children": "0",
        "comment": "",
        "published": "1",
        "published_date": "0000-00-00 00:00:00",
        "auto_accept": "0",
        "step_completed": "1",
        "trashed": "0",
        "active": "1",
        "cancelled": "0",
        "cancellation_details": "",
        "created_date": "2016-03-23 21:08:51",
        "created_session_id": "200",
        "modified_date": "2016-03-23 21:08:51",
        "modified_session_id": "200",
        "ride_hash": "7f71e4d46fc13a1cb63944bbd2ad85f3",
        "ride_id": "31",
        "start_loc_en": "Neguac NB CA",
        "start_loc_fr": "Néguac NB CA",
        "start_point_en": "Neguac, NB, Canada",
        "start_point_fr": "Néguac, NB, Canada",
        "start_lat": "47.2553011",
        "start_lon": "-65.0708682",
        "end_loc_en": "Bathurst NB CA",
        "end_loc_fr": "Bathurst NB CA",
        "end_point_en": "390 Murray Ave, Bathurst, NB E2A 1T3, Canada",
        "end_point_fr": "390 Rue Murray, Bathurst, NB E2A 1T3, Canada",
        "end_lat": "47.6186509",
        "end_lon": "-65.6497037",
        "route_distance": "78520.00",
        "price_per_seat": "32.00",
        "waypoints": "71.72",
        "suggested_price": "32.00",
        "position": "1",
        "waypoint_id": "46",
        "waypoint_key": "e92d798afa0718a6c2f30414b5bfcb23",
        "date_key": "7f71e4d46fc13a1cb63944bbd2ad85f3",
        "is_return": "0",
        "unix_depature_time": "1458731280",
        "unix_return_time": "1521803280",
        "unix_start_date": "1481717280",
        "unix_end_date": "1481720707",
        "diver_first_name": "Henry J",
        "diver_last_name": "Driver",
        "profile_pic": "thumb_640.png",
        "social_login": "0",
        "gender": "1",
        "seats_available": "1",
        "user_hash": "9c62f33ad26eec8cb3b04f3a92bac7bd",
        "from_distance": "2945.4971898053595",
        "to_distance": "2897.6394282316105"
      }
    ],
    "one_off": 0,
    "regular": 1,
    "total": 1,
    "women_only": 0
  },
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```
#### Current

```json
{
  "message": "Please send valid data",
  "status": "",
  "ride_data": {}
}
```

#### Ideal

Depending on the data returned, the response when there is no data should look similar to the following.

Depending on the parameter, the empty result should be identified by the proper data type.

```json
{
  "ride_data": {
    "cur_language": "en",
    "ride": {},
    "waypoints": [{}],
    "hash_key": "7eb4b85147b80781934a194f0ddaf784",
    "driver_details": {},
    "booked_users": [],
    "vehicle": {},
    "is_booked": true,
    "ride_offerd": 0,
    "rating_datas": [],
    "count_active_rides": 0,
    "usergroup": "100"
  },
  "status": true
}
```
