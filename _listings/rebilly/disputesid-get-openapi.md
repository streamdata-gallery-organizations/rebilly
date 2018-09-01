---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Retrieve a dispute
  description: Retrieve a dispute with specified identifier string
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
    post:
      summary: Create a Bank Account
      description: Create a Bank Account
      operationId: bank_accounts.post
      x-api-path-slug: bankaccounts-post
      parameters:
      - in: body
        name: body
        description: BankAccount resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bank
      - Account
  /bank-accounts/{id}:
    get:
      summary: Retrieve a Bank Account
      description: Retrieve a Bank Account with specified identifier string
      operationId: bank_accounts.id.get
      x-api-path-slug: bankaccountsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Bank
      - Account
    put:
      summary: Create a BankAccount with predefined ID
      description: Create or update a BankAccount with predefined identifier string
      operationId: bank_accounts.id.put
      x-api-path-slug: bankaccountsid-put
      parameters:
      - in: body
        name: body
        description: BankAccount resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - BankAccount
      - Predefined
      - ID
  /bank-accounts/{id}/deactivation:
    post:
      summary: Deactivate a Bank Account
      description: Deactivate a Bank Account
      operationId: bank_accounts.id.deactivation.post
      x-api-path-slug: bankaccountsiddeactivation-post
      responses:
        200:
          description: OK
      tags:
      - Deactivate
      - Bank
      - Account
  /blacklists:
    get:
      summary: Retrieve a list of blacklists
      description: Retrieve a list of blacklists
      operationId: blacklists.get
      x-api-path-slug: blacklists-get
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
      - Blacklists
    post:
      summary: Create a blacklist
      description: Create a blacklist
      operationId: blacklists.post
      x-api-path-slug: blacklists-post
      parameters:
      - in: body
        name: body
        description: Blacklist resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Blacklist
  /blacklists/{id}:
    delete:
      summary: Delete a blacklist
      description: Delete a blacklist with predefined identifier string
      operationId: blacklists.id.delete
      x-api-path-slug: blacklistsid-delete
      responses:
        200:
          description: OK
      tags:
      - Blacklist
    get:
      summary: Retrieve a blacklist
      description: Retrieve a blacklist with specified identifier string
      operationId: blacklists.id.get
      x-api-path-slug: blacklistsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Blacklist
    put:
      summary: Create a blacklist with predefined ID
      description: Create a blacklist with predefined identifier string
      operationId: blacklists.id.put
      x-api-path-slug: blacklistsid-put
      parameters:
      - in: body
        name: body
        description: Blacklist resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Blacklist
      - Predefined
      - ID
  /contacts:
    get:
      summary: Retrieve a list of contacts
      description: Retrieve a list of contacts
      operationId: contacts.get
      x-api-path-slug: contacts-get
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
      - Contacts
    post:
      summary: Create a contact
      description: Create a contact
      operationId: contacts.post
      x-api-path-slug: contacts-post
      parameters:
      - in: body
        name: body
        description: Contact resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Contact
  /contacts/{id}:
    delete:
      summary: Delete a contact
      description: Delete a contact with predefined identifier string
      operationId: contacts.id.delete
      x-api-path-slug: contactsid-delete
      responses:
        200:
          description: OK
      tags:
      - Contact
    get:
      summary: Retrieve a contact
      description: Retrieve a contact with specified identifier string
      operationId: contacts.id.get
      x-api-path-slug: contactsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Contact
    put:
      summary: Create or update a contact with predefined ID
      description: Create or update a contact with predefined identifier string
      operationId: contacts.id.put
      x-api-path-slug: contactsid-put
      parameters:
      - in: body
        name: body
        description: Contact resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Contact
      - Predefined
      - ID
  /coupons:
    get:
      summary: Retrieve a list of coupons
      description: Retrieve a list of coupons
      operationId: coupons.get
      x-api-path-slug: coupons-get
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
      - Coupons
    post:
      summary: Create a coupon
      description: Create a coupon
      operationId: coupons.post
      x-api-path-slug: coupons-post
      parameters:
      - in: body
        name: body
        description: Coupon resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Coupon
  /coupons-redemptions:
    get:
      summary: Retrieve a list of coupon redemptions
      description: ""
      operationId: coupons_redemptions.get
      x-api-path-slug: couponsredemptions-get
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
      - Coupon
      - Redemptions
    post:
      summary: Redeem a coupon
      description: Redeem a coupon
      operationId: coupons_redemptions.post
      x-api-path-slug: couponsredemptions-post
      parameters:
      - in: body
        name: body
        description: Redeem a coupon
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Redeem
      - Coupon
  /coupons-redemptions/{id}:
    get:
      summary: Retrieve a coupon redemption with specified identifier string
      description: ""
      operationId: coupons_redemptions.id.get
      x-api-path-slug: couponsredemptionsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Coupon
      - Redemption
      - Specified
      - Identifier
      - String
  /coupons-redemptions/{id}/cancel:
    post:
      summary: Cancel a coupon redemption
      description: ""
      operationId: coupons_redemptions.id.cancel.post
      x-api-path-slug: couponsredemptionsidcancel-post
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Coupon
      - Redemption
  /coupons/{redemptionCode}:
    get:
      summary: Retrieve a coupon
      description: Retrieve a coupon with specified redemption code string
      operationId: coupons.redemptionCode.get
      x-api-path-slug: couponsredemptioncode-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Coupon
    put:
      summary: Create or update a coupon with predefined redemption code
      description: Create or update a coupon with predefined redemption code
      operationId: coupons.redemptionCode.put
      x-api-path-slug: couponsredemptioncode-put
      parameters:
      - in: body
        name: body
        description: Coupon resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Coupon
      - Predefined
      - Redemption
      - Code
  /coupons/{redemptionCode}/expiration:
    post:
      summary: Set a coupon's expiration time.
      description: |-
        Set a coupon's expiry time with the specified redemption code.
        The expiredTime of a coupon must be greater than its issuedTime.
        This cannot be performed on expired coupons.
      operationId: coupons.redemptionCode.expiration.post
      x-api-path-slug: couponsredemptioncodeexpiration-post
      parameters:
      - in: body
        name: body
        description: Coupon resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Set
      - Coupons
      - Expiration
      - Time
  /credentials:
    get:
      summary: Retrieve a list of credentials
      description: Retrieve a list of credentials
      operationId: credentials.get
      x-api-path-slug: credentials-get
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
      - Credentials
    post:
      summary: Create a credential
      description: Create a credential
      operationId: credentials.post
      x-api-path-slug: credentials-post
      parameters:
      - in: body
        name: body
        description: Credential resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Credential
  /credentials/{id}:
    delete:
      summary: Delete a credential
      description: Delete a credential with predefined identifier string
      operationId: credentials.id.delete
      x-api-path-slug: credentialsid-delete
      responses:
        200:
          description: OK
      tags:
      - Credential
    get:
      summary: Retrieve a credential
      description: Retrieve a credential with specified identifier string
      operationId: credentials.id.get
      x-api-path-slug: credentialsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Credential
    put:
      summary: Create or update a credential with predefined ID
      description: Create or update a credential with predefined identifier string
      operationId: credentials.id.put
      x-api-path-slug: credentialsid-put
      parameters:
      - in: body
        name: body
        description: Credential resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Credential
      - Predefined
      - ID
  /custom-fields/{resource}:
    get:
      summary: Retrieve Custom Fields
      description: Retrieve a schema of Custom Fields for the given resource type
      operationId: custom_fields.resource.get
      x-api-path-slug: customfieldsresource-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Custom
      - Fields
  /custom-fields/{resource}/{name}:
    delete:
      summary: Delete a custom field
      description: Delete a custom field by its name
      operationId: custom_fields.resource.name.delete
      x-api-path-slug: customfieldsresourcename-delete
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Field
    get:
      summary: Retrieve a Custom Field
      description: Retrieve a schema of the given Custom Field for the given resource
        type
      operationId: custom_fields.resource.name.get
      x-api-path-slug: customfieldsresourcename-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Custom
      - Field
    put:
      summary: Create or alter a Custom Field
      description: Create or alter a schema of the given Custom Field for the given
        resource type.
      operationId: custom_fields.resource.name.put
      x-api-path-slug: customfieldsresourcename-put
      parameters:
      - in: body
        name: body
        description: Custom Fields schema of the given resource type
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Alter
      - Custom
      - Field
  /customers:
    get:
      summary: Retrieve a list of customers
      description: Retrieve a list of customers
      operationId: customers.get
      x-api-path-slug: customers-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
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
      - Customers
    post:
      summary: Create a customer
      description: Create a customer
      operationId: customers.post
      x-api-path-slug: customers-post
      parameters:
      - in: body
        name: body
        description: Customer resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
  /customers/{id}:
    get:
      summary: Retrieve a customer
      description: Retrieve a customer with specified identifier string
      operationId: customers.id.get
      x-api-path-slug: customersid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Customer
    put:
      summary: Create a customer with predefined ID
      description: Create a customer with predefined identifier string
      operationId: customers.id.put
      x-api-path-slug: customersid-put
      parameters:
      - in: body
        name: body
        description: Customer resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
      - Predefined
      - ID
  /customers/{id}/lead-source:
    delete:
      summary: Delete a Lead Source for a customer
      description: Delete a Lead Source that belongs to a certain customer
      operationId: customers.id.lead_source.delete
      x-api-path-slug: customersidleadsource-delete
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcea
      - Customer
    get:
      summary: Retrieve a customer's Lead Source
      description: Retrieve a Lead Source of given customer
      operationId: customers.id.lead_source.get
      x-api-path-slug: customersidleadsource-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Customers
      - Lead
      - Source
    put:
      summary: Create a Lead Source for a customer
      description: Create a Lead Source for a customer
      operationId: customers.id.lead_source.put
      x-api-path-slug: customersidleadsource-put
      parameters:
      - in: body
        name: body
        description: Lead Source resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcea
      - Customer
  /disputes:
    get:
      summary: Retrieve a list of disputes
      description: Retrieve a list of disputes
      operationId: disputes.get
      x-api-path-slug: disputes-get
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
      - Disputes
    post:
      summary: Create a dispute
      description: Create a dispute
      operationId: disputes.post
      x-api-path-slug: disputes-post
      parameters:
      - in: body
        name: body
        description: Dispute resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dispute
  /disputes/{id}:
    get:
      summary: Retrieve a dispute
      description: Retrieve a dispute with specified identifier string
      operationId: disputes.id.get
      x-api-path-slug: disputesid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Dispute
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