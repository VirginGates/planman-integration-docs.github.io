---
title: /api/v1/trips
name: List Trips
position_number: 1.6
type: get
description: Retrieve a list of trips filtered by criteria and/or sorted by one of trips's properties (e.g creationDate) in asc/desc order
parameters:
  - name: criteria
    content: String
  - name: sortBy
    content: String
  - name: sortType
    content: String
content_markdown: |-
  The trips will be displayed.
  {: .success}

  Sign in as a branch user.
left_code_blocks:
  - code_bl nj ock: |-
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
      [
        {
          "id": 9921381276774878,
          "vendorBranch": {
            "id": 2165529378315486700,
            "label": "McDonald Manial",
            "vendorId": 2165529378315486700
          },
          "pilot": {
            "id": 2165529378315486700,
            "mobileNo": "0102312381",
            "fullName": "Bakaka Dassa",
            "lastKnownLocation": {
              "type": "Point",
              "coordinates": [
                -1.43,
                31.3
              ]
            },
            "status": "UNAVAILABLE"
          },
          "status": "CANCELLED",
          "assignmentDate": "2018-09-01T18:04:53.178Z",
          "pendingCollectionDate": "2018-09-01T18:04:53.178Z",
          "creationDate": "2018-09-01T18:04:53.178Z",
          "eta": 600,
          "slaTier": "LESS_THAN_5_MINUTES",
          "maxAllowedTasksCount": 4,
          "requestedTasksCount": 4
        }
      ]
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


