
```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Writes note and clicks "Save"
    Browser->>Server: Sends HTTP POST request with note data
    Server-->>Browser: Sends response (e.g., 201 Created)
    Browser->>Browser: Reloads the notes page
    Browser->>User: Displays the updated list of notes
