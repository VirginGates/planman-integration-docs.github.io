---
title: Errors
name: Errors
position_number: 5
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

  __Exception Codes__

  | Name | Description |
  | --- | --- |
  | MissingParameterException | A required request parameter is missing. |
  | NotFoundException | The requested resource is not found. |
  | UnAuthorizedException | The branch code used for sign in is not correct, or the bearer token is not valid. |
  | InactiveVendorBranchException | The branch is not active. |
  | BranchExceedsTripsThresholdException | The maximum number of concurrent trips per branch has been exceeded. |
  | VendorTierConfigDoesNotExist | The vendor has no current pricing configuration. |
  | InsufficientBalanceException | The vendor has insufficient balance to request pilot. |
  | InvalidParameterException | The value of the parameter is not supported. |
  | InvalidTripStatusException | The trip's status is not as expected for this request to be completed. |
  | InvalidPilotStatusException | The pilot's status is not as expected for this request to be completed. |
  | InvalidServiceTypesException | The service type is not as expected for this request to be completed. For example, it could be "B2B" while it's required to be "B2C". |

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