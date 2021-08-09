---
title: /api/v1/branches/{id}/served-zones
name: Served Zones
position_number: 1.1
type: get
description: Retrieve a list of served zones for specific branch
parameters:
  - name: id
    content: Integer
content_markdown: |-
  A pilot will be requested for the order.
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
        "code": "InactiveVendorBranchException"
      }
    title: Error
    language: json
---


