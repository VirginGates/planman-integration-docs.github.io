---
title: /api/v1/branches/sign-in
name: Sign In
position_number: 1.0
type: post
description: Sign In
parameters:
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
        "code": "InactiveVendorBranchException"
      }
    title: Error
    language: json
---


