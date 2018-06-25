---
name: Reddit
x-slug: reddit
description: Reddit is a community of millions of users engaging in the creation of
  content and the sharing of conversation across tens of thousands of topics.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
x-kinRank: "9"
x-alexaRank: "6"
tags: Wiki
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/apis.md
specificationVersion: "0.14"
apis:
- name: Reddit Add Subreddit Wiki Alloweditor Act
  x-api-slug: reddit
  description: Allow/deny username to edit this wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/alloweditor/act
  tags: Subreddit, Wikioweditor, Act
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikialloweditoract-postnbsp-openapi.md
- name: Reddit Subreddit Wiki Edit
  x-api-slug: reddit
  description: Edit a wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/edit
  tags: Subreddit, Wiki, Edit
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikiedit-postnbsp-openapi.md
- name: Reddit Add Subreddit Wiki
  x-api-slug: reddit
  description: Toggle the public visibility of a wiki page revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/hide
  tags: Subreddit, Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikihide-postnbsp-openapi.md
- name: Reddit Add Subreddit Wiki Revert
  x-api-slug: reddit
  description: Revert a wiki page to revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/revert
  tags: Subreddit, Wiki, Revert
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikirevert-postnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Discussions Page
  x-api-slug: reddit
  description: Retrieve a list of discussions about this wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/discussions/page
  tags: Subreddit, Wiki, Discussions, Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikidiscussionspage-getnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Pages
  x-api-slug: reddit
  description: Retrieve a list of wiki pages in this subreddit
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/pages
  tags: Subreddit, Wiki, Pages
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikipages-getnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Revisions
  x-api-slug: reddit
  description: Retrieve a list of recently changed wiki pages in this subreddit
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/revisions
  tags: Subreddit, Wiki, Revisions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikirevisions-getnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Revisions Page
  x-api-slug: reddit
  description: Retrieve a list of revisions of this wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/revisions/page
  tags: Subreddit, Wiki, Revisions, Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikirevisionspage-getnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Settings Page
  x-api-slug: reddit
  description: Retrieve the current permission settings for page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/settings/page
  tags: Subreddit, Wiki, Settings, Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikisettingspage-getnbsp-openapi.md
- name: Reddit Add Subreddit Wiki Settings Page
  x-api-slug: reddit
  description: Update the permissions and visibility of wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/settings/page
  tags: Subreddit, Wiki, Settings, Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikisettingspage-postnbsp-openapi.md
- name: Reddit Get Subreddit Wiki Page
  x-api-slug: reddit
  description: Return the content of a wiki page
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com///{/r/subreddit}/wiki/page
  tags: Subreddit, Wiki, Page
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/rsubredditwikipage-getnbsp-openapi.md
- name: Reddit
  x-api-slug: reddit
  description: Reddit is a community of millions of users engaging in the creation
    of content and the sharing of conversation across tens of thousands of topics.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/3516-reddit.jpg
  humanURL: http://www.reddit.com
  baseURL: https://www.reddit.com//
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/reddit/openapi.md
x-common:
- type: x-authentication
  url: https://github.com/reddit/reddit/wiki/OAuth2
- type: x-base
  url: https://www.reddit.com/
- type: x-best-practices
  url: https://github.com/reddit/reddit/wiki/API
- type: x-blog
  url: http://www.redditblog.com/
- type: x-blog-rss
  url: https://www.reddit.com/r/datasets/.rss
- type: x-blog-rss
  url: http://www.redditblog.com/feeds/posts/default?alt=rss
- type: x-code-libraries
  url: https://github.com/reddit/reddit/wiki/API-Wrappers
- type: x-console
  url: https://apigee.com/console/reddit
- type: x-crunchbase
  url: https://crunchbase.com/organization/reddit
- type: x-developer
  url: http://www.reddit.com/dev/api
- type: x-email
  url: legal@reddit.com
- type: x-github
  url: https://github.com/reddit
- type: x-linkedin
  url: https://www.linkedin.com/company/product-hunt/
- type: x-privacy
  url: https://www.reddit.com/help/privacypolicy
- type: x-security
  url: https://www.reddit.com/help/privacypolicy#section_security
- type: x-support
  url: https://www.reddit.com/contact/
- type: x-terms-of-service
  url: http://www.reddit.com/help/useragreement
- type: x-transparency-report
  url: https://www.reddit.com/wiki/transparency
- type: x-twitter
  url: https://twitter.com/reddit
- type: x-website
  url: http://www.reddit.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---