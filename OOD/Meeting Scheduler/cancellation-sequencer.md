```mermaid
sequenceDiagram
    participant Organizer
    participant Scheduler
    participant Calendar
    participant MeetingRoom
    participant Attendee

    Organizer->>Scheduler: cancelMeeting(meeting)
    Scheduler->>Calendar: removeMeeting(meeting)
    Calendar-->>Scheduler: meeting removed
    Scheduler->>MeetingRoom: updateRoomStatus(available)
    MeetingRoom-->>Scheduler: roomStatus updated
    Scheduler->>Attendee: cancelNotification()
    Scheduler-->>Organizer: meeting canceled
