# Tutorial: Update a journal entry page number

This tutorial demonstrates the operations to call to update the page number of an existing journal entry in the service.

This tutorial takes about 10 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Update a journal entry page number

Updating the page number of an existing journal entry requires the use of the `PATCH` method to modify the [journal entry](../api/journalEntries.md) resource in the service.

To update a journal entry page number:

### Step 1. Start your local service by using this command

```bash
cd <your-github-workspace>/PagebyPage-API/api>
json-server -w pagebypabe-db-source.json
```

### Step 2. Open the Postman app

### Step 3. Select `PATCH` in the left hand corner

### Step 4. Enter the {{base_url}}/journalEntries/{id} URL, replacing `{id}` with the id of the journal entry you want to update

### Step 5. Navigate to "Headers" and select

- `Content-Type: application/json`

1. In the request body enter the updated page number value.

```json
{
    "pageNumber": 300
}
```

### Step 6. Make the request by selecting **Send**

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
