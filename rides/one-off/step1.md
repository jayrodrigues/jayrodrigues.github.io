# Offer Ride - One-Off - Step 1

This endpoint is used for Offering a One-Off Ride for Step 1

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
| ride_data[process]              | Int      |          |             |
| ride_data[frequency]            | String |Yes| one-off               
| ride_data[depature_date]        | String   |          |             |
| ride_data[depature_time]        | Datetime |          |             |
| ride_data[return_depature_date] | String   |          |             |
| ride_data[return_depature_time] | Datetime |          |             |
| ride_data[flexibility]          | Int      |          |             |
| ride_data[regular_flexibility]  | Int      |          |             |
| ride_data[total_distance]       | Int      |          |             |
| ride_data[total_duration]       | Int      |          |             |
| start[lng]                      | String   |          |             |
| start[lat]                      | String   |          |             |
| start[address]                  | String   |          |             |
| end[lng]                        | String   |          |             |
| end[lat]                        | String   |          |             |
| end[address]                    | String   |          |             |
| route[start][lng]               | String   |          |             |
| route[start][lat]               | String   |          |             |
| route[start][address]           | String   |          |             |
| route[end][lng]                 | String   |          |             |
| route[end][lat]                 | String   |          |             |
| route[end][address]             | String   |          |             |
| route[distance]                 | Int      |          |             |
| route[duration]                 | Int      |          |             |
| start[lng]                      | String   |          |             |
| start[lat]                      | String   |          |             |
| start[address]                  | String   |          |             |
| end[lng]                        | String   |          |             |
| end[lat]                        | String   |          |             |
| end[address]                    | String   |          |             |
| distance                        | Int      |          |             |
| duration                        | Int      |          |             |
| stopover[lng]                   | String   |          |             |
| stopover[lat]                   | String   |          |             |
| stopover[address]               | String   |          |             |
| waypoints[location]             | String   |          |             |
| waypoints[stopover]             | String   |          |             |

## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/offer_ride?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&step=route&ride_data[process]=1&ride_data[frequency]=one-off&ride_data[depature_date]=20-12-2016&ride_data[depature_time]=8:00&ride_data[return_depature_date]=20-12-2016&ride_data[return_depature_time]=17:00:00&ride_data[flexibility]=00:00:00&ride_data[regular_flexibility]=00:00:00&ride_data[total_distance]=57&ride_data[total_duration]=60&start[lng]=-79.383184&start[lat]=43.653226&start[address]=Toronto%2C%20ON%2C%20Canada&end[lng]=-79.799032&end[lat]=43.325520&end[address]=Burlington%2C%20ON%2C%20Canada&route[start][lng]=-79.383184&route[start][lat]=43.653226&route[start][address]=Toronto%2C%20ON%2C%20Canada&route[end][lng]=-79.799032&route[end][lat]=43.325520&route[end][address]=Burlington%2C%20ON%2C%20Canada&route[distance]=68&route[duration]=81&start[lng]=-79.383184&start[lat]=43.653226&start[address]=Toronto%2C%20ON%2C%20Canada&end[lng]=-79.799032&end[lat]=43.325520&end[address]=Burlington%2C%20ON%2C%20Canada&distance=57&duration=60&stopover[lng]=-79.762418&stopover[lat]=43.731548&stopover[address]=Brampton%2C%20ON%2C%20Canada&waypoints[location]=Brampton%2C%20ON%2C%20Canada&waypoints[stopover]=true"
```

### Response
***

**Status-Code:**

```

```


### Error Responses
***
<!--No data aside from Login Hash and Site Language-->
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
