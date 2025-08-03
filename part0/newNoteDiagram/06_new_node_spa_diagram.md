sequenceDiagram
    participant browser
    participant server

    Note right of browser: User fills form and clicks "Save"<br/>JavaScript intercepts the event using event listeners.

    browser->>server: POST /exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: JavaScript updates the page dynamically<br/>by adding the new note to the list.
