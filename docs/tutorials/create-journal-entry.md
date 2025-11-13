# Tutorial: Create a new journal entry

This tutorial demonstrates the operations to call to create a new journal entry in the service.

This tutorial takes about 15 minutes to complete.

## Before you begin

Make sure you've completed the steps on the [prerequisites](prerequisites.md) page.

## Create a new journal entry

Adding a new journal entry to the service requires the use of the `POST` method to store the details of the new [journal entry](../api/journalEntries.md) resource in the service.

To create a new journal entry:

**Start your local service by using this command:**

```bash
cd <your-github-workspace>/PagebyPage-API/api>
json-server -w pagebypage-db-source.json
```

### Step 1. Open the Postman app

### Step 2. Select `POST` in the left hand corner

### Step 3. Enter the {{base_url}}/journalEntries URL

### Step 4. Navigate to "Headers" and select

- `Content-Type: application/json`

### Step 5. In the request body enter the values of each property per your needs

```json
{
    "bookId": 1,
    "pageNumber": 245,
    "date": "2025-08-10",
    "notes": "Winston's torture in the Ministry of Love is brutal. The breaking of his spirit shows the ultimate power of totalitarian control. O'Brien's words are haunting.",
    "impressions": "disturbed"
}
```

### Step 6. Make the request by selecting **Send**

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
