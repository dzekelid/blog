swagger: "2.0"
x-collection-name: Blogger
x-complete: 1
info:
  title: Blogger
  description: api-for-access-to-the-data-within-blogger-
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /blogger/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /blogs/byurl:
    get:
      summary: Get Blog by URL
      description: Retrieve a Blog by URL.
      operationId: blogger.blogs.getByUrl
      x-api-path-slug: blogsbyurl-get
      parameters:
      - in: query
        name: url
        description: The URL of the blog to retrieve
      - in: query
        name: view
        description: Access level with which to view the blog
      responses:
        200:
          description: OK
      tags:
      - Blog
  /blogs/{blogId}:
    get:
      summary: Get Blog
      description: Gets one blog by ID.
      operationId: blogger.blogs.get
      x-api-path-slug: blogsblogid-get
      parameters:
      - in: path
        name: blogId
        description: The ID of the blog to get
      - in: query
        name: maxPosts
        description: Maximum number of posts to pull back with the blog
      - in: query
        name: view
        description: Access level with which to view the blog
      responses:
        200:
          description: OK
      tags:
      - Blog