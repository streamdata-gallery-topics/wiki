---
name: Wikipedia
x-slug: wikipedia
description: Wikipedia is a free online encyclopedia, created and edited by volunteers
  around the world and hosted by the Wikimedia Foundation.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
x-kinRank: "8"
x-alexaRank: "5"
tags: Wiki
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/apis.md
specificationVersion: "0.14"
apis:
- name: Wikipedia Check and normalize a TeX formula.
  x-api-slug: wikipedia
  description: |-
    Checks the supplied TeX formula for correctness and returns the
    normalised formula representation as well as information about
    identifiers. Available types are tex and inline-tex. The response
    contains the `x-resource-location` header which can be used to retrieve
    the render of the checked formula in one of the supported rendering
    formats. Just append the value of the header to `/media/math/{format}/`
    and perform a GET request against that URL.

    Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//media/math/check/{type}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/mediamathchecktype-post-openapi.md
- name: Wikipedia Get a previously-stored formula
  x-api-slug: wikipedia
  description: |-
    Returns the previously-stored formula via `/media/math/check/{type}` for
    the given hash.

    Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//media/math/formula/{hash}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/mediamathformulahash-get-openapi.md
- name: Wikipedia Get rendered formula in the given format.
  x-api-slug: wikipedia
  description: |-
    Given a request hash, renders a TeX formula into its mathematic
    representation in the given format. When a request is issued to the
    `/media/math/check/{format}` POST endpoint, the response contains the
    `x-resource-location` header denoting the hash ID of the POST data. Once
    obtained, this endpoint has to be used to obtain the actual render.

    Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//media/math/render/{format}/{hash}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/mediamathrenderformathash-get-openapi.md
- name: |-
    Wikipedia Get the sum of absolute value of text bytes difference between current edit and
    previous one.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of absolute bytes
    difference sums. You can filter by editors-type (all-editor-types, anonymous, group-bot,
    name-bot, user) and page-type (all-page-types, content, non-content). You can choose
    between daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/bytes-difference/absolute/aggregate/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricsbytesdifferenceabsoluteaggregateprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get the sum of net text bytes difference between current edit and
    previous one.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of bytes difference net
    sums. You can filter by editors-type (all-editor-types, anonymous, group-bot, name-bot,
    user) and page-type (all-page-types, content or non-content). You can choose between
    daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/bytes-difference/net/aggregate/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricsbytesdifferencenetaggregateprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get edited-pages counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of its edited-pages counts.
    You can filter by editor-type (all-editor-types, anonymous, group-bot, name-bot, user),
    page-type (all-page-types, content or non-content) or activity-level (1..4-edits,
    5..24-edits, 25..99-edits, 100..-edits). You can choose between daily and monthly
    granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edited-pages/aggregate/{project}/{editor-type}/{page-type}/{activity-level}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditedpagesaggregateprojecteditortypepagetypeactivitylevelgranularitystartend-get-openapi.md
