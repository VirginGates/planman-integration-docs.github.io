---
title: /api/v1/trips
name: List Trips
position_number: 1.5
type: get
description: Returns various information about multiple trips filtered by criteria and/or sorted by one of trips's properties in ascending/descending order.
parameters:
  - name: 
    content:
content_markdown: |-
  __Query Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | criteria | String | true |  ......................... |
  | sortBy | String | true |  ......................... |
  | sortType | String | true |  ......................... |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | id | Integer | ........................ |
  | vendorBranch | Object | ........................ |
  | vendorBranch.id | Integer | ........................ |
  | vendorBranch.label | String |  ........................  |
  | vendorBranch.vendorId | Integer |  ........................  |
  | pilot | Object | ........................ |
  | pilot.id | Integer | ........................ |
  | pilot.mobileNo | String | ........................ |
  | pilot.fullName | String | ........................ |
  | pilot.lastKnownLocation | Object | ........................ |
  | pilot.lastKnownLocation.type | String | ........................ |
  | pilot.lastKnownLocation.coordinates | Array | ........................ |
  | pilot.status | String |  ........................  |
  | status | String |  ........................  |
  | assignmentDate | String | ........................ |
  | pendingCollectionDate | String | ........................ |
  | creationDate | String | ........................ |
  | eta | Integer | ........................ |
  | slaTier | String | ........................ |
  | maxAllowedTasksCount | Integer | ........................ |
  | requestedTasksCount | Integer | ........................ |
  
  Returns a maximum of 800 trips.
  {: .info }

left_code_blocks:
  - code_block: |-
      curl "https://srvbeta.virgingates.com/api/v1/trips?sortType=asc&criteria={"vendorBranchId":1440482015196672,"status":["CANCELLED"]}&sortBy="  -H "Authorization: Bearer $ACCESS_TOKEN"
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


