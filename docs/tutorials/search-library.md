# Tutorial: Search library by book id

This tutorial demonstrates how to retrieve a specific book from your library using its unique id.

This tutorial takes about 5 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Get a book by id

Retrieving a specific book requires the use of the `GET` method to access the [book](../api/books.md) resource in the service.

To get a book by id:

### Step 1. Start your local service by using this command

```bash
cd <your-github-workspace>/PagebyPage-API/api>
json-server -w pagebypage-db-source.json
```

### Step 2. Open the Postman app

### Step 3. Select `GET` in the left hand corner

### Step 4. Enter the {{base_url}}/books/{id} URL, replacing `{id}` with the id of the book you want to retrieve

For example, to retrieve the book with id 7, use:

```json
{{base_url}}/books/7
```

### Step 5. Make the request by selecting **Send**

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

Common errors include incorrect id references and malformed URLs.

Verify that the book id in the URL corresponds to an existing book in your database. If you receive a 404 error, the book with that id may not exist in your library.

## Helpful links

**[Home](../index.md)**

**[Create journal entry](create-journal-entry.md)**

**[Track your reading progress](track-progress.md)**

**[Update book details](update-book.md)**

**[Search your library](search-library.md)**

**[Delete a book from your library](delete-book.md)**
