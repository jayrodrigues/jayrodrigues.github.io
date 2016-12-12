# Settings - Manage Vehicle

Endpoint to Add, Edit Vehicle Settings

## Resource

```
GET /settings/manage_veh
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
req_item			|string		| (add/edit)
site_lang			|string		|**[required]** en
login_hash			|string		|**[required]** <user hash key>
veh_data[ac]		  	|int	 	| optional
veh_data[bike_rack]		  	|int	 	| optional
veh_data[body_type]		|int  |
veh_data[co2_output]		|int  |
veh_data[color] |string | optional
veh_data[comfort_level] | int |
veh_data[distance_driven] | string |
veh_data[fuel_efficiency] | string |
veh_data[license_code] | string |
veh_data[license_number] | string |
veh_data[luggage] | int |
veh_data[make] | int |
veh_data[mileage] | int |
veh_data[mileage_checked] | int |
veh_data[model] | string |
veh_data[process] | int | (1=submitted 0=not submitted)
veh_data[seats] | string |
veh_data[ski_rack] | int | optional
veh_data[transmission] | int |
veh_data[transmission_checked] | int |
veh_data[tyre_type] | int |
veh_data[year] | string |
veh_id | string | if req_item = edit <id of the vehicles needs to update>

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/manage_veh?req_item=&site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&veh_data[ac]=&veh_data[bike_rack]=&veh_data[body_type]=&veh_data[co2_output]=&veh_data[color]=&veh_data[comfort_level]=&veh_data[distance_driven]=&veh_data[fuel_efficiency]=&veh_data[license_code]=&veh_data[license_number]=&veh_data[luggage]=&veh_data[make]=&veh_data[mileage]=&veh_data[mileage_checked]=&veh_data[model]=&veh_data[process]=&veh_data[seats]=&veh_data[ski_rack]=&veh_data[transmission]=&veh_data[transmission_checked]=&veh_data[tyre_type]=&veh_data[year]=&veh_id="
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Vehicle details added successfully.",
  "status": true,
  "vehicle_data": {
    "hash_key": "393190b9b8e5fbab9897d15104670579",
    "user_id": "351",
    "maker": "",
    "model": "",
    "year_built": "",
    "transmission": "",
    "mileage": "",
    "vehicle_image": "",
    "number_plate": "-",
    "color": "",
    "ac": "",
    "tyre_type": "",
    "distance_driven_per_year": "",
    "luggage_size": "",
    "seats": "",
    "comfort_level": "",
    "bike_rack": "",
    "ski_rack": "",
    "created_date": "2016-12-12 02:44:32",
    "modified_date": "2016-12-12 02:44:32",
    "modified_session_id": "351",
    "co2_output": "",
    "fuel_efficiency": "",
    "veh_body_type": "",
    "veh_id": 80
  }
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```

**Status-Code:** ```200 OK```

```json
{
  "message": "Vehicle with this license plate number already exist.",
  "status": ""
}
```
