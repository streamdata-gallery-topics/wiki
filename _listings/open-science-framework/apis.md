---
name: Open Science Framework
x-slug: open-science-framework
description: OSF provides free and open source project management support for researchers
  across the entire research lifecycle. As a collaboration tool, OSF helps researchers
  work on projects privately with a limited number of collaborators and make parts
  of their projects public, or make all the project publicly accessible for broader
  dissemination. As a workflow system, OSF enables connections to the many services
  researchers already use to streamline their process and increase efficiency. As
  a flexible repository, it can store and archive research data, protocols, and materials.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Wiki
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/apis.md
specificationVersion: "0.14"
apis:
- name: Open Science Framework List all wikis
  x-api-slug: open-science-framework
  description: |-
    List of wiki pages on a node.
    ####Returns
    Paginated list of the node's current wiki page versions ordered by their date_modified. Each resource contains the full representation of the wiki, meaning additional requests to an individual wiki's detail view are not necessary.

    Note that if an anonymous view_only key is being used, the user relationship will not be exposed.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
    #### Filtering
    Wiki pages can be filtered based on their `name` and `date_modified` fields.
    + `filter[name]=<Str>` -- filter wiki pages by name
    + `filter[date_modified][comparison_operator]=YYYY-MM-DDTH:M:S` -- filter wiki pages based on date modified.

    Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/wikis/
  tags: Nodes,Node,Wikis
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/nodesnode-idwikis-get-openapi.md
- name: Open Science Framework List all wikis
  x-api-slug: open-science-framework
  description: |-
    A paginated list of the registration's wiki pages
    ####Returns
    A list of all registration's current wiki page versions ordered by their date_modified. Each resource contains the full representation of the wiki, meaning additional requests to an individual wiki's detail view are not necessary.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
    #### Filtering
    Wiki pages can be filtered based on their `name` and `date_modified` fields.
    + `filter[name]=<Str>` -- filter wiki pages by name
    + `filter[date_modified][comparison_operator]=YYYY-MM-DDTH:M:S` -- filter wiki pages based on date modified.

    Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//registrations/{registration_id}/wikis/
  tags: Registrations,Registration,Wikis
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/registrationsregistration-idwikis-get-openapi.md
- name: Open Science Framework Retrieve a Wiki
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details about a specific wiki.
    A wiki is a collection of markdown text pages that can be used to describe the project or dataset of contained in the attached node.
    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested wiki, if the request was successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//wikis/{wiki_id}/
  tags: Wikis,Wiki
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/wikiswiki-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/wikiswiki-id-get-openapi.md
- name: Open Science Framework Retrieve the Content of a Wiki
  x-api-slug: open-science-framework
  description: |-
    Retrieves the plaintext content of a wiki in markdown format.
    ####Returns
    Returns `text/markdown` of the wiki content itself.
    If the request is unsuccessful, plaintext with the error message will be displayed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//wikis/{wiki_id}/content/
  tags: Wikis,Wiki,Content
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/wikiswiki-idcontent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/wikiswiki-idcontent-get-openapi.md
- name: Open Science Framework
  x-api-slug: open-science-framework
  description: OSF provides free and open source project management support for researchers
    across the entire research lifecycle. As a collaboration tool, OSF helps researchers
    work on projects privately with a limited number of collaborators and make parts
    of their projects public, or make all the project publicly accessible for broader
    dissemination. As a workflow system, OSF enables connections to the many services
    researchers already use to streamline their process and increase efficiency. As
    a flexible repository, it can store and archive research data, protocols, and
    materials.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Wiki
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/wiki/master/_listings/open-science-framework/openapi.md
x-common:
- type: x-website
  url: https://cos.io
- type: x-github
  url: https://github.com/OSFramework
- type: x-twitter
  url: https://twitter.com/OSFramework
- type: x-website
  url: http://osf.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---