swagger: "2.0"
x-collection-name: Healthcare.gov
x-complete: 1
info:
  title: Healthcare
  version: 1.0.0
host: www.healthcare.gov
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/blog{mediaTypeExtension}:
    get:
      summary: Get Blog
      description: Returns pages content.
      operationId: getApiBlogMediatypeextension
      x-api-path-slug: apiblogmediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      responses:
        200:
          description: OK
      tags:
      - Blog
  /blog/{pageName}{mediaTypeExtension}:
    get:
      summary: Get Blog Pagename
      description: Returns pages content.
      operationId: getBlogPagenameMediatypeextension
      x-api-path-slug: blogpagenamemediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      - in: path
        name: pageName
      responses:
        200:
          description: OK
      tags:
      - Blog
      - Pagename
  /es/blog/{pageName}{mediaTypeExtension}:
    get:
      summary: Get Es Blog Pagename
      description: Returns pages content.
      operationId: getEsBlogPagenameMediatypeextension
      x-api-path-slug: esblogpagenamemediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      - in: path
        name: pageName
      responses:
        200:
          description: OK
      tags:
      - Es
      - Blog
      - Pagename