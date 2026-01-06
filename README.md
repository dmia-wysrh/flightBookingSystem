# flightBookingSystem

graph TD;
    A[Start Process] --> B{Is it a decision point?};
    B -- Yes --> C(Action 1);
    B -- No --> D(Action 2);
    C --> E[End];
    D --> E;
