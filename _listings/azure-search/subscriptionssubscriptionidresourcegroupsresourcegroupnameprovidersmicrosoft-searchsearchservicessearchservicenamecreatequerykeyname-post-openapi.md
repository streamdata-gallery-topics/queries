---
swagger: "2.0"
x-collection-name: Azure Search
x-complete: 0
info:
  title: Azure Search API Query Keys Create
  description: Generates a new query key for the specified Search service. You can
    create up to 50 query keys per service.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Search/searchServices/{searchServiceName}/createQueryKey/{name}
  : post:
      summary: Query Keys Create
      description: Generates a new query key for the specified Search service. You
        can create up to 50 query keys per service.
      operationId: QueryKeys_Create
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-searchsearchservicessearchservicenamecreatequerykeyname-post
      parameters:
      - in: path
        name: name
        description: The name of the new query API key
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Query Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Search/searchServices/{searchServiceName}/listQueryKeys
  : get:
      summary: Query Keys List By Search Service
      description: Returns the list of query API keys for the given Azure Search service.
      operationId: QueryKeys_ListBySearchService
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-searchsearchservicessearchservicenamelistquerykeys-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Query Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Search/searchServices/{searchServiceName}/deleteQueryKey/{key}
  : delete:
      summary: Query Keys Delete
      description: Deletes the specified query key. Unlike admin keys, query keys
        are not regenerated. The process for regenerating a query key is to delete
        and then recreate it.
      operationId: QueryKeys_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-searchsearchservicessearchservicenamedeletequerykeykey-delete
      parameters:
      - in: path
        name: key
        description: The query key to be deleted
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Query Keys
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