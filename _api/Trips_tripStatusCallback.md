---
title: /Caller/Provided/URL
name: Trip Status Callback
position_number: 1.8
type: patch
description: Caller systems should implement an API with the below request body (request body have extra parameters then the below but the below are the caller system concern) and provide it's URL while requesting Pilot.
content_markdown: |-
  __Body Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | tripId | Long | true | The unique identifier of the Trip. |
  | --- | --- | --- | --- |
  | tripStatus | String | true | The Trip new Status. |
  | --- | --- | --- | --- |
  | taskStatuses | List | true | List of the Tasks' statuses inside the Trip. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- | 
  | data | Map | Any data the could be used to assist the fleet operation. |


right_code_blocks:
  - code_block: |-
      {
          "tripId": 2165529378315486700,
          "tripStatus": "OPENED",
          "taskStatuses": [
            {
              "taskId": 2165529378315486700,
              "status": "COLLECTED"
            },
            {
              "taskId": 2165529378315486701,
              "status": "REACHED"
            }
          ]
      }
    title: Request
    language: json
  - code_block: |-
      {
          "data": {"example": {"ex1": 123}}
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


