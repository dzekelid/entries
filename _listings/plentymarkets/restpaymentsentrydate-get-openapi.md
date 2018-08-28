---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets List payments by entry date
  description: Lists all payments by entry date within a certain date range. The start
    and the end of the date range must be specified.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/newsletters:
    delete:
      summary: Delete entries
      description: Delete entries.
      operationId: deleteRestNewsletters
      x-api-path-slug: restnewsletters-delete
      responses:
        200:
          description: OK
      tags:
      - Entries
    get:
      summary: List newsletter entries
      description: List newsletter entries.
      operationId: getRestNewsletters
      x-api-path-slug: restnewsletters-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Newsletter
      - Entries
    post:
      summary: Create an entry
      description: Create an entry.
      operationId: postRestNewsletters
      x-api-path-slug: restnewsletters-post
      parameters:
      - in: body
        name: /rest/newsletters
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: body
        description: The body of the newsletter entry
      - in: query
        name: kind
        description: The type of the entry
      - in: query
        name: subject
        description: The subject of the newsletter entry
      responses:
        200:
          description: OK
      tags:
      - Entry
  /rest/logs:
    post:
      summary: Create a log entry.
      description: Create a log entry..
      operationId: postRestLogs
      x-api-path-slug: restlogs-post
      parameters:
      - in: body
        name: /rest/logs
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Log
      - Entry
  /rest/logs/{id}:
    get:
      summary: Get Log entry by ID.
      description: Get log entry by id..
      operationId: getRestLogs
      x-api-path-slug: restlogsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Log
      - Entry
      - By
      - ID
  /rest/newsletters/{entryId}:
    delete:
      summary: Delete an entry
      description: Deletes an entry. The ID of the entry must be specified.
      operationId: deleteRestNewslettersEntry
      x-api-path-slug: restnewslettersentryid-delete
      parameters:
      - in: path
        name: entryId
      responses:
        200:
          description: OK
      tags:
      - Entry
    get:
      summary: List details of an entry
      description: Lists details of an entry. The ID of the entry must be specified.
      operationId: getRestNewslettersEntry
      x-api-path-slug: restnewslettersentryid-get
      parameters:
      - in: path
        name: entryId
      responses:
        200:
          description: OK
      tags:
      - List
      - Details
      - Of
      - Entry
    put:
      summary: Update an entry
      description: Updates an entry. The ID of the entry must be specified.
      operationId: putRestNewslettersEntry
      x-api-path-slug: restnewslettersentryid-put
      parameters:
      - in: query
        name: body
        description: The body of the entry
      - in: path
        name: entryId
      - in: query
        name: kind
        description: The type of the entry
      - in: query
        name: subject
        description: The subject of the entry
      responses:
        200:
          description: OK
      tags:
      - Entry
  /rest/payments/entrydate:
    get:
      summary: List payments by entry date
      description: Lists all payments by entry date within a certain date range. The
        start and the end of the date range must be specified.
      operationId: getRestPaymentsEntrydate
      x-api-path-slug: restpaymentsentrydate-get
      parameters:
      - in: query
        name: endDate
        description: The end date of the date range for the entry date of the payment
      - in: query
        name: itemsPerPage
        description: The number of items to list per page
      - in: query
        name: page
        description: The page of results to search for
      - in: query
        name: startDate
        description: The start date of the date range for the entry date of the payment
      responses:
        200:
          description: OK
      tags:
      - List
      - Payments
      - By
      - Entry
      - Date
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