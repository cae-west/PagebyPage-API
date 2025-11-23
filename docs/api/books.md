# `books` resource

The `books` resource has data about books in a user's library.

## Base endpoint

```bash
{base_url}/books
```

Throughout the API documentation, `{base_url}` represents the root URL where the service runs.

For local development environments, the `{base_url}` is generally `http://localhost:3000`.

## Resource properties

sample `books` resource

```json
  {
      "id": 1,
      "title": "1984",
      "author": "George Orwell",
      "totalPages": 328,
      "currentPage": 328,
      "status": "completed"
    }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The book's unique ID |
| `title` | string | Book title|
| `author` | string | Book author |
| `totalPages` | number | Total pages |
| `currentPage` | number | Page the user is on  |
| `status` | string | completed, reading, to-read|

### Jump to

- Information about the [journalEntries](journalEntries.md) resource.
- [Set up](../tutorials/prerequisites.md) for installation.
- Logging your first [book](../tutorials/log-first-book.md).

### Related topics

- [Delete](../tutorials/delete-book.md) a book entry.
- [Update](../tutorials/update-book.md) a book entry.
- [Search](../tutorials/search-library.md) by book id.
