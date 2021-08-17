---
title: /api/v1/trips/:id
name: Retrieve a Trip
position_number: 1.4
type: get
description: Returns various information about a single trip specified by the requested ID.
parameters:
  - name: 
    content: 
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true |  ......................... |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | id | Long | ........................ |
  | vendorBranch | Object | ........................ |
  | vendorBranch.id | Long | ........................ |
  | vendorBranch.label | String |  ........................  |
  | vendorBranch.vendorId | Long |  ........................  |
  | pilot | Object | ........................ |
  | pilot.id | Long | ........................ |
  | pilot.mobileNo | String | ........................ |
  | pilot.fullName | String | ........................ |
  | pilot.lastKnownLocation | Object | ........................ |
  | pilot.lastKnownLocation.type | String | ........................ |
  | pilot.lastKnownLocation.coordinates | Array | ........................ |
  | pilot.status | String |  ........................  |
  | status | String |  ........................  |
  | assignmentDate | String | ........................ |
  | creationDate | String | ........................ |
  | lastUpdateDate | String | ........................ |
  | routeDataEnriched | Boolean | ........................ |
  | eta | Integer | ........................ |
  | slaTier | String | ........................ |
  | maxAllowedTasksCount | Integer | ........................ |
  | requestedTasksCount | Integer | ........................ |
  | distanceInMeters | Integer | ........................ |
  | durationInSeconds | Integer | ........................ |
  | tasks | Array | ........................ |
  | tasks[0].id | Long | ........................ |
  | tasks[0].sequence | Integer | ........................ |
  | tasks[0].distanceInMeters | Integer | ........................ |
  | tasks[0].distanceFromLastTaskInMeters | Integer | ........................ |
  | tasks[0].durationInSeconds | Integer | ........................ |
  | tasks[0].durationSinceLastTask | Integer | ........................ |
  | tasks[0].pinnedDestinationPoint | Object | ........................ |
  | tasks[0].pinnedDestinationPoint.type | String | ........................ |
  | tasks[0].pinnedDestinationPoint.coordinates | Array | ........................ |
  | tasks[0].reachedDestinationDate | String | ........................ |
  | tasks[0].status | String | ........................ |
  | tasks[0].linkStatus | String | ........................ |
  | tasks[0].customer | Object | ........................ |
  | tasks[0].customer.id | Long | ........................ |
  | tasks[0].customer.addressId | Long | ........................ |
  | tasks[0].customer.mobileNo | String | ........................ |
  | hasOnlineOrder | Boolean | ........................ |
  

left_code_blocks:
  - code_block: |-
      curl "https://srvstg.virgingates.com/api/v1/trips/9921381276774878" -H "Authorization: Bearer $ACCESS_TOKEN"
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
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
        "creationDate": "2018-09-01T18:04:53.178Z",
        "lastUpdateDate": "2018-09-01T18:05:23.178Z",
        "routeDataEnriched": true,
        "eta": 600,
        "slaTier": "LESS_THAN_5_MINUTES",
        "maxAllowedTasksCount": 4,
        "requestedTasksCount": 4,
        "distanceInMeters": 3350,
        "durationInSeconds": 90,
        "tasks": [
          {
            "id": 9921381276774878,
            "sequence": 12,
            "distanceInMeters": 3350,
            "distanceFromLastTaskInMeters": 3350,
            "durationInSeconds": 90,
            "durationSinceLastTask": 90,
            "pinnedDestinationPoint": {
              "type": "Point",
              "coordinates": [
                -1.43,
                31.3
              ]
            },
            "reachedDestinationDate": "2018-09-01T18:04:53.178Z",
            "status": "REACHED",
            "linkStatus": "UNDECIDED",
            "customer": {
              "id": 2165529378315486700,
              "addressId": 2165529378315486700,
              "mobileNo": "01061239214"
            }
          }
        ],
        "hasOnlineOrder": false
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


