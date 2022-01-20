# Step07 - Open API Testing and Development with Swagger and Postman

## Class Notes

- Use [Swagger editor](https://editor.swagger.io/)
  - Enter open api version
  - from insert tab add info with title and version
  - All the information can be added from the insert tab
- [Designing APIs with Swagger and OpenAPI](https://www.manning.com/books/designing-apis-with-swagger-and-openapi)

  - Chapter 04

    ```yml
    openapi: 3.0.0
    info:
      title: FarmStall API
      version: v1
    servers:
      - url: https://farmstall.ponelat.com/v1
    paths:
      /reviews:
        get:
          description: Get a bunch of reviews.
          parameters:
            - name: maxRating
              description: Filter the reviews by the maximum rating
              in: query
              schema:
                type: number
          responses:
            '200':
              description: A bunch of reviews
    ```

  - Chapter 05

    - Status Codes
      Status | Status text | Description
      --- | --- | ---
      101 | Switching Protocols | Typically used to upgrade to a websocket connection
      200 | Ok | The request was successfully executed
      201 | Created | A new resource was successfully created
      301 | Moved Permanently | Redirect to another URL, which the client can always do in future.
      403 | Forbidden | Elevated permissions are required
      404 | Not Found | The resource asked for was not found
      504 | Gateway Timeout | The proxy/gateway could not reach the backend server

    - Status code categories
      Range | Category | Notes
      --- | --- | ---
      1xx | Informational | Most common is when a websocket connection is upgraded
      2xx | Success | This indicates some form of success like the general or the 200 201 for created
      3xx | Redirects | The resource has a different location/URI
      4xx | Client Error | The client did something wrong like misspell a resource or provide invalid details
      5xx | Server Error | The server hit an error that isn’t a fault of the client

    - Media Types (aka MIME)
      | MIME | Description |
      | --- | --- |
      | text/html | The HTML you get back from a webserver |
      | text/csv | Comma separate values |
      | image/png | PNG encoded image |
      | application/json | JSON data |
      | application/xml | XML data |

## Reading Material

- [Design and Prototype an API](https://www.youtube.com/watch?v=r4kb3jOSsmk&ab_channel=Postman)
- [API Testing and Development with Postman Book](https://www.packtpub.com/product/api-testing-and-development-with-postman/9781800569201)
- [Book on Oreilly Website](https://www.oreilly.com/library/view/api-testing-and/9781800569201/)
- [Book Repo](https://github.com/PacktPublishing/API-Testing-and-Development-with-Postman)
