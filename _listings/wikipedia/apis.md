---
name: Wikipedia
description: Wikipedia is a Wikimedia Foundation project to build free encyclopedias
  in all languages of the world. Virtually anyone with Internet access is free to
  contribute, by contributing neutral, cited information. As of March 2008 Wikipedia
  is offered in 250 languages.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/144_logo.png
x-kinRank: "8"
x-alexaRank: ""
tags:
- Wiki
- Stack Network
- Stack
- Media
- Imports
- Content
created: "2018-03-24"
modified: "2018-03-24"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/apis.yaml
specificationVersion: "0.14"
apis:
- name: Wikipedia
  description: Wikipedia is a Wikimedia Foundation project to build free encyclopedias
    in all languages of the world
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/144_logo.png
  humanURL: ""
  baseURL: https://wikimedia.org//api/rest_v1
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transform-word-from-from-lang-to-to-lang-word-provider-get.md
- name: Wikipedia Given a project and a date range, returns a timeseries of pagecounts.
    You can filter by access site (mobile or desktop) and you can choose between monthly,
    daily and hourly granularity as well.
  description: |-
    Given a project and a date range, returns a timeseries of pagecounts.
    You can filter by access site (mobile or desktop) and you can choose between monthly,
    daily and hourly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/144_logo.png
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metrics-legacy-pagecounts-aggregate-project-access-site-granularity-start-end-get.md
x-common:
- type: x-base
  url: http://en.wikipedia.org/w/api.php
- type: x-crunchbase
  url: http://www.crunchbase.com/company/wikipedia
- type: x-developer
  url: http://www.mediawiki.org/wiki/API
- type: x-github
  url: https://github.com/Wikipedia
- type: x-swagger--original
  url: http://rest.wikimedia.org/en.wikipedia.org/v1/?spec
- type: x-transparency-report
  url: https://transparency.wikimedia.org/
- type: x-twitter
  url: https://twitter.com/wikipedia
- type: x-website
  url: https://www.wikipedia.org/
- type: x-base
  url: http://en.wikipedia.org/w/api.php
- type: x-crunchbase
  url: http://www.crunchbase.com/company/wikipedia
- type: x-developer
  url: http://www.mediawiki.org/wiki/API
- type: x-github
  url: https://github.com/Wikipedia
- type: x-swagger--original
  url: http://rest.wikimedia.org/en.wikipedia.org/v1/?spec
- type: x-transparency-report
  url: https://transparency.wikimedia.org/
- type: x-twitter
  url: https://twitter.com/wikipedia
- type: x-website
  url: https://www.wikipedia.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---