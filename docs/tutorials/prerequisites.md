# Prerequisites

Perform the following steps before beginning a tutorial for the Page by Page service.

## FYI about the API

- Server: This API runs on your local machine or a chosen server environment.
- Base URL: `http://localhost:3000` or your own {base_url} server.
- Data format: JSON for all requests and responses.

## Getting started

To use the Page by Page API you need:

- A [GitHub](https://github.com/) account
- [Git](https://git-scm.com/downloads)
- [node.js](https://nodejs.org/en/download)
- [json-server](https://www.npmjs.com/package/json-server)
- [curl](https://curl.se/download.html) or [Postman desktop app](https://www.postman.com/downloads/)

## Set up

### Step 1: create a fork of the [Page by Page API repository](https://github.com/Venutom/PagebyPage-API)

### Step 2: clone your fork to your local machine

### Step 3: open your terminal and navigate to the repository

```bash
cd <your-github-workspace>/PagebyPage-API/api
```

**For example:**

```bash
cd ~/OneDrive/Documents/GitHub/PagebyPage-API/api
```

### Step 4: in that same terminal, start the JSON server

```bash
json-server -w pagebypage-db-source.json
```

**You are ready to test with curl if you see:**

```bash
Resources
http://localhost:3000/books
http://localhost:3000/journalEntries

Home
http://localhost:3000
```

## Test with curl

### Step 1: open a new terminal window and run

```bash
curl http://localhost:3000/books
```

**You are successful if you see a list of books in JSON format.**

For example:

```bash
[
  {
    "id": 1,
    "title": "1984",
    "author": "George Orwell",
    "totalPages": 328,
    "currentPage": 328,
    "status": "completed"
  },
  {
    "id": 2,
    "title": "Gideon the Ninth",
    "author": "Tamsyn Muir",
    "totalPages": 448,
    "currentPage": 448,
    "status": "completed"
  },
  {
    "id": 3,
    "title": "To Kill a Mockingbird",
    "author": "Harper Lee",
    "totalPages": 324,
    "currentPage": 156,
    "status": "reading"
  },
  {
    "id": 4,
    "title": "Atomic Habits",
    "author": "James Clear",
    "totalPages": 320,
    "currentPage": 87,
    "status": "reading"
  },
  {
    "id": 5,
    "title": "The Midnight Library",
    "author": "Matt Haig",
    "totalPages": 304,
    "currentPage": 0,
    "status": "to-read"
  }
]
```

When you see a list of books from the service, you are ready to proceed to the [Tutorials](tutorials.md).

### Common errors

1. You aren't in the correct directory.
2. You mistyped the command.
3. Installation of a required software component didn't install correctly or is in need of an update.
