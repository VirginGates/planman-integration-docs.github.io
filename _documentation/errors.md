---
title: Errors
name: Errors
position_number: 5
parameters:
  - name:
    content:
content_markdown: |- 
  __HTTP response codes__

  | Code | Name | Description |
  | --- | --- | --- |
  | 200 | OK | Success |
  | 400 | Bad Request | The server could not process the request |
  | 401 | Unauthorized | The request did not include an access token or the access token was expired |
  | 404 | Not Found | The server could not find the requested resource |
  | 409 | Conflict | The request could not be processed due to a conflict in the current state of the resource |
  | 500 | Internal Server Error | The server encountered an unexpected condition |


  __Response Fields__

  | Name | Type | Description |
  | --- | --- | --- |
  | stackTraceId | Long | ........................ |
  | args | Object | ........................ |
  | devDetails | String |  ........................  |
  | propagated | Boolean | ........................ |
  | trace | Object | ........................ |
  | code | String |  ........................  |

  __Exception Codes__

  | Name | Description |
  | --- | --- |
  | MissingParameterException | A required request parameter is missing. |
  | NotFoundException | ........................ |
  | UnAuthorizedException | ........................ |
  | InactiveVendorBranchException | Branch is not active. |
  | BranchExceedsTripsThresholdException | ........................ |
  | VendorTierConfigDoesNotExist | ........................ |
  | WebClientOperationException | ........................ |
  | InsufficientBalanceException | ........................ |
  | InvalidParameterException | ........................ |
  | InvalidTripStatusException | ........................ |
  | InvalidPilotStatusException | ........................ |
  | InvalidServiceTypesException | ........................ |

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
        "devDetails": "",
        "propagated": false,
        "trace": {
          "exceptionClass": "",
          "message": "",
          "stackTrace": [
            ""
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