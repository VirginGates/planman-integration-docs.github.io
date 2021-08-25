---
title: /api/v1/branches/:id/request-pilot
name: Request Pilot
position_number: 1.3
type: post
description: Requests a pilot for the branch specified by the requested ID and creates a new trip.
parameters:
  - name: 
    content: 
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true | The unique identifier of the branch. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | tripId | Long | The unique identifier of the created trip. |
  | taskId | Long | The unique identifier of the created task.  |
  | maxAllowedTasksCount | Integer | The maximum allowed number of tasks per trip. |

left_code_blocks:
  - code_block: |- 
      curl -X POST https://srvstg.virgingates.com/api/v1/branches/2165529378315486700/request-pilot -H "Authorization: Bearer $ACCESS_TOKEN"'
    title: cURL
    language: bash
right_code_blocks:
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


