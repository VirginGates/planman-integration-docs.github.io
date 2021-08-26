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
  | routeDataEnriched | Boolean | A flag indicating whether the route data was set in the trip. |
  | eta | Integer | The estimated time of arrival of the trip. |
  | slaTier | String | Refers to the service-level agreement between the vendor and the fleet operator. |
  | maxAllowedTasksCount | Integer | The maximum allowed number of tasks per trip. |
  | requestedTasksCount | Integer | The number of tasks in the trip. |
  | distanceInMeters | Integer | The total distance of the route taken by the pilot from the branch's location to the last customer's location. |
  | durationInSeconds | Integer | The total duration of the trip in seconds. |

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
  | sequence | Integer | Indicates the order of delivery of this task relative to the other tasks in the same trip. |
  | distanceInMeters | Integer | The total distance of the route taken by the pilot from the branch's location to the customer's location. |
  | distanceFromLastTaskInMeters | Integer | The distance between this task's delivery location and the previous task in the same trip's delivery location. |
  | durationInSeconds | Integer | The total duration between the task's request date and delivery date. |
  | durationSinceLastTask | Integer | The duration since the delivery date of the previous task in the same trip. |
  | pinnedDestinationPoint | Location | The customer's location where this task was/is being delivered. |
  | reachedDestinationDate | String | The date that this task reached the customer location. |
  | status | TaskStatus | The current status of the task. |
  | linkStatus | String | Indicates whether the customer location was entered by the pilot and can be linked to this task or not. |
  | customer | Customer | The customer for whom this task belongs. |

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
  | en | String | String representation in English. | 
  | ar | String | String representation in Arabic. |

  __MoneyWithCurrency__

  | Name | Type | Description |
  | --- | --- | --- | 
  | amount | Double | The exact amount of money. | 
  | currency | String | The currency of the money, for example "EGP". |



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