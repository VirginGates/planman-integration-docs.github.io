---
title: /api/v1/branches/:id/sign-out
name: Sign Out
position_number: 1.1
type: post
description: Allows you to sign out using your branch ID.
content_markdown: |-
  __Path Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | id | Long | true | The unique identifier of the branch. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | id | Long | The unique identifier of the branch. |

left_code_blocks:
  - code_block: |- 
      curl -X POST https://srvstg.virgingates.com/business/api/v1/branches/2165529378315486700/sign-out -H "Authorization: Bearer $ACCESS_TOKEN" 
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": 2165529378315486700
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


