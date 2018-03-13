---
swagger: "2.0"
info:
  title: Reddit
  description: The Reddit API allows you to access the user submitted and rated stories
    on reddit.com. It also provides advanced functionality, including user account
    information and sub-reddit moderation.
  version: 1.0.0
host: www.reddit.com
basePath: api/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '{/r/subreddit}/wiki/alloweditor/act':
    post:
      summary: Add Subreddit Wiki Alloweditor Act
      description: Allow/deny username to edit this wiki page
      operationId: post&nbsp;RSubredditWikiAlloweditorAct
      parameters:
      - in: query
        name: act
        description: one of (del, add)
        type: string
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      - in: query
        name: username
        description: the name of an existing user
        type: string
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - wikioweditor
      - act
definitions: []
x-collection-name: Reddit
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