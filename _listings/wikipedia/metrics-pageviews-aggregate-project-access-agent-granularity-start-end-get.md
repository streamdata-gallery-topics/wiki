---
swagger: "2.0"
info:
  title: Wikipedia Get pageview counts for a project.
  description: |-
    Given a date range, returns a timeseries of pageview counts. You can filter by project,
    access method and/or agent type. You can choose between daily and hourly granularity
    as well.

    - Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable)
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
  /metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end}:
    get:
      summary: Get pageview counts for a project.
      description: Given a date range, returns a timeseries of pageview counts
      operationId: given-a-date-range-returns-a-timeseries-of-pageview-counts-you-can-filter-by-projectaccess-method-an
      parameters:
      - in: path
        name: access
        description: If you want to filter by access method, use one of desktop, mobile-app
          or mobile-web
      - in: path
        name: agent
        description: If you want to filter by agent type, use one of user or spider
      - in: path
        name: end
        description: The timestamp of the last hour/day/month to include, in YYYYMMDDHH
          format
      - in: path
        name: granularity
        description: The time unit for the response data
      - in: path
        name: project
        description: |-
          If you want to filter by project, use the domain of any Wikimedia project,
          for example 'en
      - in: path
        name: start
        description: The timestamp of the first hour/day/month to include, in YYYYMMDDHH
          format
      responses:
        200:
          description: OK
      tags:
      - wiki
definitions:
  "":
    properties:
      type:
        description: This is a default description.
        type: string
      title:
        description: This is a default description.
        type: string
      detail:
        description: This is a default description.
        type: string
      instance:
        description: This is a default description.
        type: string
      items:
        description: This is a default description.
        type: string
      counter:
        description: This is a default description.
        type: string
      ids:
        description: This is a default description.
        type: string
      count:
        description: This is a default description.
        type: string
  absolute-bytes-difference:
    properties:
      items:
        description: This is a default description.
        type: parameters
  by-country:
    properties:
      items:
        description: This is a default description.
        type: parameters
  cx_dict:
    properties:
      source:
        description: This is a default description.
        type: parameters
      translations:
        description: This is a default description.
        type: parameters
  cx_languagepairs:
    properties:
      source:
        description: This is a default description.
        type: parameters
      target:
        description: This is a default description.
        type: parameters
  cx_list_tools:
    properties:
      tools:
        description: This is a default description.
        type: parameters
  cx_mt:
    properties:
      contents:
        description: This is a default description.
        type: parameters
  edited-pages:
    properties:
      items:
        description: This is a default description.
        type: parameters
  editors:
    properties:
      items:
        description: This is a default description.
        type: parameters
  edits:
    properties:
      items:
        description: This is a default description.
        type: parameters
  listing:
    properties:
      items:
        description: This is a default description.
        type: parameters
  net-bytes-difference:
    properties:
      items:
        description: This is a default description.
        type: parameters
  new-pages:
    properties:
      items:
        description: This is a default description.
        type: parameters
  new-registered-users:
    properties:
      items:
        description: This is a default description.
        type: parameters
  originalimage:
    properties:
      height:
        description: This is a default description.
        type: parameters
      source:
        description: This is a default description.
        type: parameters
      width:
        description: This is a default description.
        type: parameters
  pagecounts-project:
    properties:
      items:
        description: This is a default description.
        type: parameters
  pageview-article:
    properties:
      items:
        description: This is a default description.
        type: parameters
  pageview-project:
    properties:
      items:
        description: This is a default description.
        type: parameters
  pageview-tops:
    properties:
      items:
        description: This is a default description.
        type: parameters
  problem:
    properties:
      detail:
        description: This is a default description.
        type: parameters
      instance:
        description: This is a default description.
        type: parameters
      title:
        description: This is a default description.
        type: parameters
      type:
        description: This is a default description.
        type: parameters
  summary:
    properties:
      coordinates:
        description: This is a default description.
        type: parameters
      description:
        description: This is a default description.
        type: parameters
      dir:
        description: This is a default description.
        type: parameters
      displaytitle:
        description: This is a default description.
        type: parameters
      extract:
        description: This is a default description.
        type: parameters
      extract_html:
        description: This is a default description.
        type: parameters
      lang:
        description: This is a default description.
        type: parameters
      pageid:
        description: This is a default description.
        type: parameters
      timestamp:
        description: This is a default description.
        type: parameters
      title:
        description: This is a default description.
        type: parameters
  thumbnail:
    properties:
      height:
        description: This is a default description.
        type: parameters
      source:
        description: This is a default description.
        type: parameters
      width:
        description: This is a default description.
        type: parameters
  top-edited-pages-by-abs-bytes-diff:
    properties:
      items:
        description: This is a default description.
        type: parameters
  top-edited-pages-by-edits:
    properties:
      items:
        description: This is a default description.
        type: parameters
  top-edited-pages-by-net-bytes-diff:
    properties:
      items:
        description: This is a default description.
        type: parameters
  top-editors-by-abs-bytes-diff:
    properties:
      items:
        description: This is a default description.
        type: parameters
  top-editors-by-edits:
    properties:
      items:
        description: This is a default description.
        type: parameters
  top-editors-by-net-bytes-diff:
    properties:
      items:
        description: This is a default description.
        type: parameters
  unique-devices:
    properties:
      items:
        description: This is a default description.
        type: parameters
x-collection-name: Wikipedia
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