# Tutorial: Update book details

This tutorial demonstrates the operations to call to update the details of an existing book in the service.

This tutorial takes about 10 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Update book details

Updating the details of an existing book requires the use of the `PATCH` method to update the [book](../api/books.md) resource in the service.

Follow the steps below to update book details:

1. Start your local service by using this command:

    ```bash
    cd <your-github-workspace>/PagebyPage-API/api>
    json-server -w pagebypage-db-source.json
    ```

1. Open the Postman app.

1. Select `PATCH` in the left hand corner.

1. Enter the {{base_url}}/books/{id} URL, replacing `{id}` with the id of the book you want to update.

1. Navigate to "Headers" and select: `Content-Type: application/json`.

1. In the request body enter the properties you want to update.

    ```json
    {
        "currentPage": 324
        "status": "completed"
    }
    ```

1. Make the request by selecting **Send**.

## Confirm success

A successful body response in Postman looks like this:

```json
{
    "id": 3,
    "title": "To Kill A Mockingbird",
    "author": "Harper Lee",
    "totalPages": 324,
    "currentPage": 324
    "status": "completed"
}

```

## Common errors

Common errors include syntax errors and incorrect id references.

Confirm you are using numeric values without quotes for `totalPages` and `currentPage`, while `title`, `author`, and `status` are text strings with quotes. Also verify that the book id in the URL corresponds to an existing book in your database.

## Helpful links

**[Home](../index.md)**

**[Log your first book](log-first-book.md)**

**[Track your reading progress](track-progress.md)**

**[Create journal entry](create-journal-entry.md)**

**[Search your library](search-library.md)**

**[Delete a book from your library](delete-book.md)**
