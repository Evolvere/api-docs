# Components

## Component object

```json
{
  "id": 54369,
  "siteId": 3393714,
  "clientId": 419010,
  "parentId": 3393714,
  "parentType": "SITE",
  "nodeId": "OB.001EC1111DC9.1",
  "name": "PV Meter",
  "nodeType": "METER",
  "application": "GENERATION",
  "generationType": "SOLAR",
  "oem": "Locus Energy",
  "model": "LGate 120",
  "isConceptualNode": false
}
```

### Attributes

Attribute | Type| Description | Always returned?
---|---|---|---
id | Integer | Unique identifier for the component | yes
siteId | Integer | Identifier for the parent site | yes
clientId | Integer | Identifier for the grandparent client | yes
parentId | Integer | Identifier for the parent. This could be the ID of a component or site depending upon the site hierarchy. | yes
parentType | String | Type of parent. This can be SITE or COMPONENT. | yes
nodeID | String | Unique MAC address of the physical device that this component represents. | yes
name | String | Component name | yes
nodeType | String | Type of component | yes
application | String | Use of component. Options are: GENERATION or NET-GRID | yes
generationType | String | Type of generation. Options are: SOLAR, WIND, THERMAL, OTHER, NET-GRID or EVSE | yes
oem | String | Original Equipment Manufacturer of the component | yes
model | String | Model name of the component | yes
isConceptualNode | boolean | Conceptual means non-monitored. If this component actually collects data, it is not conceptual. | yes

## Get component

> Example request:

```http
GET https://api.locusenergy.com/v3/components/54369 HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/components/54369
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
	"statusCode": 200,
	"id": 54369,
	"siteId": 3393714,
	"clientId": 419010,
	"parentId": 3393714,
	"parentType": "SITE",
	"nodeId": "OB.001EC1111DC9.1",
	"name": "PV Meter",
	"nodeType": "METER",
	"application": "GENERATION",
	"generationType": "SOLAR",
	"oem": "Locus Energy",
	"model": "LGate 120",
	"isConceptualNode": false
}
```

This endpoint retrieves a component object.

### Definition

`GET /v3/components/{componentId}`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
componentId | Unique identifier for the component | yes |

### Returns

Returns a [component object](#component-object).

## Get components for a site

> Example request:

```http
GET https://api.locusenergy.com/v3/sites/3393714/components HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/sites/3393714/components
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
  "statusCode": 200,
  "components": [
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 3393714,
      "parentType": "SITE",
      "nodeId": "OB.001EC1111DC9.1",
      "name": "PV Meter",
      "nodeType": "METER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Locus Energy",
      "model": "LGate 120",
      "isConceptualNode": false
    },
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 2050424,
      "parentType": "COMPONENT",
      "nodeId": "OB.TESTNODE.44",
      "name": "AE Inverter E1",
      "nodeType": "INVERTER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Advanced Energy",
      "model": "AE 500NX 480V",
      "isConceptualNode": false
    }
  ]
}
```

This endpoint retrieves components for a site.

### Definition

`GET /v3/sites/{siteId}/components`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
siteId | Unique identifier for the site | yes |

### Returns

Returns an array of [component objects](#component-object).

## Get components for a client

> Example request:

```http
GET https://api.locusenergy.com/v3/clients/419010/components HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/clients/419010/components
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
  "statusCode": 200,
  "components": [
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 3393714,
      "parentType": "SITE",
      "nodeId": "OB.001EC1111DC9.1",
      "name": "PV Meter",
      "nodeType": "METER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Locus Energy",
      "model": "LGate 120",
      "isConceptualNode": false
    },
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 2050424,
      "parentType": "COMPONENT",
      "nodeId": "OB.TESTNODE.44",
      "name": "AE Inverter E1",
      "nodeType": "INVERTER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Advanced Energy",
      "model": "AE 500NX 480V",
      "isConceptualNode": false
    }
  ]
}
```

This endpoint retrieves components for a client.

### Definition

`GET /v3/clients/{clientId}/components`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
clientId | Unique identifier for the client | yes |

### Returns

Returns an array of [component objects](#component-object).

## Get components for a partner

> Example request:

```http
GET https://api.locusenergy.com/v3/partners/123/components HTTP/1.1
Accept: application/json
Authorization: Bearer ACCESS_TOKEN
```

```shell
curl https://api.locusenergy.com/v3/partners/123/components
  -X GET
  -H "Accept: application/json"
  -H "Authorization: Bearer ACCESS_TOKEN"
```

> Example response:

```json
{
  "statusCode": 200,
  "components": [
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 3393714,
      "parentType": "SITE",
      "nodeId": "OB.001EC1111DC9.1",
      "name": "PV Meter",
      "nodeType": "METER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Locus Energy",
      "model": "LGate 120",
      "isConceptualNode": false
    },
    {
      "id": 54369,
      "siteId": 3393714,
      "clientId": 419010,
      "parentId": 2050424,
      "parentType": "COMPONENT",
      "nodeId": "OB.TESTNODE.44",
      "name": "AE Inverter E1",
      "nodeType": "INVERTER",
      "application": "GENERATION",
      "generationType": "SOLAR",
      "oem": "Advanced Energy",
      "model": "AE 500NX 480V",
      "isConceptualNode": false
    }
  ]
}
```

This endpoint retrieves components for a partner.

### Definition

`GET /v3/partners/{partnerId}/components`

### Arguments

Argument | Description | Required? | Default
--- | --- | --- | ---
partnerId | Unique identifier for the partner | yes |
nodeId | Node ID of component. A URL-encoded `%` will function as a wildcard in the search. | no |
notes | Value of note fields to search on. A URL-encoded `%` will function as wildcard in the search. | no |

### Returns

Returns an array of [component objects](#component-object).