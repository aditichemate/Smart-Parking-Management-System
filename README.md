Unit 3 – Linked List
Project: Smart Parking Management System
1. Problem Statement

To develop a Smart Parking Management System using a linked list to efficiently add, delete, search, and display vehicles parked in a parking area.

2. Objectives
To manage parked vehicles efficiently.
To add and remove vehicle records dynamically.
To search for a particular vehicle.
To display all currently parked vehicles.
To understand the practical use of linked lists.
3. Data Structure

Singly Linked List

Each node contains:

Vehicle Number
Pointer to the next node

Node structure:
[Vehicle Number | Next Pointer]

4. Operations
Insertion – Add a new vehicle to the parking list.
Deletion – Remove a vehicle from the parking list.
Searching – Search for a vehicle using its number.
Display – Display all parked vehicles.
5. Algorithm
Start.
Initialize head = NULL.
Display the main menu.
Enter the user's choice.
If choice is Add Vehicle, create a new node and insert the vehicle.
If choice is Delete Vehicle, search and delete the required node.
If choice is Search Vehicle, traverse the list and find the vehicle.
6. Flowchart
  <img width="1024" height="1536" alt="WhatsApp Image 2026-10-05 at 10 57 09 PM" src="https://github.com/user-attachments/assets/3c3ebd2b-a179-4a48-b067-311e9cc01518" />
7. Code
#include <iostream>
#include <string>
using namespace std;

struct Node
{
    string number;
    Node* next;
};

Node* head = NULL;

void addVehicle()
{
    Node* temp = new Node;

    cout << "Enter vehicle number: ";
    cin >> temp->number;

    temp->next = NULL;

    if (head == NULL)
    {
        head = temp;
    }
    else
    {
        Node* p = head;

        while (p->next != NULL)
        {
            p = p->next;
        }

        p->next = temp;
    }

    cout << "Vehicle added successfully.\n";
}

void deleteVehicle()
{
    string number;
    cout << "Enter vehicle number to delete: ";
    cin >> number;

    Node* p = head;
    Node* prev = NULL;

    while (p != NULL && p->number != number)
    {
        prev = p;
        p = p->next;
    }

    if (p == NULL)
    {
        cout << "Vehicle not found.\n";
        return;
    }

    if (prev == NULL)
        head = p->next;
    else
        prev->next = p->next;

    delete p;

    cout << "Vehicle deleted successfully.\n";
}

void searchVehicle()
{
    string number;
    cout << "Enter vehicle number to search: ";
    cin >> number;

    Node* p = head;

    while (p != NULL)
    {
        if (p->number == number)
        {
            cout << "Vehicle found in parking.\n";
            return;
        }

        p = p->next;
    }

    cout << "Vehicle not found.\n";
}

void displayVehicles()
{
    Node* p = head;

    if (p == NULL)
    {
        cout << "Parking is empty.\n";
        return;
    }

    cout << "\nParked Vehicles:\n";

    while (p != NULL)
    {
        cout << p->number << " -> ";
        p = p->next;
    }

    cout << "NULL\n";
}

int main()
{
    int choice;

    do
    {
        cout << "\n===== SMART PARKING MANAGEMENT SYSTEM =====\n";
        cout << "1. Add Vehicle\n";
        cout << "2. Delete Vehicle\n";
        cout << "3. Search Vehicle\n";
        cout << "4. Display Vehicles\n";
        cout << "5. Exit\n";

        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice)
        {
        case 1:
            addVehicle();
            break;

        case 2:
            deleteVehicle();
            break;

        case 3:
            searchVehicle();
            break;

        case 4:
            displayVehicles();
            break;

        case 5:
            cout << "Exiting program...\n";
            break;

        default:
            cout << "Invalid choice.\n";
        }

    } while (choice != 5);

    return 0;
}

8.Output
<img width="1600" height="842" alt="WhatsApp Image 2026-10-05 at 5 53 29 PM" src="https://github.com/user-attachments/assets/be8d1c53-77d0-43d9-8ab1-fe6fd9c09789" />
8. Concepts Used
Singly Linked List
Structures
Dynamic Memory Allocation
Pointers
Insertion
Deletion
Searching
Traversal
Functions
Conditional Statements
Loops
9. Programming Language

C++

10. Conclusion

The Smart Parking Management System successfully manages vehicle records using a singly linked list. It allows vehicles to be added, deleted, searched, and displayed efficiently. This project demonstrates the practical application of linked-list operations in a real-world system.

 
If choice is Display, traverse and display all vehicles.
Repeat the menu until the user selects Exit.
Stop.
