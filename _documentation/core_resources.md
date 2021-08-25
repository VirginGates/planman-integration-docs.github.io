---
title: Core Resources
name: Core Resources
position_number: 6
parameters:
  - name:
    content:
content_markdown: |-
  
  __Branch__

  | Name | Type | Description |
  | --- | --- | --- | 
  | id | Long | The unique identifier of the branch. |
  | label | String |  The label (name) of the branch. |
  | vendorId | Long |  The unique identifier of the vendor. |

  __Customer__

  | Name | Type | Description |
  | --- | --- | --- | 
  | id | Long | The unique identifier of the customer. |
  | addressId | Long | The unique identifier of the customer's address. |
  | mobileNo | String | The customer's mobile number. |

  __Location__

  | Name | Type | Description |
  | --- | --- | --- |
  | type | String | A string indicating whether this location is a "Point" or a "Polygon" |
  | coordinates | Array | An array containing the longitude and the latitude coordinates of a location of type "Point", or containing multiple arrays of longitude and latitude coordinates of a location of type "Polygon". |

  __Trip__
  
  | Name | Type | Description |
  | --- | --- | --- | 
  | id | Long | The unique identifier of the trip. |
  | status | TripStatus Enum  | The updated status of the trip. |
  | assignmentDate | String | The date the pilot was assigned to the trip. |
  | creationDate | String | The date the trip was created. |
  | pendingCollectionDate | String | The date the tasks of the trip were ready for collection. |
  | lastUpdateDate | String | The date of the last trip update. |
  | routeDataEnriched | Boolean | ........................ |
  | eta | Integer | The estimated time of arrival of the trip. |
  | slaTier | String | ........................ |
  | maxAllowedTasksCount | Integer | The maximum allowed number of tasks per trip. |
  | requestedTasksCount | Integer | he number of tasks in the trip. |
  | distanceInMeters | Integer | ........................ |
  | durationInSeconds | Integer | ........................ |

  | TripStatus | 
  | --- | 
  | PENDING |
  | REQUESTED |
  | OPENED |
  | CLOSED |
  | ASSIGNED |
  | CANCELLED |
  | NONE |

  __Task__

  | Name | Type | Description |
  | --- | --- | --- | 
  | id | Long | The unique identifier of the task. |
  | sequence | Integer | ........................ |
  | distanceInMeters | Integer | ........................ |
  | distanceFromLastTaskInMeters | Integer | ........................ |
  | durationInSeconds | Integer | ........................ |
  | durationSinceLastTask | Integer | ........................ |
  | pinnedDestinationPoint | Location | ........................ |
  | reachedDestinationDate | String | ........................ |
  | status | TaskStatus | The current status of the task. |
  | linkStatus | String | ........................ |
  | customer | Customer | .............. |

  | TaskStatus | 
  | --- | 
  | PENDING |
  | REQUESTED |
  | ASSIGNED |
  | PENDING_COLLECTION |
  | COLLECTED |
  | REACHED |
  | DELIVERED |
  | RETURNED |
  | CANCELED |
  | RECALLED |
  | ON_DELIVERY |
  | UNKNOWN |
  | NONE |

  __Pilot__

  | Name | Type | Description |
  | --- | --- | --- | 
  | id | Long | The unique identifier of the pilot. | 
  | mobileNo | String | The pilot's mobile number. |
  | fullName | String | The pilot's full name. | 
  | lastKnownLocation | Location | The last location that was recorded for this pilot. |
  | status | PilotStatus |  The current status of the pilot.  |

  | PilotStatus |
  | --- |
  | CANDIDATE |
  | UNAVAILABLE |
  | AVAILABLE |
  | LOADED |
  | IN_HUB |
  | ASSIGNED |
  | WAITING |
  | COLLECTING |
  | MANUALLY_ASSIGNED |
  | REACHED_PILOT |
  | NONE |

  __MultilingualString__

  | Name | Type | Description |
  | --- | --- | --- | 
  | en | String | Name in english. | 
  | ar | String | Name in arabic. |

  __MoneyWithCurrency__

  | Name | Type | Description |
  | --- | --- | --- | 
  | amount | Double | ........................ | 
  | currency | String | ........................ |



#
left_code_blocks:
- code_block:
  title:
  language:
  right_code_blocks:
- code_block:
  title:
  language:
---