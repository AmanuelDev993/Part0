#### 0.6: New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server
    
    Note right of browser: User creates a new note and hits the Save button

    browser->>server: POST /exampleapp/new_note_spa
    activate server
    server-->>browser: JSON with the new note
    deactivate server

    Note right of browser: New note is added to the page by the browser

    Note right of browser: Notes on the page are refreshed without reloading the page
```
