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

## Reading Material

- [Design and Prototype an API](https://www.youtube.com/watch?v=r4kb3jOSsmk&ab_channel=Postman)
- [API Testing and Development with Postman Book](https://www.packtpub.com/product/api-testing-and-development-with-postman/9781800569201)
- [Book on Oreilly Website](https://www.oreilly.com/library/view/api-testing-and/9781800569201/)
- [Book Repo](https://github.com/PacktPublishing/API-Testing-and-Development-with-Postman)
