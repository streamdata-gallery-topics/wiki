---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get Tags Wikis
  description: "Returns the wikis that go with the given set of tags in {tags}.\n
    \nBe aware that not all tags have wikis.\n \n{tags} can contain up to 20 individual
    tags per request.\n \nThis method returns a list of tag wikis."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tags/{tags}/wikis:
    get:
      summary: Get Tags Wikis
      description: "Returns the wikis that go with the given set of tags in {tags}.\n
        \nBe aware that not all tags have wikis.\n \n{tags} can contain up to 20 individual
        tags per request.\n \nThis method returns a list of tag wikis."
      operationId: returns-the-wikis-that-go-with-the-given-set-of-tags-in-tags-be-aware-that-not-all-tags-have-wikis-t
      x-api-path-slug: tagstagswikis-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: path
        name: tags
        description: String list (semicolon delimited)
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Wikis
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