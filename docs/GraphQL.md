# GraphQL API
### 1. What is GraphQL?
GraphQL is a query language and server-side runtime for application programming interfaces 
(APIs) that prioritizes giving clients exactly the data they request and no more.
With GraphQL Developers can build APIs with whatever methods they prefer, and the GraphQL 
specification will ensure they function in predictable ways to clients.

### 2. Benefits
* Clients get what they request with no overfetching
* A GraphQL schema sets a single source of truth in a GraphQL application
* GraphQL does not dictate a specific application architecture. And It can also be introduced on top of
  an existing REST API

### 3. Drawbacks
* Presents a learning curve for developers familiar with REST APIs
* Shifts much of the work of a data query to the server side -> increased complexity for server devs
* API maintainers have to create a GraphQL schema.

### GraphQL Queries
In GraphQL the result of a query has exactly the same shape so you always get back what you expect. 


Example Query:

```js
{
  book(id: 123) {
    title
    genre
    reviews
    author {
        name
        bio
        books {
            name
        }
    }
  }
}
```

Response:

```JSON
{
    "data": {
        "book": {
            "title": "Booktitle",
            "genre": "Bookgenre",
            "reviews": "Bookreviews",
            "author": {
                "name": "Authorname",
                "bio": "Authorbio",
                "books": [
                    {
                        "name": "Book1name"
                    },
                    {
                        "name": "Book2name"
                    }
                ]
            }
        }
    }
}
```
