---
# markdownlint-disable
# vale off
layout: deafult
parent: Tutorials
nav_order: 2
# tags used by AI files
description: Get all 'collections' from the collection resource
tags:
    - api
categories:
    - tutorials
ai_relevance: high
importance: 6
---
# Tutorial: Delete a book by id

This tutorial demonstrates how to remove a specific book from your library using its unique id.

This tutorial takes about 5 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Delete a book by id

Removing a specific book requires the use of the `DELETE` method to remove the [book](../api/books.md) resource from the service.

Follow the steps below to delete a book by id:

1. Start your local service by using the following command:

     ```bash
        cd <your-github-workspace>/PagebyPage-API/api>
        json-server -w pagebypage-db-source.json
     ```

1. Open the Postman app.

1. Select `DELETE` in the left hand corner.

1. Enter the {{base_url}}/books/{id} URL, replacing `{id}` with the id of the book you want to delete.

    For example, to delete the book with id 7, use:

     ```json
        {{base_url}}/books/7
     ```

1. Make the request by selecting **Send**.

## Confirm success

A successful response in Postman returns a status code of `200 OK` with an empty response body:

```json
{}
```

You can verify the deletion by attempting to retrieve the same book id using a `GET` request. This should return a `404 Not Found` error.

## Common errors

Common errors include incorrect id references and attempting to delete non-existent books.

Verify that the book id in the URL corresponds to an existing book in your database. If you receive a 404 error before deleting, the book with that id doesn't exist in your library.

## Helpful links

**[Home](../index.md)**

**[Log your first book](log-first-book.md)**

**[Track your reading progress](track-progress.md)**

**[Update book details](update-book.md)**

**[Search your library](search-library.md)**

**[Create journal entry](create-journal-entry.md)**
