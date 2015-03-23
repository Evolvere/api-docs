# Data

## Data object

```json
{
  "id": 123,
  "ts": "2014-04-01T12:00:00-07:00",
  "W_avg": 23.717,
  "Wh_sum": 5936
}
```

### Attributes

Attribute | Type| Description | Always returned?
---|---|---|---
id | Integer | Corresponds to the entity ID for which this data was requested | yes
ts | String (datetimestamp) | Datetimestamp for this data point | yes

For each `data` object, any non-null data is returned with the field name. In this example, `W_avg` and `Wh_sum` were requested.