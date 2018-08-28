---
swagger: "2.0"
x-collection-name: MasterCard
x-complete: 0
info:
  title: Mastercard Put Entry
  description: |-
    Add a transaction entry for your application to the blockchain. Note that
    this entry must be a valid message according to the application configuration
    that you set up.
  version: 1.0.0
host: eas5stl0.mastercard.int:13046
basePath: /z0/core/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /entry:
    put:
      summary: Put Entry
      description: |-
        Add a transaction entry for your application to the blockchain. Note that
        this entry must be a valid message according to the application configuration
        that you set up.
      operationId: putEntry
      x-api-path-slug: entry-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: MCWSSAML
        description: SAML Authorization
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Entry
  /entry/{key}:
    get:
      summary: Get Entry Key
      description: |-
        Returns full detail of the value of the blockchain entry
        referenced by the specified key, if it has been previously recorded
        by your node's key-value store (database).
      operationId: getEntryKey
      x-api-path-slug: entrykey-get
      parameters:
      - in: path
        name: key
      - in: header
        name: MCWSSAML
        description: SAML Authorization
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Entry
      - Key
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