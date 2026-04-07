```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    User->>Browser: Kirjoittaa muistiinpanon ja painaa "tallenna"
    Browser->>Server: POST /new_note (sisältää muistiinpanon)
    Servers-->>Browser: 302 Redirect /notes 
    Browser->>server: GET /notes
    server-->>Browser: HTML-sivu (Päivitetty muistiinpanolista)
    browser-->>User: Näyttää uuden muistiinpanon
