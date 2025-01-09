
sequenceDiagram
    participant User
    participant Browser
    participant SPA
    participant Server

    User->>Browser: Types new note and clicks "Save"
    Browser->>SPA: Sends new note data to SPA (via JavaScript)
    SPA->>Server: Sends new note data to server via API
    Server->>SPA: Confirms new note creation
    SPA->>Browser: Updates UI with the new note (no page reload)
