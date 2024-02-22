sequenceDiagram
    participant browser
    participant server

  
    browser->>server: POST 
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    add note
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: The browser executes the javascript adding note to the list