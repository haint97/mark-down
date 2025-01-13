```mermaid
flowchart TD
    start([Start])
    A[Customer receives OTP]
    B[Customer goes to locker]
    C[Customer enters code]
    D{Code validation}
    E[Search for locker]
    F[Open locker]
    G[Customer picks up product]
    end([End])

    start --> A
    A --> B
    B --> C
    C --> D
    D -- Incorrect --> C
    D -- Correct --> E
    E --> F
    F --> G
    G --> end

