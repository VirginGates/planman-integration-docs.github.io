---
title: Main Flow
name: Main Flow
position_number: 4
parameters:
  - name:
    content:
content_markdown: |-
  Planman's main delivery unit is a Trip. For every requested delivery, a new trip entity is created. 

  After you sign in using your branch code, you can list the served zones to identify which geographical zones are served by your branch. This can be done using the __List Served Zones__ endpoint. To initiate a delivery, simply call the __Request Pilot__ endpoint, which will create a new trip entity and request a pilot for delivery.
 
  You can view the trip's information by calling the __Retrieve Trip__ endpoint. Similarly, you can view multiple trips' information through the __List Trips__ endpoint.
  
  Moreover, you can cancel the trip any time before the pilot starts collecting your order by calling the __Cancel Trip__ endpoint.
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