'''mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>browser: User creates a new note
    Note right of browser: User interacts with the form<br/>to create a new note
    browser->>browser: JavaScript handles form submission
    Note right of browser: JavaScript prevents default<br/>form submission behavior
    browser->>browser: JavaScript creates a new note object
    Note right of browser: JavaScript constructs a JSON object<br/>with note content and timestamp
    browser->>browser: JavaScript sends POST request to server
    Note right of browser: Data is sent to server asynchronously<br/>using XMLHttpRequest or Fetch API
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTTP Status Code 201 Created
    Note left of server: Server successfully<br/>receives and processes<br/>the new note data
    deactivate server