- name: Wikipedia Get new pages counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of its new pages counts.
    You can filter by editor type (all-editor-types, anonymous, group-bot, name-bot, user)
    or page-type (all-page-types, content or non-content). You can choose between daily and
    monthly granularity as well.
    The new pages value is computed as follow:
      [number of created pages] - [number of deleted pages] + [number of restored pages]
    for the chosen filters.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edited-pages/new/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditedpagesnewprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 edited-pages by absolute bytes-difference.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 edited-pages
    by absolute bytes-difference. You can filter by editor-type (all-editor-types, anonymous,
    group-bot, name-bot, user) or page-type (all-page-types, content or non-content). You can
    choose between daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edited-pages/top-by-absolute-bytes-difference/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditedpagestopbyabsolutebytesdifferenceprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 edited-pages by edits count.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 edited-pages
    by edits count. You can filter by editor-type (all-editor-types, anonymous, group-bot,
    name-bot, user) or page-type (all-page-types, content or non-content). You can choose
    between daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edited-pages/top-by-edits/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditedpagestopbyeditsprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 edited-pages by net bytes-difference.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 edited-pages
    by net bytes-difference. You can filter by editor-type (all-editor-types, anonymous,
    group-bot, name-bot, user) or page-type (all-page-types, content or non-content). You can
    choose between daily and monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edited-pages/top-by-net-bytes-difference/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditedpagestopbynetbytesdifferenceprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get editors counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of its editors counts.
    You can filter by editory-type (all-editor-types, anonymous, group-bot, name-bot, user),
    page-type (all-page-types, content or non-content) or activity-level (1..4-edits,
    5..24-edits, 25..99-edits or 100..-edits). You can choose between daily and monthly
    granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/editors/aggregate/{project}/{editor-type}/{page-type}/{activity-level}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditorsaggregateprojecteditortypepagetypeactivitylevelgranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 editors by absolute bytes-difference.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 editors by
    absolute bytes-difference. You can filter by editor-type (all-editor-types, anonymous,
    group-bot, name-bot, user) or page-type (all-page-types, content or non-content). You can
    choose between daily and monthly granularity as well. The user_id returned is either the
    mediawiki user_id if user is registered, or his/her IP if the user is anonymous.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/editors/top-by-absolute-bytes-difference/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditorstopbyabsolutebytesdifferenceprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 editors by edits count.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 editors by
    edits count. You can filter by editor-type (all-editor-types, anonymous, group-bot,
    name-bot, user) or page-type (all-page-types, content or non-content). You can choose
    between daily and monthly granularity as well. The user_id returned is either the
    mediawiki user_id if user is registered, or his/her IP if the user is anonymous.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/editors/top-by-edits/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditorstopbyeditsprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get top 100 editors by net bytes-difference.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of the top 100 editors by
    net bytes-difference. You can filter by editor-type (all-editor-types, anonymous, group-bot,
    name-bot, user) or page-type (all-page-types, content or non-content). You can choose
    between daily and monthly granularity as well. The user_id returned is either the mediawiki
    user_id if user is registered, or his/her IP if the user is anonymous.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/editors/top-by-net-bytes-difference/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditorstopbynetbytesdifferenceprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Get edits counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of edits counts.
    You can filter by editors-type (all-editor-types, anonymous, bot, registered) and
    page-type (all-page-types, content or non-content). You can choose between daily and
    monthly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/edits/aggregate/{project}/{editor-type}/{page-type}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricseditsaggregateprojecteditortypepagetypegranularitystartend-get-openapi.md
- name: Wikipedia Given a project and a date range, returns a timeseries of pagecounts.
    You can filter by access site (mobile or desktop) and you can choose between monthly,
    daily and hourly granularity as well.
  x-api-slug: wikipedia
  description: |-
    Given a project and a date range, returns a timeseries of pagecounts.
    You can filter by access site (mobile or desktop) and you can choose between monthly,
    daily and hourly granularity as well.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/legacy/pagecounts/aggregate/{project}/{access-site}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricslegacypagecountsaggregateprojectaccesssitegranularitystartend-get-openapi.md
- name: Wikipedia Get pageview counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a date range, returns a timeseries of pageview counts. You can filter by project,
    access method and/or agent type. You can choose between daily and hourly granularity
    as well.

    - Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricspageviewsaggregateprojectaccessagentgranularitystartend-get-openapi.md
- name: Wikipedia Get pageview counts for a page.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki article and a date range, returns a daily timeseries of its pageview
    counts. You can also filter by access method and/or agent type.

    - Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/pageviews/per-article/{project}/{access}/{agent}/{article}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricspageviewsperarticleprojectaccessagentarticlegranularitystartend-get-openapi.md
- name: Wikipedia Get pageviews by country and access method.
  x-api-slug: wikipedia
  description: |-
    Lists the pageviews to this project, split by country of origin for a given month.
    Because of privacy reasons, pageviews are given in a bucketed format, and countries
    with less than 100 views do not get reported.
    Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/pageviews/top-by-country/{project}/{access}/{year}/{month}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricspageviewstopbycountryprojectaccessyearmonth-get-openapi.md
