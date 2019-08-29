# GraphQL Client in Vanilla JS

from [Writing a GraphQL Client in Vanilla JS](https://link.medium.com/L7H21CwgxZ) by Shlok Desai

```
graphql-faker ./schema/books.graphql
```

```graphql
{
  allBooks {
    id
    author
    title
    url
  }
}
```

```json
{
  "data": {
    "allBooks": [
      {
        "id": "07de8ae8-ab88-4ba5-97d3-3f0b290f0b63",
        "author": "結菜",
        "title": "Central Integration Manager",
        "url": "https://www.facebook.com"
      },
      {
        "id": "7381b835-6e94-47fc-bafc-05f5dea47861",
        "author": "蓮",
        "title": "Chief Group Director",
        "url": "https://www.facebook.com"
      },
      {
        "id": "04c447ed-59e1-46d9-b2b0-eecf3692d0fb",
        "author": "大和",
        "title": "International Accountability Executive",
        "url": "https://www.google.com"
      }
    ]
  }
}
```