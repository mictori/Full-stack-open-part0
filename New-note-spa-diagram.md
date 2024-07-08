sequenceDiagram

    participant browser
    participant server
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

     Note right of browser: Request content: {"content":"new","date":"2024-07-08T16:02:29.394Z"}

    server-->>browser: the json file
    deactivate server

    Note left of server: Response content: {"message":"note created"}