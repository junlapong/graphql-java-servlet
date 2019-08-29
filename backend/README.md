# graphql-java-servlet

## Run

    mvn jetty:run

## URL 

- Web: http://localhost:8080
- GraphQL Endpoint: http://localhost:8080/graphql

## Query

```graphql
{
  allLinks {
    url
    description
  }
}
```