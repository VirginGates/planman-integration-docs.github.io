---
title: /api/v1/branches/:id/request-pilot
name: Request a Pilot
position_number: 1.3
type: post
description: Requests a pilot for the branch specified by the requested ID and creates a new trip.
path_parameters:
  - name: id
    content: Integer
content_markdown: |-

left_code_blocks:
  - code_block: |- 
      curl -X POST https://srvbeta.virgingates.com/api/v1/branches/2165529378315486700/request-pilot -H "Authorization: Bearer $ACCESS_TOKEN"'
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


