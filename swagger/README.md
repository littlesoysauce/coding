# Swagger API
https://app.swaggerhub.com/help/tutorials/writing-swagger-definitions
## What is Swagger?
If you've ever worked with APIs, chances are, you've heard of Swagger. Swagger is the most widely used tooling ecosystem for developing APIs with the OPENAPI Specification (OAS). Swagger consists of both open source as well as professional tools, catering to almost every need and use case.

Swagger is an open-source framework for designing and describing APIs. Swagger's journey started in 2010 when it was developed by Reverb Technologies to solve the need for keeping the API design and documentation in sync. Fast Forward 6 years and Swagger has become the de-facto standard for designing and describing Restful apis by millions of developers and organizations for developing their APIs, be it internal or client facing.

In this tutorial, we will write an API definition in the Swagger 2.0 format (also known as OpenAPI 2.0). Swagger can be written in JSON or YAML, though we recommend writing it in YAML, because it is easier to read and understand.
```
swagger: '2.0'
info:
    version: 1.0.0
    title: Simple example API
    description: An API to illustrate Swagger
paths:
    /list:
     get:
        description: Returns a list of stuff
        responses:
            200:
                description: Successful response
```
The syntax above will make sense once we finish this walkthrough
## Why Swagger?
There are a lot of factors that contributed to Swagger's meteoric adoption for building RESTful APIs. We have listed the most important ones as to why use Swagger for designing APIs:
* Design and document APIs simultaneously, thus keeping the blueprint and documentation in sync.
* Both human and machine readable, with an interactive API documentation automatically generated to see the API in action
* Large comprehensive tooling ecosystem around the framework, which lets you go beyond just design, from SDK generation to testing and debugging
* Strong open source community supporting and spearheading the framework

## Prerequisites
* Basic knowledge of RESTFUL APIs
## Nice to have
* Basic knowledge of YAML

## Creating an API
We will be designing an API for a record label. Let's assume that the record label has a database of artists with the follwing information:
* Artist name
* Artist genre
* Number of albums published under the label
* Artist username

The API will let consumers obtain the list of artists stored in the database and add a new artist to the database
The Swagger definition of an API can be divided into 3 different sections
* The Meta Information
* The Path items:
    - Parameters
    - Responses
* Reusuable compoennts:
    - Definitions
    - Parameters
    - Responses

## The meta Information
The meta information section is where you can give information about your overall API information like what the API does, what the bsae URL of the API is and what web-based protocol it follows can be defined in this section.

All Swagger defined API start with the swagger 2.0 declaration. The info object is then specified with additional, required metadat alike the version and title. The description is optional.

The base URL is what any application or end user will call in order to consume the API. In this case, it is https://example.io/v1, which is defined by the schemes, host and basePath objects respectively.

We can also add a basic authentication which only lets authorized users consume the API.

Let's start with a simple meta information section
```
swagger: '2.0'
info:
  version: 1.0.0
  title: Simple Artist API
  description: A simple API to understand the Swagger Specification in greater detail
schemes: 
- https
host: example.io
basePath: /v1
securityDefinitions:
  UserSecurity:
    type: basic
security:
  - UserSecurity: [] 
paths: {}
```
## The Path items
The path items are the endpoints of your API under which you can specify HTTP verbs for manipulating the resources in the desired manner. These endpoints are relative to the base URL. In this example, we have listed the /artists endpoint under which is ghte GET method.
Thus, a client would use GET http://example.io/v1/artists to obtain a list of artists.
```
paths:
    /artists:
        get:
         description: Returns a list of artists
```
## The responses
The GET method, under the artists endpoint, lets the consumer of the API obtain the details of a list of artists from hte http://example.io.v1 databse.
Every response would need at least one HTTP status code to describe the kind of responses a consumer is likely to expect. The description gives details on what the responses of the API would be. In our sample code, we have specified 200, which is a successful client request, while 400 is an unsuccessful request. You can find more information about HTTP status code here. A successful response will return the artist name, genre, username and albums recorded. An unsuccessful request is described under the 400 HTTP code, with a corresponding error message detailing why the response is invalid.
```
responses:
    200:
        description: Successfully returned a list of artists
        schema:
            type: array
            items:
                type: object
                required:
                    - username
                properties:
                    artist_name:
                        type: string
                    artist_genre:
                        type: string
                    albums_recorded:
                        type: integer
                    username:
                        type: string
    400:
        description: Invalid request
        schema:
            type: object
            properties:
                message:
                    type: string
```
## The parameters
Restful parameters specify the variable part of the resource a user works with. If you want to get some advanced information on parameters.

