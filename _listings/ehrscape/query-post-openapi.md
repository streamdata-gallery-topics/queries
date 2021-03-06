---
swagger: "2.0"
x-collection-name: EhrScape
x-complete: 0
info:
  title: Ehr Scape Electronic Health Record APIs Querying with named parameter support.
  description: Querying with named parameter support..
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: rest.ehrscape.com
basePath: /rest/v1
paths:
  /demographics/party/query:
    get:
      summary: Queries the demographics store for matching parties, with the query
        parameters specified in the URL.
      description: Queries the demographics store for matching parties, with the query
        parameters specified in the url..
      operationId: queryParties
      x-api-path-slug: demographicspartyquery-get
      parameters:
      - in: query
        name: maxHits
        description: Limit the query results to this many hits
      - in: query
        name: parameters
        description: Query parameters in the key1=value1&key2=value2 format
      responses:
        200:
          description: OK
      tags:
      - Demographics
      - Party
      - Query
    post:
      summary: Queries the demographics store for matching parties.
      description: Queries the demographics store for matching parties..
      operationId: queryParties
      x-api-path-slug: demographicspartyquery-post
      parameters:
      - in: body
        name: body
        description: An array of key-value query criteria
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: maxHits
        description: Limit the query results to this many hits
      responses:
        200:
          description: OK
      tags:
      - Demographics
      - Party
      - Query
  /query:
    get:
      summary: Returns the results of the specified AQL query.
      description: Returns the results of the specified aql query..
      operationId: query
      x-api-path-slug: query-get
      parameters:
      - in: query
        name: aql
        description: The AQL query to execute
      responses:
        200:
          description: OK
      tags:
      - Query
    post:
      summary: Querying with named parameter support.
      description: Querying with named parameter support..
      operationId: query
      x-api-path-slug: query-post
      parameters:
      - in: body
        name: body
        description: A JSON object representing the AQL query and its parameters (see
          model)
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Query
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