```mermaid
sequenceDiagram
    participant Organizer
    participant Scheduler
    participant MeetingRoom
    participant Meeting
    participant Calendar
    participant Attendee

    Organizer->>Scheduler: scheduleMeeting(attendee, interval)
    Scheduler->>MeetingRoom: roomAvailability(interval)
    MeetingRoom-->>Scheduler: [room available]

    alt room available
        Scheduler->>MeetingRoom: bookRoom(interval)
        MeetingRoom-->>Scheduler: room booked
        Scheduler->>Meeting: createMeeting(room, attendees, interval)
        Meeting->>Calendar: updateCalendar(meeting)
        Calendar-->>Meeting: calendar updated
        Meeting->>Attendee: sendInvite()
        Scheduler-->>Organizer: meeting scheduled
    else room unavailable
        Scheduler-->>Organizer: select another interval
    end
