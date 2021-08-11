---
title: /api/v1/trips/:id
name: Retrieve a Trip
position_number: 1.4
type: get
description: Retreive the trip's info using id
path_parameters:
  - name: id
    content: Integer
content_markdown: |-
  The trip's info will be displayed.
  {: .success}

  Sign in as a branch user.
left_code_blocks:
  - code_block: |-
      curl "https://srvbeta.virgingates.com/api/v1/trips/9921381276774878" -H "Authorization: Bearer $ACCESS_TOKEN"
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


