# API Testing (Postman)

## Overview
A Postman collection that tests the public JSONPlaceholder demo API
(https://jsonplaceholder.typicode.com), including negative tests.

## Scope
- 15 requests in 4 folders: GET Requests, POST Requests, PUT/DELETE, Negative Tests
- GET: all posts, single post, non-existent post, comments, filter by user (query parameter)
- POST: create a new post
- PUT / PATCH / DELETE: update, partially update and delete a post
- Negative tests folder: missing token, non-existent resource, delayed response, invalid payload

## Files
- `JSONPlaceholder API Tests.postman_collection.json`: the exported collection (v2.1)

## How to run
1. Open Postman and import the collection file.
2. Create an environment with a variable `baseUrl` = `https://jsonplaceholder.typicode.com`.
3. Run the collection with the Collection Runner.

## Notes
- Only public demo APIs were used. No credentials or real data.
- The environment file is not included.
- The collection is exported as is. The "POST invalid payload" request is incomplete.