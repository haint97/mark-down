mermaid
sequenceDiagram
    participant Customer
    participant System
    participant Locker
    Customer->>System: requestReturn(package)
    alt request approved
        System->>Customer: send OTP code
        Customer->>System: verifyOTP(code)
        alt verification successful
            System->>Locker: requestLocker()
            Locker->>System: return locker
            System->>Customer: assign locker
            Customer->>Locker: place package
        else verification failed
            System->>Customer: error
        end
    else request unapproved
        System->>Customer: return not approved
    end
