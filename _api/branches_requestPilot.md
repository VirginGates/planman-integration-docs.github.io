---
title: /api/v1/branches/:id/request-pilot
name: Request Pilot
position_number: 1.3
type: post
description: Requests a pilot for the branch specified by the requested ID and creates a new trip.
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true | The unique identifier of the branch. |

  __Body Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | deliveryLocation | PickupLocation | false |  The Delivery Location. |
  | --- | --- | --- | --- |
  | customerMobileNo | String | false |  Customer Mobile number. |
  | --- | --- | --- | --- |
  | value | MoneyWithCurrency | false |  task total amount. |
  | --- | --- | --- | --- |
  | vendorTaskId | String | false |  Vendor Order Id. |
  | --- | --- | --- | --- |
  | callbackURL | String | false |  URL for callback with status updates. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | tripId | Long | The unique identifier of the created trip. |
  | taskId | Long | The unique identifier of the created task.  |
  | maxAllowedTasksCount | Integer | The maximum allowed number of tasks per trip. |

left_code_blocks:
  - code_block: |- 
      curl -X POST https://srvstg.virgingates.com/business/api/v1/branches/2165529378315486700/request-pilot -H "Authorization: Bearer $ACCESS_TOKEN"
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "deliveryLocation": {
          "description": "Point",
          "point": {
            "type" : "Point", 
            "coordinates" : [
              31.0, 
              32.0
            ]
          } 
        },
        "customerMobileNo": "123123123",
        "value": {
          "amount": 300.0,
          "currency": "EGP"
        },
        "vendorTaskId": "123",
        "callbackURL": "http://callback.com"
      }
    title: Request 
    language: json
  - code_block: |-
      {
          "tripId": 9921381276774878,
          "taskId": 9921381276774878,
          "maxAllowedTasksCount": 3
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


