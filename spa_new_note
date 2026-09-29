#### 0.6: New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note and clicks the Save button

    browser->>server: POST /exampleapp/new_note_spa
    activate server
    server-->>browser: JSON containing the new note
    deactivate server

    Note right of browser: Browser adds the new note to the page

    Note right of browser: Browser updates the displayed notes without reloading the page
```
