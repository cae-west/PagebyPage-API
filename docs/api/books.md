# `books` resource

The `books` resource has data about books in a user's library.

## Base endpoint

```shell
{base_url}/books
```

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
    },
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The book's unique ID |
| `title` | string | Book title|
| `author` | string | Book author |
| `totalPages` | number | Total pages |
| `currentPage` | number | Page the user is on  |
| `status` | string | Done, in progress, or not started|

### Other resources

Refer to the [journalEntries](journalEntries.md) resource.
