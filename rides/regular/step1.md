# Offer Ride - Regular - Step 1

This endpoint is used for Offering a Regular Ride for Step 1

## Resource

```
POST /ride/offer_ride
```

## Parameters

| URI Parameter                   | Type     | Required | Description |
|:--------------------------------|:---------|:---------|:------------|
| site_lang                       | String   | Yes         |             |
| login_hash                      | String   | Yes         |             |
| step                            | String |Yes| route                          |
| ride_data[depature_date]        | String   |          |             |
| ride_data[depature_days]        | Int   |          |             |
| ride_data[depature_time]        | Datetime |          |             |
| end[address]                    | String   |          |             |
| end[lat]                        | String   |          |             |
| end[lng]                        | String   |          |             |
| ride_data[flexibility]          | Int      |          |             |
| ride_data[frequency]            | String |Yes| regular                
| ride_data[process]              | Int      |          |             |
| ride_data[regular_begining_from] | Datetime |          |             |
| ride_data[regular_departure_time] | Datetime |          |             |
| ride_data[regular_flexibility]  | Int      |          |             |
| ride_data[regular_return]  | string      |          |             |
| ride_data[regular_return_departure_time]  | Datetime      |          |             |
| ride_data[regular_until]  | Datetime      |          
| ride_data[return_days]  | Int      |          
| ride_data[return_depature_date] | String   |          |             |
| ride_data[return_depature_time] | Datetime |          |             |
| route[distance]                 | Int      |          |             |
| route[duration]                 | Int      |          |             |
| end[address]                    | String   |          |             |
| end[lat]                        | String   |          |             |
| end[lng]                        | String   |          |             |
| start[address]                  | String   |          |             |
| start[lat]                      | String   |          |             |
| start[lng]                      | String   |          |             |
| route[distance]                 | Int      |          |             |
| route[duration]                 | Int      |          |             |
| end[address]                    | String   |          |             |
| end[lat]                        | String   |          |             |
| end[lng]                        | String   |          |             |
| start[address]                  | String   |          |             |
| start[lat]                      | String   |          |             |
| start[lng]                      | String   |          |             |
| start[address]                  | String   |          |             |
| start[lat]                      | String   |          |             |
| start[lng]                      | String   |          |             |
| stopover[address]               | String   |          |             |
| stopover[lat]                   | String   |          |             |
| stopover[lng]                   | String   |          |             |
| total_distance                  | Int      |          |             |
| total_duration                  | Int      |          |             |
| waypoints[location]             | String   |          |             |
| waypoints[stopover]             | String   |          |             |



## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/offer_ride?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&step=route&ride_data[depature_date]=20-12-2016&ride_data[depature_days]=[1%2C%202%2C%204]&ride_data[depature_time]=9:00&end[address]=Burlington%2C%20ON%2C%20Canada&end[lat]=43.325520&end[lng]=-79.799032&ride_data[flexibility]=00:00:00&ride_data[frequency]=regular&ride_data[process]=1&ride_data[regular_begining_from]=20-12-2016&ride_data[regular_departure_time=9:00&ride_data[regular_flexibility]=00:00:00&ride_data[regular_return]=on&ride_data[regular_return_departure_time]=18:00&ride_data[regular_until]=28-12-2016&ride_data[return_days]=[1%2C3]&ride_data[return_depature_date]=&ride_data[return_depature_time]=14:50&route[distance]=50&route[duration]=60&end[address]=Burlington%2C%20ON%2C%20Canada&end[lat]=43.325520&end[lng]=-79.799032&start[address]=Toronto%2C%20ON%2C%20Canada&start[lat]=43.653226&start[lng]=-79.383184&route[distance]=57&route[duration]=81&end[address]=Burlington%2C%20ON%2C%20Canada&end[lat]=43.325520&end[lng]=-79.799032&start[address]=Toronto%2C%20ON%2C%20Canada&start[lat]=43.653226&start[lng]=-79.383184&start[address]=Burlington%2C%20ON%2C%20Canada&start[lat]=43.325520&start[lng]=-79.799032&stopover[address]=Brampton%2C%20ON%2C%20Canada&stopover[lat]=43.731548&stopover[lng]=-79.762418&total_distance=45&total_duration=40&waypoints[location]=Oakville%2C%20ON%2C%20Canada&waypoints[stopover]=true"
```

### Response
***

**Status-Code:**

```

```


### Error Responses
***
<!--
- No data aside from Login Hash and Site Language
- With Data entered
-->
**Status-Code:** ```200 OK```


```json
{
  "message": "Please send valid data.",
  "status": ""
}
```

<!--No Login Hash-->
**Status-Code:** ```200 OK```


```json
{
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```

<!--No Site Language-->
**Status-Code:** ```404 Not Found```


```
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>404 Not Found</title>
</head><body>
<h1>Not Found</h1>
<p>The requested URL /fr/api/message/unread was not found on this server.</p>
</body></html>
```
