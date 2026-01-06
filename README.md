# flightBookingSystem

```mermaid
flowchart LR
    Start([Start]) --> Search[Search Flights]
    Search --> Results{Flights Found?}
    
    Results -- No --> Search
    Results -- Yes --> Select[Select Flight & Seat]
    
    Select --> Auth{User Logged In?}
    Auth -- No --> Login[Login / Register]
    Login --> Payment
    Auth -- Yes --> Payment[Process Payment]
    
    Payment --> Success{Payment Success?}
    Success -- No --> Retry[Retry Payment]
    Retry --> Payment
    
    Success -- Yes --> Confirm[Generate Ticket]
    Confirm --> End([End])

    style Start fill:#f9f,stroke:#333,stroke-width:2px
    style End fill:#f9f,stroke:#333,stroke-width:2px
    style Success fill:#00ff00,stroke:#333
