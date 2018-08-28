swagger: "2.0"
x-collection-name: moltin
x-complete: 1
info:
  title: Moltin
  description: -welcomethis-is-a-place-to-put-general-notes-and-extra-information-for-internal-use-to-get-started-designingdocumenting-this-api-select-a-version-on-the-left-
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