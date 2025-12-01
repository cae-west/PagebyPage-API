---
# markdownlint-disable
# vale off
layout: deafult
parent: Tutorials
nav_order: 1
# tags used by AI files
description: Get all 'collections' from the collection resource
tags:
    - api
categories:
    - tutorials
ai_relevance: high
importance: 6
---
# Tutorial: Create a new journal entry

This tutorial demonstrates the operations to call to create a new journal entry in the service.

This tutorial takes about 15 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Create a new journal entry

Adding a new journal entry to the service requires the use of the `POST` method to store the details of the new [journal entry](../api/journalEntries.md) resource in the service.

Follow the steps below to create a new journal entry:

1. Start your local service using the following command:

    ```bash
        cd <your-github-workspace>/PagebyPage-API/api>
        json-server -w pagebypage-db-source.json
    ```

1. Open the Postman app.

1. Select `POST` in the left hand corner.

1. Enter `{{base_url}}/journalEntries`.

1. Navigate to "Headers" and select: `Content-Type: application/json`.

1. In the request body enter the values of each property per your needs.

    ```json
        {
            "bookId": 1,
            "pageNumber": 245,
            "date": "2025-08-10",
            "notes": "Winston's torture in the Ministry of Love is brutal. The breaking of his spirit shows the ultimate power of totalitarian control. O'Brien's words are haunting.",
            "impressions": "disturbed"
        }
    ```

1. Make the request by selecting **Send**.

## Confirm success

A successful body response in Postman looks like this:

```json
{
    "bookId": 1,
    "pageNumber": 245,
    "date": "2025-08-10",
    "notes": "Winston's torture in the Ministry of Love is brutal. The breaking of his spirit shows the ultimate power of totalitarian control. O'Brien's words are haunting.",
    "impressions": "disturbed",
    "id": 2
}
```

## Common errors

Common errors include syntax errors.

Ensure that `bookId` and `pageNumber` are numeric values without quotes, while `date`, `notes`, and `impressions` are text strings with quotes. Commas are to used to separate properties.

## Helpful links

**[Home](../index.md)**

**[Log your first book](log-first-book.md)**

**[Track your reading progress](track-progress.md)**

**[Update book details](update-book.md)**

**[Search your library](search-library.md)**

**[Delete a book from your library](delete-book.md)**
