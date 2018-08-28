swagger: "2.0"
x-collection-name: Square
x-complete: 1
info:
  title: Square Connect
  description: client-library-for-accessing-the-square-connect-apis
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{location_id}/settlements/{settlement_id}:
    get:
      summary: Provides comprehensive information for a single settlement, including
        the entries that contribute to the settlement's total.
      description: Provides comprehensive information for a single settlement, including
        the entries that contribute to the settlement's total.
      operationId: RetrieveSettlement
      x-api-path-slug: v1location-idsettlementssettlement-id-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the settlementss associated location
      - in: path
        name: settlement_id
        description: The settlements Square-issued ID
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Comprehensive
      - Informationa
      - Single
      - Settlement
      - ""
      - Including
      - Entries
      - That
      - Contribute
      - To
      - Settlements
      - Total