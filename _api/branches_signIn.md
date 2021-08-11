---
title: /api/v1/branches/sign-in
name: Sign In
position_number: 1.0
type: post
description: Sign In
body_parameters:
  - name: code
    content: String
  - name: notificationToken
    content: String
content_markdown: |-
  The branch user will be successfully authenticated
  {: .success}

  Sign in as a branch user.
left_code_blocks:
  - code_block: |-
      curl -X POST https://srvbeta.virgingates.com/api/v1/branches/sign-in -H "Content-type: application/json" -d '{"code": "1234567", "notificationToken": "cjNFU9Cvavk:APA91bELJxqwc8h8FhHkZmiua-0TzLSfYGXBDFu0eBA_u2f_jLptfq_7881kd1F10TkX7ksGMl2gvU1FpCAtBrQvDUwpcIx90IPj9VSVpil7F_NhgO7twwWctevngUrULA8tKo2wTIho"}'
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": 2165529378315486700,
        "label": "Branch Label",
        "code": "147657930",
        "vendorId": 2165529378315486700,
        "token": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJKb2UifQ.1KP0SsvENi7Uz1oQc07aXTL7kpQG5jBNIybqr60AlD4",
        "onlineOrderingFlag": false
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


