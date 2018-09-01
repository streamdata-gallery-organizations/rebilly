---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Retrieve a list of bank accounts
  description: Retrieve a list of Bank Accounts
  termsOfService: https://www.rebilly.com/terms/
  contact:
    name: Rebilly API Support
    url: https://www.rebilly.com/contact/
    email: integrations@rebilly.com
  version: "2.1"
host: api.rebilly.com
basePath: /v2.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /3dsecure:
    get:
      summary: Retrieve a list of ThreeDSecure entries
      description: Retrieve a list of ThreeDSecure entries
      operationId: 3dsecure.get
      x-api-path-slug: 3dsecure-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - ThreeDSecure
      - Entries
    post:
      summary: Create a ThreeDSecure entry
      description: Create a ThreeDSecure entry
      operationId: 3dsecure.post
      x-api-path-slug: 3dsecure-post
      parameters:
      - in: body
        name: body
        description: ThreeDSecure resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - ThreeDSecure
      - Entry
  /3dsecure/{id}:
    get:
      summary: Retrieve a ThreeDSecure entry
      description: Retrieve a ThreeDSecure entry with specified identifier string
      operationId: 3dsecure.id.get
      x-api-path-slug: 3dsecureid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - ThreeDSecure
      - Entry
  /attachments:
    get:
      summary: Retrieve a list of Attachments
      description: Retrieve a list of Attachments
      operationId: attachments.get
      x-api-path-slug: attachments-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: sort
        description: The collection items sort field and order (prefix with - for
          descending sort)
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Attachments
    post:
      summary: Create an Attachment
      description: Create an Attachment
      operationId: attachments.post
      x-api-path-slug: attachments-post
      parameters:
      - in: body
        name: body
        description: Attachment resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /attachments/{id}:
    delete:
      summary: Delete an Attachment
      description: Delete the Attachment with predefined identifier string
      operationId: attachments.id.delete
      x-api-path-slug: attachmentsid-delete
      responses:
        200:
          description: OK
      tags:
      - Attachment
    get:
      summary: Retrieve an Attachment
      description: Retrieve a Attachment with specified identifier string
      operationId: attachments.id.get
      x-api-path-slug: attachmentsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Attachment
    put:
      summary: Update the Attachment with predefined ID
      description: Update the Attachment with predefined ID
      operationId: attachments.id.put
      x-api-path-slug: attachmentsid-put
      parameters:
      - in: body
        name: body
        description: Attachment resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Attachment
      - Predefined
      - ID
  /authentication-options:
    get:
      summary: Read current authentication options
      description: Read current authentication options
      operationId: authentication_options.get
      x-api-path-slug: authenticationoptions-get
      responses:
        200:
          description: OK
      tags:
      - Read
      - Current
      - Authentication
      - Options
    put:
      summary: Change authentication options
      description: Change options
      operationId: authentication_options.put
      x-api-path-slug: authenticationoptions-put
      parameters:
      - in: body
        name: body
        description: Authentication Options resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Change
      - Authentication
      - Options
  /authentication-tokens:
    get:
      summary: Retrieve a list of auth tokens
      description: Retrieve a list of auth tokens
      operationId: authentication_tokens.get
      x-api-path-slug: authenticationtokens-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Auth
      - Tokens
    post:
      summary: Login
      description: Login a user (customer)
      operationId: authentication_tokens.post
      x-api-path-slug: authenticationtokens-post
      parameters:
      - in: body
        name: body
        description: AuthenticationToken resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Login
  /authentication-tokens/{token}:
    delete:
      summary: Logout a user
      description: Logout a user
      operationId: authentication_tokens.token.delete
      x-api-path-slug: authenticationtokenstoken-delete
      responses:
        200:
          description: OK
      tags:
      - Logout
      - User
    get:
      summary: Verify
      description: Verify an authentication token
      operationId: authentication_tokens.token.get
      x-api-path-slug: authenticationtokenstoken-get
      responses:
        200:
          description: OK
      tags:
      - Verify
  /bank-accounts:
    get:
      summary: Retrieve a list of bank accounts
      description: Retrieve a list of Bank Accounts
      operationId: bank_accounts.get
      x-api-path-slug: bankaccounts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Bank
      - Accounts
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---