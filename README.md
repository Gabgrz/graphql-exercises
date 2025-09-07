# GraphQL Exercises

A Spring Boot application demonstrating GraphQL with Java.

## Features

- GraphQL API for book and author data
- Query books by ID with author details
- Spring Boot 2.1.2 with GraphQL Java

## Quick Start

```bash
cd book-details
./gradlew bootRun
```

Visit `http://localhost:8080/graphql` for the GraphQL playground.

## Schema

```graphql
type Query {
    bookById(id: ID): Book
}

type Book {
    id: ID
    name: String
    pageCount: Int
    author: Author
}

type Author {
    id: ID
    firstName: String
    lastName: String
}
```

## Example Query

```graphql
{
  bookById(id: "book-1") {
    id
    name
    pageCount
    author {
      firstName
      lastName
    }
  }
}
```
