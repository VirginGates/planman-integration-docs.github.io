---
title: /api/v1/trips/:id/cancel
name: Cancel Trip
position_number: 1.7
type: post
description: Cancels the trip specified by the requested ID. Trip status must not be "OPENED".
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true |  The unique identifier of the trip. |

  __Body Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | branchId | Long | true | The unique identifier of the branch. |
  | cancellationReason | String | true | The reason for the trip cancellation. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- | 
  | tripStatus | TripStatus | The updated status of the trip. |

left_code_blocks:
  - code_block: |- 
        curl -X POST https://srvstg.virgingates.com/business/api/v1/trips/9921381276774878/cancel -H "Authorization: Bearer $ACCESS_TOKEN" -H "Content-type: application/json" -d '{"branchId": 2165529378315486700, "cancellationReason": "Order Taking Too Long"}'
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
          "branchId": 2165529378315486700,
          "cancellationReason": "Order Taking Too Long"
      }
    title: Request
    language: json
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


