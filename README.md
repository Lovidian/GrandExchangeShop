# Grand Exchange Shopping System

### C++17 | Object-Oriented Programming | Multithreading

A console-based shopping application inspired by the Grand Exchange in **Old School RuneScape (OSRS)**.

This project was developed to demonstrate object-oriented programming, inheritance, polymorphism, inventory management, multithreading, and error handling using C++.

## Features

- **Product Catalog:** Browse 28 OSRS-inspired items organized into six categories.
- **Shopping Cart:** Add products, remove items, update quantities, and calculate totals.
- **Membership System:** Regular, Premium, and VIP users with different discount privileges.
- **Simulated Checkout:** Confirm purchases, calculate discounts, and generate order receipts.
- **Inventory Management:** Track stock quantities and update product availability.
- **Multithreading:** Simulate multiple customers attempting to purchase limited-stock items simultaneously.
- **Error Handling:** Validate user inputs and prevent invalid purchases.

## Technologies Used

- C++17
- Microsoft Visual Studio
- Standard Template Library (STL)
- `std::thread`
- `std::mutex`
- Object-Oriented Programming (OOP)

## Object-Oriented Design

The application uses multiple classes to separate responsibilities:

| Class | Purpose |
|---|---|
| Product | Stores item information and stock quantities |
| Catalog | Manages available products |
| ShoppingCart | Handles customer selections |
| User | Base class for customer accounts |
| RegularUser | Standard customer privileges |
| PremiumUser | 5% purchase discount |
| VIPUser | 10% purchase discount |

## Multithreading and Concurrency

The application demonstrates how multiple customers may attempt to purchase the same product simultaneously.

Using threads and mutex-based synchronization, the program prevents conflicting inventory updates and ensures that purchases cannot exceed available stock.

## Running the Project

1. Download or clone the repository.
2. Open the project in Visual Studio with the Desktop development with C++ workload installed.
3. Ensure the project uses C++17.
4. Build and run the application.
5. Follow the console prompts to browse products, manage your cart, or test concurrent purchases.

## Screenshots

*Screenshots of the application will be added here.*

## Future Improvements

- Introduce player-to-player trading.
- Implement dynamic Grand Exchange pricing.
- Save purchase histories.
- Add persistent inventory storage.
- Develop a graphical user interface.

## Project Purpose

This project combines my interest in Old School RuneScape with the practical application of C++ programming concepts. It demonstrates how object-oriented design and concurrency control can be used to build a simplified online shopping system.

*This is an educational project inspired by OSRS and is not affiliated with Jagex.*
