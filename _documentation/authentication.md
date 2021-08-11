---
title: Authentication
name: Authentication
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. The Planman API uses access tokens to authenticate requests. To get an access token, you can sign in using your branch code through our sign in endpoint.

  The access token should be added as a request header as follows:

    Authorization: Bearer $ACCESS_TOKEN

  None of the requests will succeed unless you include a correct access token in the request header.
  {: .error}
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
       $.get("http://api.myapp.com/books/", { "token": "YOUR_APP_KEY"}, function(data) {
         alert(data);
       });
    title: JQuery
    language: javascript
  - code_block: |2-
       curl http://api.myapp.com/books?token=YOUR_APP_KEY
    title: Curl
    language: bash
---