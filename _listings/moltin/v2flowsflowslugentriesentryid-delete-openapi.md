---
swagger: "2.0"
x-collection-name: moltin
x-complete: 0
info:
  title: Moltin API Delete an entry
  description: Delete an entry.
  version: 1.0.0
host: api.moltin.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/flows/{flowSlug}/entries:
    get:
      summary: Get all entries on a flow
      description: Get all entries on a flow.
      operationId: V2FlowsEntriesByFlowSlugGet
      x-api-path-slug: v2flowsflowslugentries-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entries
      - "On"
      - Flow
    post:
      summary: Create an entry
      description: Create an entry.
      operationId: V2FlowsEntriesByFlowSlugPost
      x-api-path-slug: v2flowsflowslugentries-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
  /v2/flows/{flowSlug}/entries/{entryID}:
    get:
      summary: Get an entry
      description: Get an entry.
      operationId: V2FlowsEntriesByFlowSlugAndEntryIDGet
      x-api-path-slug: v2flowsflowslugentriesentryid-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: entryID
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
    put:
      summary: Update an entry
      description: Update an entry.
      operationId: V2FlowsEntriesByFlowSlugAndEntryIDPut
      x-api-path-slug: v2flowsflowslugentriesentryid-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: entryID
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
    delete:
      summary: Delete an entry
      description: Delete an entry.
      operationId: V2FlowsEntriesByFlowSlugAndEntryIDDelete
      x-api-path-slug: v2flowsflowslugentriesentryid-delete
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: entryID
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
  /v2/flows/{flowSlug}/entries/{ENTRY_ID}/relationships/{flowSlug}:
    put:
      summary: Update Entry Relationship(s)
      description: Update entry relationship(s).
      operationId: V2FlowsEntriesRelationshipsFlowSlugByFlowSlugAndENTRYIDPut
      x-api-path-slug: v2flowsflowslugentriesentry-idrelationshipsflowslug-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: ENTRY_ID
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
      - Relationship(s)
    delete:
      summary: Delete Entry Relationship(s)
      description: Delete entry relationship(s).
      operationId: V2FlowsEntriesRelationshipsFlowSlugByFlowSlugAndENTRYIDDelete
      x-api-path-slug: v2flowsflowslugentriesentry-idrelationshipsflowslug-delete
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: ENTRY_ID
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
      - Relationship(s)
  /v2/flows/{flowSlug}/entries/{entryID}/relationships/{fieldSlug}:
    post:
      summary: Create Entry Relationship(s)
      description: Create entry relationship(s).
      operationId: V2FlowsEntriesRelationshipsFieldSlugByFlowSlugAndEntryIDPost
      x-api-path-slug: v2flowsflowslugentriesentryidrelationshipsfieldslug-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: entryID
      - in: path
        name: fieldSlug
      - in: path
        name: flowSlug
      responses:
        200:
          description: Successful response
      tags:
      - Entry
      - Relationship(s)
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