- name: Wikipedia Get the most viewed articles for a project.
  x-api-slug: wikipedia
  description: |-
    Lists the 1000 most viewed articles for a given project and timespan (month or day).
    You can filter by access method.

    - Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/pageviews/top/{project}/{access}/{year}/{month}/{day}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricspageviewstopprojectaccessyearmonthday-get-openapi.md
- name: Wikipedia Get newly registered users counts for a project.
  x-api-slug: wikipedia
  description: |-
    Given a Mediawiki project and a date range, returns a timeseries of its newly registered
    users counts. You can choose between daily and monthly granularity. The newly registered
    users value is computed with self-created users only, not auto-login created ones.

    - Stability: [experimental](https://www.mediawiki.org/wiki/API_versioning#Experimental)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/registered-users/new/{project}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricsregisteredusersnewprojectgranularitystartend-get-openapi.md
- name: Wikipedia Get unique devices count per project
  x-api-slug: wikipedia
  description: |-
    Given a project and a date range, returns a timeseries of unique devices counts.
    You need to specify a project, and can filter by accessed site (mobile or desktop).
    You can choose between daily and hourly granularity as well.

    - Stability: [stable](https://www.mediawiki.org/wiki/API_versioning#Stable)
    - Rate limit: 100 req/s
    - License: Data accessible via this endpoint is available under the
      [CC0 1.0 license](https://creativecommons.org/publicdomain/zero/1.0/).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//metrics/unique-devices/{project}/{access-site}/{granularity}/{start}/{end}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/metricsuniquedevicesprojectaccesssitegranularitystartend-get-openapi.md
- name: Wikipedia Machine-translate content
  x-api-slug: wikipedia
  description: |-
    Fetches the machine translation for the posted content from the source
    to the destination language.

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/html/from/{from_lang}/to/{to_lang}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformhtmlfromfrom-langtoto-lang-post-openapi.md
- name: Wikipedia Machine-translate content
  x-api-slug: wikipedia
  description: |-
    Fetches the machine translation for the posted content from the source
    to the destination language.

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/html/from/{from_lang}/to/{to_lang}/{provider}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformhtmlfromfrom-langtoto-langprovider-post-openapi.md
- name: Wikipedia Lists the language pairs supported by the back-end
  x-api-slug: wikipedia
  description: |-
    Fetches the list of language pairs the back-end service can translate

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/list/languagepairs/
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformlistlanguagepairs-get-openapi.md
- name: Wikipedia Lists the tools available for a language pair
  x-api-slug: wikipedia
  description: |-
    Fetches the list of tools that are available for the given pair of languages.

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/list/pair/{from}/{to}/
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformlistpairfromto-get-openapi.md
- name: Wikipedia Lists the tools and language pairs available for the given tool
    category
  x-api-slug: wikipedia
  description: |-
    Fetches the list of tools and all of the language pairs it can translate

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/list/tool/{tool}/
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformlisttooltool-get-openapi.md
- name: Wikipedia Fetch the dictionary meaning of a word
  x-api-slug: wikipedia
  description: |-
    Fetches the dictionary meaning of a word from a language and displays
    it in the target language.

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/word/from/{from_lang}/to/{to_lang}/{word}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformwordfromfrom-langtoto-langword-get-openapi.md
- name: Wikipedia Fetch the dictionary meaning of a word
  x-api-slug: wikipedia
  description: |-
    Fetches the dictionary meaning of a word from a language and displays
    it in the target language.

    Stability: [unstable](https://www.mediawiki.org/wiki/API_versioning#Unstable)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1//transform/word/from/{from_lang}/to/{to_lang}/{word}/{provider}
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/transformwordfromfrom-langtoto-langwordprovider-get-openapi.md
- name: Wikipedia
  x-api-slug: wikipedia
  description: Wikipedia is a free online encyclopedia, created and edited by volunteers
    around the world and hosted by the Wikimedia Foundation.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/144-wikipedia.jpg
  humanURL: https://www.wikipedia.org/
  baseURL: https://wikimedia.org//api/rest_v1
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/wikipedia/openapi.md
x-common:
- type: x-base
  url: http://en.wikipedia.org/w/api.php
- type: x-crunchbase
  url: https://crunchbase.com/organization/wikipedia
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
- type: x-website
  url: http://wikipedia.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---