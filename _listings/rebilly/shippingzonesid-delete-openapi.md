---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Delete a shipping zone
  description: Delete a shipping zone with predefined identifier string
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
    put:
      summary: Create or update a Dispute with predefined ID
      description: Create or update a Dispute with predefined identifier string
      operationId: disputes.id.put
      x-api-path-slug: disputesid-put
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
      - Update
      - Dispute
      - Predefined
      - ID
  /disputes/{id}/matched-rules:
    get:
      summary: Get matched rules for the dispute
      description: Get matched rules for the dispute
      operationId: disputes.id.matched_rules.get
      x-api-path-slug: disputesidmatchedrules-get
      responses:
        200:
          description: OK
      tags:
      - Matched
      - Rulesthe
      - Dispute
  /files:
    get:
      summary: Retrieve a list of files
      description: Retrieve a list of files
      operationId: files.get
      x-api-path-slug: files-get
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
      - Files
    post:
      summary: Create a file
      description: Create a file
      operationId: files.post
      x-api-path-slug: files-post
      parameters:
      - in: body
        name: body
        description: Additionally, a file can be sent with a multipart/form-data POST
          request or the files raw body can be sent as a request body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - File
  /files/{id}:
    delete:
      summary: Delete a File
      description: Delete the File with predefined identifier string
      operationId: files.id.delete
      x-api-path-slug: filesid-delete
      responses:
        200:
          description: OK
      tags:
      - File
    get:
      summary: Retrieve a File Record
      description: Retrieve a File with specified identifier string
      operationId: files.id.get
      x-api-path-slug: filesid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - File
      - Record
    put:
      summary: Update the File with predefined ID. Note that file can be uploaded
        with POST only.
      description: Update the File with predefined ID
      operationId: files.id.put
      x-api-path-slug: filesid-put
      parameters:
      - in: body
        name: body
        description: File resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - File
      - Predefined
      - ID
      - ""
      - Note
      - That
      - File
      - Can
      - Be
      - Uploaded
      - POST
      - Only
  /files/{id}/download:
    get:
      summary: Download a file
      description: Download a file
      operationId: files.id.download.get
      x-api-path-slug: filesiddownload-get
      responses:
        200:
          description: OK
      tags:
      - Download
      - File
  /files/{id}/download{extension}:
    get:
      summary: Download image in specific format
      description: Download image in specific format. Images are converted server-side
      operationId: files.id.downloadextension.get
      x-api-path-slug: filesiddownloadextension-get
      responses:
        200:
          description: OK
      tags:
      - Download
      - Image
      - In
      - Specific
      - Format
  /invoices:
    get:
      summary: Retrieve a list of invoices
      description: Retrieve a list of invoices
      operationId: invoices.get
      x-api-path-slug: invoices-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Invoices
    post:
      summary: Create an invoice
      description: Create an invoice
      operationId: invoices.post
      x-api-path-slug: invoices-post
      parameters:
      - in: body
        name: body
        description: Invoice resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /invoices/{id}:
    get:
      summary: Retrieve an invoice
      description: Retrieve an invoice with specified identifier string
      operationId: invoices.id.get
      x-api-path-slug: invoicesid-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoice
    put:
      summary: Create or update an invoice with predefined ID
      description: Create or update an invoice with predefined identifier string
      operationId: invoices.id.put
      x-api-path-slug: invoicesid-put
      parameters:
      - in: body
        name: body
        description: Invoice resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Invoice
      - Predefined
      - ID
  /invoices/{id}/abandon:
    post:
      summary: Abandon an invoice
      description: Abandon an invoice with specified identifier string
      operationId: invoices.id.abandon.post
      x-api-path-slug: invoicesidabandon-post
      responses:
        200:
          description: OK
      tags:
      - Abandon
      - Invoice
  /invoices/{id}/issue:
    post:
      summary: Issue an invoice
      description: Issue an invoice with specified identifier string
      operationId: invoices.id.issue.post
      x-api-path-slug: invoicesidissue-post
      parameters:
      - in: body
        name: body
        description: InvoiceIssue resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Invoice
  /invoices/{id}/items:
    get:
      summary: Retrieve invoice items
      description: Retrieve an invoice items with specified invoice identifier string
      operationId: invoices.id.items.get
      x-api-path-slug: invoicesiditems-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoice
      - Items
    post:
      summary: Create an invoice item
      description: Create an invoice item
      operationId: invoices.id.items.post
      x-api-path-slug: invoicesiditems-post
      parameters:
      - in: body
        name: body
        description: InvoiceItem resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - Item
  /invoices/{id}/lead-source:
    delete:
      summary: Delete a Lead Source for an invoice
      description: Delete a Lead Source that belongs to a certain invoice
      operationId: invoices.id.lead_source.delete
      x-api-path-slug: invoicesidleadsource-delete
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcean
      - Invoice
    get:
      summary: Retrieve an invoice's Lead Source
      description: Retrieve a Lead Source of given invoice
      operationId: invoices.id.lead_source.get
      x-api-path-slug: invoicesidleadsource-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoices
      - Lead
      - Source
    put:
      summary: Create a Lead Source for an invoice
      description: Create a Lead Source for an invoice
      operationId: invoices.id.lead_source.put
      x-api-path-slug: invoicesidleadsource-put
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
      - Sourcean
      - Invoice
  /invoices/{id}/matched-rules:
    get:
      summary: Get matched rules for the invoice
      description: Get matched rules for the invoice
      operationId: invoices.id.matched_rules.get
      x-api-path-slug: invoicesidmatchedrules-get
      responses:
        200:
          description: OK
      tags:
      - Matched
      - Rulesthe
      - Invoice
  /invoices/{id}/void:
    post:
      summary: Void an invoice
      description: Void an invoice with specified identifier string
      operationId: invoices.id.void.post
      x-api-path-slug: invoicesidvoid-post
      responses:
        200:
          description: OK
      tags:
      - Void
      - Invoice
  /password-tokens:
    get:
      summary: Retrieve a list of tokens
      description: Retrieve a list of tokens
      operationId: password_tokens.get
      x-api-path-slug: passwordtokens-get
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
      - Tokens
    post:
      summary: Create a Reset Password Token
      description: Create a Reset Password Token
      operationId: password_tokens.post
      x-api-path-slug: passwordtokens-post
      parameters:
      - in: body
        name: body
        description: ResetPasswordToken resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Password
      - Token
  /password-tokens/{id}:
    delete:
      summary: Delete a Reset Password Token
      description: Delete a Reset Password Token with predefined identifier string
      operationId: password_tokens.id.delete
      x-api-path-slug: passwordtokensid-delete
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Password
      - Token
    get:
      summary: Retrieve a Reset Password Token
      description: Retrieve a Reset Password Token with specified identifier string
      operationId: password_tokens.id.get
      x-api-path-slug: passwordtokensid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Reset
      - Password
      - Token
  /payment-cards:
    get:
      summary: Retrieve a list of Payment Cards
      description: Retrieve a list of Payments Cards
      operationId: payment_cards.get
      x-api-path-slug: paymentcards-get
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
      - Payment
      - Cards
    post:
      summary: Create a Payment Card
      description: Create a Payment Card
      operationId: payment_cards.post
      x-api-path-slug: paymentcards-post
      parameters:
      - in: body
        name: body
        description: PaymentCard resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Payment
      - Card
  /payment-cards/{id}:
    get:
      summary: Retrieve a Payment Card
      description: Retrieve a Payment Card with specified identifier string
      operationId: payment_cards.id.get
      x-api-path-slug: paymentcardsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Payment
      - Card
    patch:
      summary: Update a payment card's cvv value with predefined ID
      description: Update a payment card's cvv value with predefined identifier string
      operationId: payment_cards.id.patch
      x-api-path-slug: paymentcardsid-patch
      parameters:
      - in: body
        name: body
        description: Payment card
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Payment
      - Cards
      - Cvv
      - Value
      - Predefined
      - ID
    put:
      summary: Create a payment card with predefined ID
      description: ""
      operationId: payment_cards.id.put
      x-api-path-slug: paymentcardsid-put
      parameters:
      - in: body
        name: body
        description: Payment card
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Payment
      - Card
      - Predefined
      - ID
  /payment-cards/{id}/authorization:
    post:
      summary: Authorize a Payment Card
      description: Authorize a Payment Card
      operationId: payment_cards.id.authorization.post
      x-api-path-slug: paymentcardsidauthorization-post
      parameters:
      - in: body
        name: body
        description: Payment Card resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Authorize
      - Payment
      - Card
  /payment-cards/{id}/deactivation:
    post:
      summary: Deactivate a Payment Card
      description: Deactivate a Payment Card
      operationId: payment_cards.id.deactivation.post
      x-api-path-slug: paymentcardsiddeactivation-post
      responses:
        200:
          description: OK
      tags:
      - Deactivate
      - Payment
      - Card
  /payment-cards/{id}/matched-rules:
    get:
      summary: Get matched rules for the payment card
      description: Get matched rules for the payment card
      operationId: payment_cards.id.matched_rules.get
      x-api-path-slug: paymentcardsidmatchedrules-get
      responses:
        200:
          description: OK
      tags:
      - Matched
      - Rulesthe
      - Payment
      - Card
  /payments:
    get:
      summary: Retrieve a payment list
      description: Retrieve a payment list
      operationId: payments.get
      x-api-path-slug: payments-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Payment
      - List
    post:
      summary: Create a payment
      description: Create a payment
      operationId: payments.post
      x-api-path-slug: payments-post
      parameters:
      - in: body
        name: body
        description: Payment resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Payment
  /payments/{id}:
    get:
      summary: Retrieve a payment
      description: Retrieve a payment with specified identifier string
      operationId: payments.id.get
      x-api-path-slug: paymentsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Payment
    put:
      summary: Create a payment with predefined ID
      description: Make a payment with predefined identifier string
      operationId: payments.id.put
      x-api-path-slug: paymentsid-put
      parameters:
      - in: body
        name: body
        description: Payment resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Payment
      - Predefined
      - ID
  /paypal-accounts:
    get:
      summary: Retrieve a list of PayPal accounts
      description: Retrieve a list of PayPal Accounts
      operationId: paypal_accounts.get
      x-api-path-slug: paypalaccounts-get
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
      - PayPal
      - Accounts
    post:
      summary: Create a PayPal Account
      description: Create a PayPal Account
      operationId: paypal_accounts.post
      x-api-path-slug: paypalaccounts-post
      parameters:
      - in: body
        name: body
        description: PayPalAccount resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - PayPal
      - Account
  /paypal-accounts/{id}:
    get:
      summary: Retrieve a PayPal Account
      description: Retrieve a PayPal Account with specified identifier string
      operationId: paypal_accounts.id.get
      x-api-path-slug: paypalaccountsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - PayPal
      - Account
    put:
      summary: Create a PayPal account with predefined ID
      description: ""
      operationId: paypal_accounts.id.put
      x-api-path-slug: paypalaccountsid-put
      parameters:
      - in: body
        name: body
        description: PayPal Account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - PayPal
      - Account
      - Predefined
      - ID
  /paypal-accounts/{id}/activation:
    post:
      summary: Activate a PayPal Account
      description: Activate a PayPal Account
      operationId: paypal_accounts.id.activation.post
      x-api-path-slug: paypalaccountsidactivation-post
      parameters:
      - in: body
        name: body
        description: PayPal Account resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Activate
      - PayPal
      - Account
  /paypal-accounts/{id}/deactivation:
    post:
      summary: Deactivate a PayPal Account
      description: Deactivate a PayPal Account
      operationId: paypal_accounts.id.deactivation.post
      x-api-path-slug: paypalaccountsiddeactivation-post
      responses:
        200:
          description: OK
      tags:
      - Deactivate
      - PayPal
      - Account
  /plans:
    get:
      summary: Retrieve a list of plans
      description: Retrieve a list of plans
      operationId: plans.get
      x-api-path-slug: plans-get
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
      - Plans
    post:
      summary: Create a plan
      description: Create a plan
      operationId: plans.post
      x-api-path-slug: plans-post
      parameters:
      - in: body
        name: body
        description: Plan resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Plan
  /plans/{id}:
    delete:
      summary: Delete a Plan
      description: Delete a Plan with predefined identifier string
      operationId: plans.id.delete
      x-api-path-slug: plansid-delete
      responses:
        200:
          description: OK
      tags:
      - Plan
    get:
      summary: Retrieve a plan
      description: Retrieve a plan with specified identifier string
      operationId: plans.id.get
      x-api-path-slug: plansid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Plan
    put:
      summary: Create or update a Plan with predefined ID
      description: Create or update a Plan with predefined identifier string
      operationId: plans.id.put
      x-api-path-slug: plansid-put
      parameters:
      - in: body
        name: body
        description: Plan resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Plan
      - Predefined
      - ID
  /products:
    get:
      summary: Retrieve a list of products
      description: Retrieve a list of products
      operationId: products.get
      x-api-path-slug: products-get
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
      - Products
    post:
      summary: Create a Product
      description: Create a Product
      operationId: products.post
      x-api-path-slug: products-post
      parameters:
      - in: body
        name: body
        description: Product resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Product
  /products/{id}:
    delete:
      summary: Delete a product
      description: Delete a product with predefined identifier string
      operationId: products.id.delete
      x-api-path-slug: productsid-delete
      responses:
        200:
          description: OK
      tags:
      - Product
    get:
      summary: Retrieve a product
      description: Retrieve a product with specified identifier string
      operationId: products.id.get
      x-api-path-slug: productsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Product
    put:
      summary: Create a product with predefined ID
      description: Create a product with predefined identifier string
      operationId: products.id.put
      x-api-path-slug: productsid-put
      parameters:
      - in: body
        name: body
        description: Product resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Product
      - Predefined
      - ID
  /queue/payments:
    get:
      summary: Retrieve a scheduled payment list
      description: Retrieve a scheduled payment list
      operationId: queue.payments.get
      x-api-path-slug: queuepayments-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Scheduled
      - Payment
      - List
  /queue/payments/{id}:
    get:
      summary: Retrieve a scheduled payment
      description: Retrieve a payment with specified identifier string
      operationId: queue.payments.id.get
      x-api-path-slug: queuepaymentsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Scheduled
      - Payment
    put:
      summary: Update pending payment
      description: ""
      operationId: queue.payments.id.put
      x-api-path-slug: queuepaymentsid-put
      parameters:
      - in: body
        name: body
        description: Payment resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Pending
      - Payment
  /shipping-zones:
    get:
      summary: Retrieve a list of shipping zones
      description: Retrieve a list of shipping zones
      operationId: shipping_zones.get
      x-api-path-slug: shippingzones-get
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
      - Shipping
      - Zones
    post:
      summary: Create a Shipping Zone
      description: Create a Shipping Zone
      operationId: shipping_zones.post
      x-api-path-slug: shippingzones-post
      parameters:
      - in: body
        name: body
        description: Shipping Zone resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Shipping
      - Zone
  /shipping-zones/{id}:
    delete:
      summary: Delete a shipping zone
      description: Delete a shipping zone with predefined identifier string
      operationId: shipping_zones.id.delete
      x-api-path-slug: shippingzonesid-delete
      responses:
        200:
          description: OK
      tags:
      - Shipping
      - Zone
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