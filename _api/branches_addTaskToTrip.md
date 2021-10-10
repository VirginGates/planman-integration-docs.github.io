---
title: /api/v1/branches/:id/trips/:tripId/tasks
name: Add Task To Trip
position_number: 1.4
type: post
description: Add new task to existing branch trip.
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true | The unique identifier of the branch. |
  | --- | --- | --- | --- |
  | tripId | Long | true | The unique identifier of the trip. |

  __Body Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | zoneName | MultilingualString | false |  The Delivery Location zonename. |
  | --- | --- | --- | --- |
  | deliveryLocation | PickupLocation | false |  The Delivery Location. |
  | --- | --- | --- | --- |
  | customerMobileNo | String | false |  Customer Mobile number. |
  | --- | --- | --- | --- |
  | value | MoneyWithCurrency | false |  task total amount. |
  | --- | --- | --- | --- |
  | vendorTaskId | String | false |  Vendor Order Id. |

left_code_blocks:
  - code_block: |- 
      curl -X POST https://srvstg.virgingates.com/api/v1/branches/2165529378315486700/trips/2165529378315486700/tasks -H "Authorization: Bearer $ACCESS_TOKEN"
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "zoneName": {
          "en": "$lastAddedZoneNameEn",
          "ar": "$lastAddedZoneNameAr"
          },
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
      }
    title: Request
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


