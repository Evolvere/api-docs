# Events

## Event object

> Example response:

```json
{
    "componentId": 2084618,
    "componentName": "ATI Tracker B63TC102",
    "start": "2015-01-29T04:00:00-08:00",
    "end": "2015-01-29T09:00:00-08:00",
    "eventType": "disconnect",
    "eventStatus": "Closed",
    "priority": "High",
    "description": "System Disconnected",
    "starttime": "2015-01-29 04:00:00",
    "fullname": "McKenzie, CA",
    "id": -1468039263
}
```

### Attributes

Attribute | Type| Description | Always returned?
---|---|---|---
id | Integer | Unique identifier for the event | yes
componentId | Integer | Unique identifier for the component | yes
componentName | String | Name of the component | yes
start | String (datetimestamp) | Start time of the event | yes
end | String (datetimestamp) | End time of the event | no
eventType | String | Type of the event | yes
eventStatus | String | Current status of the event | yes
priority | String | Priority of the event | yes
description | String | Description of the event | yes
starttime | String | Another format of the starttime... | yes

## Get events for a client

> Example request:

```http
GET https://api.locusenergy.com/v3/clients/{clientId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/clients/{clientId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
    "statusCode": 200,
    "events": [
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-29T04:00:00-08:00",
            "end": "2015-01-29T09:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-29 04:00:00",
            "fullname": "McKenzie, CA",
            "id": -1468039263
        },
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-27T18:00:00-08:00",
            "end": "2015-01-28T10:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-27 18:00:00",
            "fullname": "McKenzie, CA",
            "id": 2041705905
        }
    ]
}
```

This endpoint retrieves events for a site.

### Definition

`GET /v3/clients/{clientId}/events`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
start | The start of the time period | yes |
end | The end of the time period | yes |
tz | The timezone for the time period | no | UTC
priority | Comma-delimited list of priorities. Options are high, medium and low. | no | high,medium,low
status | Comma-delimited list of statuses. Options are open and closed. | no | open,closed

### Returns

Returns an array of [event objects](#event-object).

## Get events for a site

> Example request:

```http
GET https://api.locusenergy.com/v3/clients/{clientId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/clients/{clientId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
    "statusCode": 200,
    "events": [
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-29T04:00:00-08:00",
            "end": "2015-01-29T09:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-29 04:00:00",
            "fullname": "McKenzie, CA",
            "id": -1468039263
        },
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-27T18:00:00-08:00",
            "end": "2015-01-28T10:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-27 18:00:00",
            "fullname": "McKenzie, CA",
            "id": 2041705905
        }
    ]
}
```

This endpoint retrieves events for a site.

### Definition

`GET /v3/sites/{siteId}/events`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
start | The start of the time period | yes |
end | The end of the time period | yes |
tz | The timezone for the time period | no | UTC
priority | Comma-delimited list of priorities. Options are high, medium and low. | no | high,medium,low
status | Comma-delimited list of statuses. Options are open and closed. | no | open,closed

### Returns

Returns an array of [event objects](#event-object).

## Get events for a component

> Example request:

```http
GET https://api.locusenergy.com/v3/components/{componentId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/components/{componentId}/events?start=2015-01-28T04:00:00&end=2015-01-30T09:00:00&tz=US/Pacific
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
    "statusCode": 200,
    "events": [
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-29T04:00:00-08:00",
            "end": "2015-01-29T09:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-29 04:00:00",
            "fullname": "McKenzie, CA",
            "id": -1468039263
        },
        {
            "componentId": 2084618,
            "componentName": "ATI Tracker B63TC102",
            "start": "2015-01-27T18:00:00-08:00",
            "end": "2015-01-28T10:00:00-08:00",
            "eventType": "disconnect",
            "eventStatus": "Closed",
            "priority": "High",
            "description": "System Disconnected",
            "starttime": "2015-01-27 18:00:00",
            "fullname": "McKenzie, CA",
            "id": 2041705905
        }
    ]
}
```

This endpoint retrieves events for a component.

### Definition

`GET /v3/components/{componentId}/events`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
start | The start of the time period | yes |
end | The end of the time period | yes |
tz | The timezone for the time period | no | UTC
priority | Comma-delimited list of priorities. Options are high, medium and low. | no | high,medium,low
status | Comma-delimited list of statuses. Options are open and closed. | no | open,closed

### Returns

Returns an array of [event objects](#event-object).