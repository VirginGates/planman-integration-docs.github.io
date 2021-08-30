---
title: Authentication
name: Authentication
position_number: 3
content_markdown: |-
  Authentication is required for all API requests. Planman API uses bearer access tokens to authenticate requests. To get an access token, you can sign in using your branch code through our sign in endpoint. The access token's lifetime is 18 hours. Whenever it expires, you need to call the sign in endpoint to have a new one generated.

  The access token should be added as a request header as shown below.

  Apart from the sign in endpoint, none of the requests will succeed unless you include a correct access token in the request header.
  {: .error}

left_code_blocks:
  - code_block: |-
      Authorization: Bearer $ACCESS_TOKEN
    title: 
    language: bash
right_code_blocks:
- code_block: |-
    curl -X POST https://srvstg.virgingates.com/api/v1/branches/sign-in -H "Content-type: application/json" -d '{"code": "1234567"}'
  title: cURL
  language: bash
---