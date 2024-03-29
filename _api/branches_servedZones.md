---
title: /api/v1/branches/:id/served-zones
name: List Served Zones
position_number: 1.2
type: get
description: Retrieves a list of zones that are served by the branch specified by the requested ID.
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true | The unique identifier of the branch. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | branchLocation | Location | The location of the requested branch, returned as a Location object of type Point. |
  | hubLocation | Location | The location of the delivery hub that serves the requested branch, returned as a Location object of type Point.  |
  | zones | Array | An array of ZoneRateResponse objects. |

  __ZoneRateResponse__

  | Name | Type | Description |
  | --- | --- | --- |
  | zoneId | Long | The unique identifier of the zone. |
  | zoneName | MultilingualString | The name of the zone in english and arabic. |
  | rateName | String | The name of the pricing rate assigned to this zone. |
  | rateValue | MoneyWithCurrency | The value of the pricing rate assigned to this zone. |
  | polygon | Location | The location of the zone, returned as a Location object of type Polygon. |

left_code_blocks:
  - code_block: |-
      curl "https://srvstg.virgingates.com/business/api/v1/branches/2165529378315486700/served-zones" -H "Authorization: Bearer $ACCESS_TOKEN"
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "branchLocation": {
          "type": "Point",
          "coordinates": [
            -1.43,
            31.3
          ]
        },
        "hubLocation": {
          "type": "Point",
          "coordinates": [
            -1.43,
            31.3
          ]
        },
        "zones": [
          {
            "zoneId": 2165529378315486700,
            "zoneName": {
              "en": "El Merghany",
              "ar": "الميرغني"
            },
            "rateName": "rate1",
            "rateValue": {
              "amount": 31.01,
              "currency": "EGP"
            },
            "polygon": {
              "type": "Polygon",
              "coordinates": [
                [
                  -1.43,
                  31.3
                ]
              ]
            }
          }
        ]
      }
    title: Response
    language: json
  - code_block: |-
      {
        "stackTraceId": 2165529378315486700,
        "args": {
            "additionalProp1": {}
        },
        "devDetails": "string",
        "propagated": false,
        "trace": {
            "exceptionClass": "string",
            "message": "string",
            "stackTrace": [
                "string"
            ]
        },
        "code": "WebClientOperationException"
      }
    title: Error
    language: json
---


