---
# markdownlint-disable
# vale off
layout: default:
parent: Tutorials
nav_order: 5
# tags used by AI files
description: Get all 'collections' from the collection resource
tags:
    - api
categories:
    - tutorials
ai_relevance: high
importance: 6
---
# Tutorial: Update a journal entry

This tutorial demonstrates the operations to call to update the page number of an existing journal entry in the service.

This tutorial takes about 10 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Update a journal entry page number

Updating the page number of an existing journal entry requires the use of the `PATCH` method to update the [journal entry](../api/journalEntries.md) resource in the service.

Follow the steps below to update a journal entry page number:

1. Start your local service by using the following command:

    ```bash
    cd <your-github-workspace>/PagebyPage-API/api>
    json-server -w pagebypabe-db-source.json
    ```

1. Open the Postman app.

1. Select `PATCH` in the left hand corner.

1. Enter the {{base_url}}/journalEntries/{id} URL, replacing `{id}` with the id of the journal entry you want to update.

1. Navigate to "Headers" and select: `Content-Type: application/json`.

1. In the request body enter the updated page number value.

    ```json
    {
        "pageNumber": 300
    }
    ```

1. Make the request by selecting **Send**.

## Confirm success

A successful body response in Postman looks like this:

```json
{
    "bookId": 1,
    "pageNumber": 300,
    "date": "2025-08-10",
    "notes": "Winston's torture in the Ministry of Love is brutal. The breaking of his spirit shows the ultimate power of totalitarian control. O'Brien's words are haunting.",
    "impressions": "disturbed",
    "id": 1
}
```

## Common errors

Common errors include syntax errors and incorrect id references.

Confirm you are using a numeric value without quotes for `pageNumber`. Also verify that the journal entry id in the URL corresponds to an existing entry in your database.

## Helpful links

**[Home](../index.md)**

**[Create journal entry](create-journal-entry.md)**

**[Log your first book](log-first-book.md)**

**[Update book details](update-book.md)**

**[Search your library](search-library.md)**

**[Delete a book from your library](delete-book.md)**
