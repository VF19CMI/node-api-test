# node-api-test

1. Serve the given resources as a SPA
- `/index.html`
- `/styles/index.css`
- `/scripts/index.js`

---

2. Create the following endpoints
- `GET /api/posts`
- `GET /api/posts/:id`
- `GET /api/posts/:id/comments`
- `GET /api/tags/:name`
  
---

2.1. `GET /api/posts` response example:
```
  {
    "data": [
      {
        "id": 1,
        "title": "...",
        "headline": "...",
        "body": "...",
        "created_at": "2023-02-11",
        "tags": ["Sports"]
      },
      {
        "id": 2,
        "title": "...",
        "headline": "...",
        "body": "...",
        "created_at": "2023-02-10",
        "tags": ["Business", "Tech"]
      },
      {
        "id": 3,
        "title": "...",
        "headline": "...",
        "body": "...",
        "created_at": "2023-02-09",
        "tags": ["Economy"]
      }
    ]
  }
```

---

2.2. `GET /api/posts/:id` response example:
```
  {
    "data": {
      "id": 1,
      "title": "...",
      "headline": "...",
      "body": "...",
      "created_at": "2023-02-11",
      "tags": ["Sports"]
    }
  }
```

---

2.3. `GET /api/posts/:id/comments` response example:
```
  {
    "data": [
      {
        "id": 1,
        "created_at": "2023-02-13",
        "author": "Test User A",
        "body": "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
      },
      {
        "id": 2,
        "created_at": "2023-02-12",
        "author": "Test User B",
        "body": "Etiam tincidunt fermentum felis, quis luctus lectus suscipit nec."
      }
    ]
  }
```
---

2.4. `GET /api/tags/:name` response example (same as 2.1.)

---

3. NOTES:
- Please Create a public github repository with your solution (and share the link with us)
- You don't have to use a database for it!
- You can use a simple object or JSON to store the data, but try to separate it at least in a different file!
- For simplicity you can return a 400 whenever it makes sense (for example post doesn't exist with a given id).
