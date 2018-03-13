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
  '{/r/subreddit}/wiki/settings/page':
    post:
      summary: Add Subreddit Wiki Settings Page
      description: Update the permissions and visibility of wiki page
      operationId: post&nbsp;RSubredditWikiSettingsPage
      parameters:
      - in: query
        name: listed
        description: boolean value
        type: string
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: permlevel
        description: an integer
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - wiki
      - settings
      - page
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