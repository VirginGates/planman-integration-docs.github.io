---
title: Errors
name: Errors
position_number: 5
parameters:
  - name:
    content:
content_markdown: |- 
  | Code | Name | Description |
  | --- | --- | --- |
  | 200 | OK | Success |
  | 400 | Bad Request | The server could not process the request |
  | 401 | Unauthorized | The request did not include an access token or the access token was expired |
  | 404 | Not Found | The server could not find the requested resource |
  | 500 | Internal Server Error | The server encountered an unexpected condition |

  All errors will return JSON in the following format:
left_code_blocks:
  - code_block: |-
      {
        "stackTraceId": 2165529378315486700,
        "args": {
          "additionalProp1": {},
          "additionalProp2": {},
          "additionalProp3": {},
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
        "code": "$EXCEPTION_CODE"
      }
    title: Response
    language: json
right_code_blocks:
  - code_block:
    title:
    language:
---