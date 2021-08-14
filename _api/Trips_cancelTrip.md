---
title: /api/v1/trips/:id/cancel
name: Cancel a Trip
position_number: 1.5
type: post
description: Cancels the trip specified by the requested ID.
path_parameters:
  - name: id
    content: Integer
body_parameters:
  - name: branchId
    content: Integer
  - name: cancellationReason
    content: String
content_markdown: |-

left_code_blocks:
  - code_block: |- 
        curl -X POST https://srvbeta.virgingates.com/api/v1/trips/9921381276774878/cancel -H "Authorization: Bearer $ACCESS_TOKEN" -H "Content-type: application/json" -d '{"branchId": 2165529378315486700, "cancellationReason": "Order Taking Too Long"}'
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
          "tripStatus": "CANCELLED"
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


