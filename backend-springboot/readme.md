``` yaml
# YAML
openapi: 3.0.1
info:
  title: OpenAPI definition
  version: v0
servers:
- url: http://localhost:8080
  description: Generated server url
paths:
  /api/v1/products/category/{category}:
    get:
      tags:
      - product-catelog-controller
      description: retrieve all products by category
      operationId: getAllProductsByCategory
      parameters:
      - name: category
        in: path
        description: product category identifier
        required: true
        schema:
          type: string
        example: Commercial
      responses:
        "404":
          description: Not Found
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/ProductCatelog'
        "200":
          description: Ok
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ProductCatelog'
  /api/v1/products:
    get:
      tags:
      - product-catelog-controller
      description: retrieve all products
      operationId: getAllProducts
      responses:
        "200":
          description: Ok
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ProductCatelog'
  /swagger-resources/configuration/ui:
    get:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_5
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    put:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_2
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    post:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_1
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    delete:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_3
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    options:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_6
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    head:
      tags:
      - api-resource-controller
      operationId: uiConfiguration_4
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
    patch:
      tags:
      - api-resource-controller
      operationId: uiConfiguration
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/UiConfiguration'
  /swagger-resources/configuration/security:
    get:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_5
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    put:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_2
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    post:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_1
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    delete:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_3
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    options:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_6
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    head:
      tags:
      - api-resource-controller
      operationId: securityConfiguration_4
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
    patch:
      tags:
      - api-resource-controller
      operationId: securityConfiguration
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/SecurityConfiguration'
  /swagger-resources:
    get:
      tags:
      - api-resource-controller
      operationId: swaggerResources_5
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    put:
      tags:
      - api-resource-controller
      operationId: swaggerResources_2
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    post:
      tags:
      - api-resource-controller
      operationId: swaggerResources_1
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    delete:
      tags:
      - api-resource-controller
      operationId: swaggerResources_3
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    options:
      tags:
      - api-resource-controller
      operationId: swaggerResources_6
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    head:
      tags:
      - api-resource-controller
      operationId: swaggerResources_4
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
    patch:
      tags:
      - api-resource-controller
      operationId: swaggerResources
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/SwaggerResource'
  /v2/api-docs:
    get:
      tags:
      - swagger-2-controller
      operationId: getDocumentation
      parameters:
      - name: group
        in: query
        required: false
        schema:
          type: string
      responses:
        "200":
          description: default response
          content:
            application/json:
              schema:
                type: string
            application/hal+json:
              schema:
                type: string
  /api/v1/products/update/{id}:
    put:
      tags:
      - product-catelog-controller
      description: update product
      operationId: updateProductCatelog
      parameters:
      - name: product id
        in: path
        description: unique product identifier
        required: true
        schema:
          type: integer
          format: int64
        example: 10
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/ProductCatelog'
      responses:
        "404":
          description: Not Found
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/ProductCatelog'
        "200":
          description: ok
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ProductCatelog'
  /authenticate:
    post:
      tags:
      - jwt-authentication-controller
      operationId: generateAuthenticationToken
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/JwtRequest'
      responses:
        "200":
          description: default response
          content:
            '*/*':
              schema:
                type: object
  /api/v1/products/create:
    post:
      tags:
      - product-catelog-controller
      description: create product
      operationId: createProduct
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/ProductCatelog'
      responses:
        "201":
          description: Created
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ProductCatelog'
  /api/v1/products/{id}:
    get:
      tags:
      - product-catelog-controller
      description: retrieve all products by id
      operationId: getAllProductById
      parameters:
      - name: product id
        in: path
        description: unique product identifier
        required: true
        schema:
          type: integer
          format: int64
        example: 10
      responses:
        "404":
          description: Not Found
          content:
            '*/*':
              schema:
                $ref: '#/components/schemas/ProductCatelog'
        "200":
          description: Ok
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ProductCatelog'
components:
  schemas:
    ProductCatelog:
      required:
      - productCategory
      - productName
      type: object
      properties:
        productId:
          type: integer
          format: int64
        productCategory:
          type: string
        productName:
          type: string
        productDescription:
          type: string
        units:
          type: integer
          format: int32
    UiConfiguration:
      type: object
      properties:
        validatorUrl:
          type: string
        docExpansion:
          type: string
        apisSorter:
          type: string
        defaultModelRendering:
          type: string
        supportedSubmitMethods:
          type: array
          items:
            type: string
        jsonEditor:
          type: boolean
        showRequestHeaders:
          type: boolean
    SecurityConfiguration:
      type: object
      properties:
        clientId:
          type: string
        clientSecret:
          type: string
        realm:
          type: string
        appName:
          type: string
        apiKey:
          type: string
        apiKeyVehicle:
          type: string
        scopeSeparator:
          type: string
        apiKeyName:
          type: string
    SwaggerResource:
      type: object
      properties:
        name:
          type: string
        location:
          type: string
        swaggerVersion:
          type: string
    JwtRequest:
      type: object
      properties:
        username:
          type: string
        password:
          type: string
```
