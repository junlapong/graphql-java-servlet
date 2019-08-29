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

## Mutation

```graphql
mutation {
  createLink(url: "http://www.google.com", description: "Google") {
    url
    description
  }
}
```

## Connect with MongoDB

### Start Mongodb

``
mkdir data
mongod  --dbpath ./data
``

