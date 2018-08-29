---
swagger: "2.0"
x-collection-name: Wikipedia
x-complete: 0
info:
  title: |-
    Wikipedia Get the sum of absolute value of text bytes difference between current edit and
    previous one.
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of absolute bytes
    difference sums. You can filter by editors-type (all-editor-types, anonymous, group-bot,
    name-bot, user) and page-type (all-page-types, content, non-content). You can choose
    between daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  termsOfService: https://wikimediafoundation.org/wiki/Terms_of_Use
  contact:
    name: the Wikimedia Services team
    url: http://mediawiki.org/wiki/REST_API
  version: v1
host: wikimedia.org
basePath: /api/rest_v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /media/math/check/{type}:
    post:
      summary: Check and normalize a TeX formula.
      description: |-
        Checks the supplied TeX formula for correctness and returns the
        normalised formula representation as well as information about
        identifiers. Available types are tex and inline-tex. The response
        contains the `x-resource-location` header which can be used to retrieve
        the render of the checked formula in one of the supported rendering
        formats. Just append the value of the header to `/media/math/{format}/`
        and perform a GET request against that URL.

        Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
      operationId: checks-the-supplied-tex-formula-for-correctness-and-returns-thenormalised-formula-representation-as-
      x-api-path-slug: mediamathchecktype-post
      parameters:
      - in: formData
        name: q
        description: The formula to check
      - in: path
        name: type
        description: The input type of the given formula; can be tex or inline-tex
      responses:
        200:
          description: OK
      tags:
      - Wiki
  /media/math/formula/{hash}:
    get:
      summary: Get a previously-stored formula
      description: |-
        Returns the previously-stored formula via `/media/math/check/{type}` for
        the given hash.

        Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
      operationId: returns-the-previouslystored-formula-via-mediamathchecktype-forthe-given-hashstability-stablehttpsww
      x-api-path-slug: mediamathformulahash-get
      parameters:
      - in: path
        name: hash
        description: The hash string of the previous POST data
      responses:
        200:
          description: OK
      tags:
      - Wiki
  /media/math/render/{format}/{hash}:
    get:
      summary: Get rendered formula in the given format.
      description: |-
        Given a request hash, renders a TeX formula into its mathematic
        representation in the given format. When a request is issued to the
        `/media/math/check/{format}` POST endpoint, the response contains the
        `x-resource-location` header denoting the hash ID of the POST data. Once
        obtained, this endpoint has to be used to obtain the actual render.

        Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
      operationId: given-a-request-hash-renders-a-tex-formula-into-its-mathematicrepresentation-in-the-given-format-whe
      x-api-path-slug: mediamathrenderformathash-get
      parameters:
      - in: path
        name: format
        description: The output format; can be svg or mml
      - in: path
        name: hash
        description: The hash string of the previous POST data
      responses:
        200:
          description: OK
      tags:
      - Wiki
  /metrics/bytes-difference/absolute/aggregate/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}:
    get:
      summary: |-
        Get the sum of absolute value of text bytes difference between current edit and
        previous one.
      description: |-
        Given a Mediawiki project and a date range, returns a timeseries of absolute bytes
        difference sums. You can filter by editors-type (all-editor-types, anonymous, group-bot,
        name-bot, user) and page-type (all-page-types, content, non-content). You can choose
        between daily and monthly granularity as well.

        - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
        - Rate limit: 100 req/s
        - License: Data accessible via this endpoint is available under the
          [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
      operationId: given-a-mediawiki-project-and-a-date-range-returns-a-timeseries-of-absolute-bytesdifference-sums-you
      x-api-path-slug: metricsbytesdifferenceabsoluteaggregateprojecteditortypepagetypegranularitystartend-get
      parameters:
      - in: path
        name: editor-type
        description: If you want to filter by editor-type, use one of anonymous, group-bot
          (registeredaccounts belonging to the bot group), name-bot (registered accounts
          not belonging tothe bot group but having bot-like names) or user (registered
          account not in bot groupnor having bot-like name)
      - in: path
        name: end
        description: The date of the last day to include, in YYYYMMDD format
      - in: path
        name: granularity
        description: Time unit for the response data
      - in: path
        name: page-type
        description: If you want to filter by page-type, use one of content (edits
          on pages in contentnamespaces) or non-content (edits on pages in non-content
          namespaces)
      - in: path
        name: project
        description: The name of any Wikimedia project formatted like {language code}
      - in: path
        name: start
        description: The date of the first day to include, in YYYYMMDD format
      responses:
        200:
          description: OK
      tags:
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