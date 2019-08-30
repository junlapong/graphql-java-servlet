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

```
mkdir data

mongod  --dbpath ./data
```

## Authentication

### Create User
```graphql
mutation {
  createUser(
    name: "Jun Lee"
    authProvider: {
      email: "junlapong@gmail.com"
      password: "secret"}) {
    id
    name
  }
}
```

```json
{
  "data": {
    "createUser": {
      "id": "5d6789f81dd7d22261541c07",
      "name": "Jun Lee"
    }
  }
}
```

### Signin

```graphql
mutation {
  signinUser(auth: {
    email: "junlapong@gmail.com"
    password: "secret"
  }) {
    token
    user {
      id
      name
    }
  }
}
```

### Create Link

```graphql
mutation link {
  createLink(
    url: "https://www.apple.com"
    description: "Apple"
  ) {
    url
  }
}
```

```graphql
query all {
  allLinks {
    id
    url
    description
    postedBy {
      id
      name
    }
  }
}
```

### Create Vote

```graphql
mutation voting {
  createVote(
    linkId: "5d6791971dd7d22aa966b435"
    userId: "5d6789f81dd7d22261541c07"
  ) {
    createdAt
    link {
      url
    }
    user {
      name
    }
  }
}
```

```json
{
  "data": {
    "createVote": {
      "createdAt": "2019-08-30T06:51:20.789Z",
      "link": {
        "url": "5d6791971dd7d22aa966b435"
      },
      "user": {
        "name": "Jun Lee"
      }
    }
  }
}
```
