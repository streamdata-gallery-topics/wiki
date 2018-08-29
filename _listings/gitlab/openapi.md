swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/services/external-wiki:
    put:
      summary: Put Projects Services External Wiki
      description: Set external-wiki service for project
      operationId: putV3ProjectsIdServicesExternalWiki
      x-api-path-slug: v3projectsidservicesexternalwiki-put
      parameters:
      - in: formData
        name: external_wiki_url
        description: The URL of the external Wiki
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Services
      - External
      - Wiki