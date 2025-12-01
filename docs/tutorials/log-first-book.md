---
# markdownlint-disable
# vale off
layout: default:
parent: Tutorials
nav_order: 3
# tags used by AI files
description: Get all 'collections' from the collection resource
tags:
    - api
categories:
    - tutorials
ai_relevance: high
importance: 6
---
# Tutorial: Log a new book

This tutorial demonstrates the operations to call to log a new book into the service.

This tutorial takes about 15 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Log a new book

Adding a new book to the service requires the use of the `POST` method to store the details of the new [book](../api/books.md) resource in the service.

Follow the steps below to log your first book:

1. Start your local service by using the following command:

    ```bash
        cd <your-github-workspace>/PagebyPage-API/api>
        json-server -w pagebypage-db-source.json
    ```

1. Open the Postman app.

1. Select `POST` in the left hand corner.

1. Enter the `{{base_url}}/books` URL.

1. Navigate to "Headers" and select: `Content-Type: application/json`.

    In the request body enter the values of each property per your needs.

    ```json
        {
            "title": "Fahrenheit 451",
            "author": "Ray Bradbury",
            "totalPages": 158,
            "currentPage": 100,
            "status": "reading"
        }
    ```

1. Make the request by selecting **Send**.

## Confirm success

A successful body response in Postman looks like this:

```json
{
    "title": "Fahrenheit 451",
    "author": "Ray Bradbury",
    "totalPages": 158,
    "currentPage": 100,
    "status": "reading",
    "id": 7
}
```

## Common errors

Common errors include syntax errors.

Confirm you are placing quotes around text entries and using commas to separate properties. Also ensure that `totalPages` and `currentPage` are numeric values without quotes, while `title`, `author`, and `status` are text strings with quotes.

## Helpful links

**[Home](../index.md)**

**[Update book details](update-book.md)**

**[Track your reading progress](track-progress.md)**

**[Update book details](update-book.md)**

**[Search your library](search-library.md)**

**[Create journal entry](create-journal-entry.md)**
