---
title: Main Flow
name: Main Flow
position_number: 4
content_markdown: |-
  Planman's main delivery unit is a Trip. For every requested delivery, a new trip entity is created. Each trip can have multiple tasks, where each task represents an order from the branch by a different customer.

  After you sign in using your branch code, you can list the served zones to identify which geographical zones are served by your branch. This can be done using the __List Served Zones__ endpoint. To initiate a delivery, simply call the __Request Pilot__ endpoint, which will create a new trip entity and request a pilot for delivery. Each branch can have a maximum of two concurrent trips.
 
  You can view the trip's information by calling the __Retrieve Trip__ endpoint. Similarly, you can view multiple trips' information through the __List Trips__ endpoint.
  
  Moreover, you can cancel the trip any time before the pilot starts collecting your order by calling the __Cancel Trip__ endpoint. If you need to cancel a trip after that time, please contact our call center.
  
  Planman supports multiple service types. Integrations use the service type "B2B".

  __Trip status flow__:

  A trip's status is __REQUESTED__ when it's first created. When a pilot is nominated for a trip and still hasn't accepted, the trip's status becomes __PENDING__. When it gets assigned to the pilot, the status is __ASSIGNED__. When the pilot starts collecting the tasks, the trip's status becomes __OPENED__. The trip remains __OPENED__ until all the tasks are delivered, when it then turns __CLOSED__. If at any time the trip is cancelled, its status becomes __CANCELLED__.

  __Task status flow__:

  A task's status is __REQUESTED__ when it's first created. When a pilot is nominated for a trip and still hasn't accepted, the status of the tasks in the trip is __PENDING__. When the trip gets assigned to the pilot, the task's status is __ASSIGNED__. When the pilot reaches the branch, the task's status becomes __PENDING_COLLECTION__. When the pilot collects the task, its status is updated to __COLLECTED__. While the pilot is on the way to the customer's location, the task's status is __ON_DELIVERY__. When the pilot reaches the customer's location, the task's status is __REACHED__. When the pilot delivers the order to the customer, the task's status becomes __DELIVERED__. If at any time the task is cancelled or returned, the status becomes __CANCELED__ or __RETURNED__, respectively.
 
  __Pilot status flow__:

  A pilot's status is __IN_HUB__ when the pilot is in the delivery hub waiting for requests. When the pilot is nominated for a trip, the pilot's status is __CANDIDATE__. When the pilot accepts the trip request, his status becomes __ASSIGNED__. When the pilot reaches the branch, the status is __WAITING__. When the pilot starts collecting the tasks, his status becomes __COLLECTING__. After the pilot collects all the tasks in the trip, the status is updated to __LOADED__. When the pilot delivers all the tasks and he still hasn't arrived to the hub, his status becomes __AVAILABLE__. If a pilot is manually assigned to a trip by one of our affiliated operators, his status becomes __MANUALLY_ASSIGNED__. If one pilot picks up the tasks from another pilot, the status of the former pilot is __REACHED_PILOT__. If a pilot is offline, his status is __UNAVAILABLE__.

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