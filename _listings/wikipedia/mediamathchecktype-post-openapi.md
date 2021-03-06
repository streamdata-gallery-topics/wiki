---
swagger: "2.0"
x-collection-name: Wikipedia
x-complete: 0
info:
  title: Wikipedia Check and normalize a TeX formula.
  description: |-
    Checks the supplied TeX formula for correctness and returns the
    normalised formula representation as well as information about
    identifiers. Available types are tex and inline-tex. The response
    contains the `x-resource-location` header which can be used to retrieve
    the render of the checked formula in one of the supported rendering
    formats. Just append the value of the header to `/media/math/{format}/`
    and perform a GET request against that URL.

    Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
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