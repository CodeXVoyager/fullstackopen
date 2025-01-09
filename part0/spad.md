
sequenceDiagram
    participant User
    participant Browser
    participant Server
    participant SPA

    User->>Browser: Opens URL (https://studies.cs.helsinki.fi/exampleapp/spa)
    Browser->>Server: Requests SPA HTML, JS, CSS files
    Server->>Browser: Sends HTML, JS, CSS files
    Browser->>SPA: Executes JavaScript (SPA takes over)
    SPA->>Server: Fetches notes data via API call
    Server->>SPA: Returns notes data
    SPA->>Browser: Renders notes dynamically
    User->>SPA: Interacts with the app (e.g., add/delete note)
    SPA->>Server: Sends changes to the server (e.g., new note)
    Server->>SPA: Confirms the update
    SPA->>Browser: Updates UI without page reload
