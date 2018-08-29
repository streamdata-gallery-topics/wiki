---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 1
info:
  title: Stack Exchange
  description: stack-exchange-is-a-network-of-130-qa-communities-including-stack-overflow-
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
---