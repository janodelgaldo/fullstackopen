```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    Note right of browser: Usuario escribe una nota y hace click en Save

    browser->>server: POST /nueva_nota
    activate server
    server-->>browser: Nota guardada.
    deactivate server

    Note right of browser: browser actualiza la lista sin recargar