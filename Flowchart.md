

flowchart TD
    A([START]) --> B[Initialize Head = NULL]
    B --> C[Display Main Menu]
    C --> D[Enter Choice]

    D -->|1. Add Vehicle| E[Enter Vehicle Number]
    E --> F[Add Vehicle Node]
    F --> C

    D -->|2. Display Vehicles| G[Display All Vehicles]
    G --> C

    D -->|3. Search Vehicle| H[Enter Vehicle Number]
    H --> I[Search Vehicle]
    I --> C

    D -->|4. Remove Vehicle| J[Enter Vehicle Number]
    J --> K[Remove Vehicle Node]
    K --> C

    D -->|5. Exit| L([STOP])