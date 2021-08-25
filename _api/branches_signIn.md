---
title: /api/v1/branches/sign-in
name: Sign In
position_number: 1.0
type: post
description: Allows you to sign in using your branch code and receive an access token, which is required for performing calls to other endpoints of the API.
parameters:
  - name: 
    content:
content_markdown: |-
  __Body Parameters__

  | Name | Type | Required | Description |
  | --- | --- | --- | --- |
  | code | String | true |  The unique sign in code defined for each branch. |

  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | id | Long | The unique identifier of the branch. |
  | label | String | The label (name) of the branch. |
  | code | String |  The unique sign in code defined for each branch. |
  | vendorId | Long | The unique identifier of the vendor. |
  | token | String | The bearer access token used for authenticating service calls made to other endpoints of the API. |

  You will be successfully authenticated and can perform calls to other endpoints.
  {: .success}

left_code_blocks:
  - code_block: |-
      curl -X POST https://srvstg.virgingates.com/api/v1/branches/sign-in -H "Content-type: application/json" -d '{"code": "1234567"}'
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "code": "147657930"
      }
    title: Request
    language: json
  - code_block: |-
      {
        "id": 2165529378315486700,
        "label": "Branch Label",
        "code": "147657930",
        "vendorId": 2165529378315486700,
        "token": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJKb2UifQ.1KP0SsvENi7Uz1oQc07aXTL7kpQG5jBNIybqr60AlD4"
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


