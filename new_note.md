#### 0.4: New note diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note in the text field and clicks the Save button

    browser->>server: POST /exampleapp/new_note
    activate server
    Note right of server: The server receives and saves the new note
    server-->>browser: 302 Redirect to /exampleapp/notes
    deactivate server

    browser->>server: GET /exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET /exampleapp/main.css
    activate server
    server-->>browser: CSS file
    deactivate server

    browser->>server: GET /exampleapp/main.js
    activate server
    server-->>browser: JavaScript file
    deactivate server

    Note right of browser: Browser executes the JavaScript

    browser->>server: GET /exampleapp/data.json
    activate server
    server-->>browser: JSON containing the notes, including the new note
    deactivate server

    Note right of browser: Browser renders the notes, including the new note
```
