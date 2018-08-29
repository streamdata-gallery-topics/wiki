---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework Retrieve a Wiki
  description: |-
    Retrieves the details about a specific wiki.
    A wiki is a collection of markdown text pages that can be used to describe the project or dataset of contained in the attached node.
    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested wiki, if the request was successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /wikis/{wiki_id}/:
    get:
      summary: Retrieve a Wiki
      description: |-
        Retrieves the details about a specific wiki.
        A wiki is a collection of markdown text pages that can be used to describe the project or dataset of contained in the attached node.
        ####Returns
        Returns a JSON object with a `data` key containing the representation of the requested wiki, if the request was successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: wiki_read
      x-api-path-slug: wikiswiki-id-get
      parameters:
      - in: path
        name: wiki_id
        description: The unique identifier of the wiki
      responses:
        200:
          description: OK
      tags:
      - Wikis
      - Wiki
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