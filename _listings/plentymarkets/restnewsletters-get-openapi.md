---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets List newsletter entries
  description: List newsletter entries.
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