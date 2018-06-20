---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework Retrieve the Content of a Wiki
  description: |-
    Retrieves the plaintext content of a wiki in markdown format.
    ####Returns
    Returns `text/markdown` of the wiki content itself.
    If the request is unsuccessful, plaintext with the error message will be displayed.
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
  /nodes/{node_id}/wikis/:
    get:
      summary: List all wikis
      description: |-
        List of wiki pages on a node.
        ####Returns
        Paginated list of the node's current wiki page versions ordered by their date_modified. Each resource contains the full representation of the wiki, meaning additional requests to an individual wiki's detail view are not necessary.

        Note that if an anonymous view_only key is being used, the user relationship will not be exposed.

        If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
        #### Filtering
        Wiki pages can be filtered based on their `name` and `date_modified` fields.
        + `filter[name]=<Str>` -- filter wiki pages by name
        + `filter[date_modified][comparison_operator]=YYYY-MM-DDTH:M:S` -- filter wiki pages based on date modified.

        Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
      operationId: nodes_wikis_list
      x-api-path-slug: nodesnode-idwikis-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Wikis
  /registrations/{registration_id}/wikis/:
    get:
      summary: List all wikis
      description: |-
        A paginated list of the registration's wiki pages
        ####Returns
        A list of all registration's current wiki page versions ordered by their date_modified. Each resource contains the full representation of the wiki, meaning additional requests to an individual wiki's detail view are not necessary.

        If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
        #### Filtering
        Wiki pages can be filtered based on their `name` and `date_modified` fields.
        + `filter[name]=<Str>` -- filter wiki pages by name
        + `filter[date_modified][comparison_operator]=YYYY-MM-DDTH:M:S` -- filter wiki pages based on date modified.

        Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
      operationId: registrations_wikis_list
      x-api-path-slug: registrationsregistration-idwikis-get
      parameters:
      - in: path
        name: registration_id
        description: The unique identifier of the registration
      responses:
        200:
          description: OK
      tags:
      - Registrations
      - Registration
      - Wikis
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
  /wikis/{wiki_id}/content/:
    get:
      summary: Retrieve the Content of a Wiki
      description: |-
        Retrieves the plaintext content of a wiki in markdown format.
        ####Returns
        Returns `text/markdown` of the wiki content itself.
        If the request is unsuccessful, plaintext with the error message will be displayed.
      operationId: wiki_content
      x-api-path-slug: wikiswiki-idcontent-get
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
      - Content
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