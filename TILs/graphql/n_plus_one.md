# GraphQL N+1 problem

The N+1 problem of GraphQL is that one query can trigger multiple requests to APIs or DB. For example, if you want to fetch all authors and all their books, GraphQL will first get all the authors (1) when you hit the author field resolver; then it will trigger N DB queries for every author in the list when you hit the book field resolver.

One solution is to introduce data loader, which will batch the DB queries and make N to 1.
