```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    user->>browser: Siirtyy osoitteeseen /spa
    browser->>server: GET /spa
    server-->>browser: HTML-sivu

    browser->>server: GET /main.css
    server-->>browser: CSS-tiedosto

    browser->>server: GET /spa.js
    server-->>browser: JavaScript-tiedosto

    Note right of browser: JavaScript käynnistyy

    browser->>server: GET /data.json
    server-->>browser: JSON-data muistiinpanoista

    Note right of browser: Selain renderöi muistiinpanot
```
