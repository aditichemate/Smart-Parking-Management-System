
flowchart TD
    A([START]) --> B[Initialize Head = NULL]
    B --> C[Display Main Menu]
    C --> D[Enter Choice]

    D --> E{Select Operation}

    E -->|1. Add Vehicle| F[Enter Vehicle Details]
    F --> G[Add Vehicle to Linked List]
    G --> C

    E -->|2. Remove Vehicle| H[Enter Vehicle Number]
    H --> I[Remove Vehicle from Linked List]
    I --> C

    E -->|3. Search Vehicle| J[Enter Vehicle Number]
    J --> K[Search Vehicle in Linked List]
    K --> C

    E -->|4. Display Vehicles| L[Display All Parked Vehicles]
    L --> C

    E -->|5. Exit| M([STOP])