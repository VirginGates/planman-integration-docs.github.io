---
title: /api/v1/branches/{id}/sign-out
name: Sign Out
position_number: 1.1
type: post
description: Sign Out
parameters:
  - name: id
    content: Integer
content_markdown: |-
  The branch user will be successfully signed out
  {: .success}

  Sign out as a branch user.
left_code_blocks:
  - code_block: |-
      $.post("http://api.myapp.com/books/", {
        "token": "YOUR_APP_KEY",
        "title": "The Book Thief",
        "score": 4.3
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
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
        "code": "InactiveVendorBranchException"
     }
    title: Error
    language: json
---


