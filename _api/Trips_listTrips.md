---
title: /api/v1/trips
name: List Trips
position_number: 1.6
type: get
description: Returns various information about multiple trips filtered by criteria and/or sorted by one of trips's properties in ascending/descending order.
content_markdown: |-
  __Query Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | criteria | String | true | Used for filtering the trips returned, for example criteria={"status":["CANCELLED"]} |
  | sortBy | String | true | Used for sorting the trips returned based on one of the trip's properties. |
  | sortType | String | true | Indicates whether sorting will be done in ascending or descending order. |

  __Response Fields__

  Returns an array of trip objects with the following fields:

  | Name | Type | Description |
  | --- | --- | --- |
  | id | Long | The unique identifier of the trip. |
  | status | TripStatus |  The current status of the trip.  |
  | assignmentDate | String | The date the pilot was assigned to the trip. |
  | pendingCollectionDate | String | The date the tasks of the trip were ready for collection. |
  | creationDate | String | The date the trip was created. |
  | eta | Long | The estimated time of arrival of the pilot to the branch. |
  | slaTier | String | Refers to the time taken for the trip to be dispatched after it was created. |
  | maxAllowedTasksCount | Integer | The maximum allowed number of tasks per trip. |
  | requestedTasksCount | Integer | The number of tasks in the trip. |
  | vendorBranch | Branch | The branch from which the trip was initiated. |
  | pilot | Pilot | The pilot assigned to the trip. |

  Returns a maximum of 800 trips.
  {: .info }

left_code_blocks:
  - code_block: |-
      curl "https://srvstg.virgingates.com/business/api/v1/trips?sortType=asc&criteria={"vendorBranchId":1440482015196672,"status":["CANCELLED"]}&sortBy="  -H "Authorization: Bearer $ACCESS_TOKEN"
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
          "id": 9921381276774878,
          "vendorBranch": {
            "id": 2165529378315486700,
            "label": "Branch1",
            "vendorId": 2165529378315486700
          },
          "pilot": {
            "id": 2165529378315486700,
            "mobileNo": "0102312381",
            "fullName": "Name",
            "lastKnownLocation": {
              "type": "Point",
              "coordinates": [
                -1.43,
                31.3
              ]
            },
            "status": "UNAVAILABLE"
          },
          "status": "CANCELLED",
          "assignmentDate": "2018-09-01T18:04:53.178Z",
          "pendingCollectionDate": "2018-09-01T18:04:53.178Z",
          "creationDate": "2018-09-01T18:04:53.178Z",
          "eta": 600,
          "slaTier": "LESS_THAN_5_MINUTES",
          "maxAllowedTasksCount": 4,
          "requestedTasksCount": 4
        }
      ]
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


