---
# markdownlint-disable
# vale off
layout: default
parent: Overview
nav_order: 2
---
# `journalEntries` resource

The `journalEntries` resource contains information about a user's reading status and notes on their recorded book.

## Base endpoint

```bash
{base_url}/journalEntries
```

Throughout the API documentation, `{base_url}` represents the root URL where the service runs.

For local development environments, the `{base_url}` is generally `http://localhost:3000`.

## Resource properties

sample `journalEntries` resource

```json
   {
      "id": 1,
      "bookId": 1,
      "pageNumber": 245,
      "date": "2025-08-10",
      "notes": "Winston's torture in the Ministry of Love is brutal. The breaking of his spirit shows the ultimate power of totalitarian control. O'Brien's words are haunting.",
      "impressions": "disturbed"
    }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The journal entry's unique record id |
| `bookId` | number | The id associated with the books' resource id |
| `pageNumber` | number | Page number associated with this journal entry |
| `date` | string | Timestamp of entry creation |
| `notes` | string | User-provided notes or annotations  |
| `impression` | string | User's record of thoughts or impressions about the reading |

### Jump to

- Information about the [books](books.md) resource
[Set up](../tutorials/prerequisites.md) for installation.
- Creating your first [journal entry](../tutorials/create-journal-entry.md).

### Related topics

- [Track](../tutorials/track-progress.md) your reading progress.
- [Update](../tutorials/update-book.md) a book entry.
- [Search](../tutorials/search-library.md) by book id.
