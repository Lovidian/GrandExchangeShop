# Grand Exchange Shopping System

**C++17 | Object-Oriented Programming | Multithreading | Inventory Management**

## Project Overview

The Grand Exchange Shopping System is a console-based C++ application inspired by the Grand Exchange marketplace in *Old School RuneScape (OSRS)*. The project was developed to demonstrate fundamental and advanced programming concepts through a familiar gaming environment.

The application simulates an online marketplace where users can browse products, manage shopping carts, and complete purchases using simulated gold pieces (GP). Rather than creating a traditional e-commerce platform, I wanted to incorporate elements from a game I enjoy while exploring how real-world shopping systems manage inventory, customer accounts, and concurrent transactions.

## Key Features

**Product Catalog and Categories**

The marketplace contains 28 OSRS-inspired products organized into six categories: Weapons, Armor & Jewelry, Potions, Food, Resources, and Runes & Ammunition. Each product includes an ID, name, description, price, and available stock quantity.

Users can browse individual categories or view the entire catalog. The system also supports adding, updating, and removing products.

**Shopping Cart Management**

Users can add products to their shopping cart, remove unwanted items, and adjust quantities before purchasing. The application automatically calculates the total price and checks product availability during checkout.

**User Accounts and Membership Privileges**

The system supports three account types using inheritance and polymorphism:

- **Regular:** Standard pricing with no discounts.
- **Premium:** 5% discount on purchases.
- **VIP:** 10% discount on purchases.

All account types share common attributes, including a username, email address, shipping address, and shopping cart.

**Checkout and Inventory Management**

The checkout process asks users to confirm their purchase before completing a simulated transaction. Once confirmed, the application applies the appropriate membership discount, updates product quantities, and generates an order receipt.

No real financial transactions are performed.

## Multithreading and Concurrency

One of the most important features of this project is its multithreading demonstration.

In real-world shopping systems, multiple customers may attempt to purchase the same product simultaneously. Without proper synchronization, this could result in inventory discrepancies or overselling.

To demonstrate this challenge, the application simulates two users attempting to purchase limited-stock items concurrently.

I implemented `std::thread` to execute concurrent operations and `std::mutex` to protect shared inventory data. This ensures that inventory updates are synchronized and purchases cannot exceed available stock.

The demonstration highlights the importance of thread safety and maintaining data integrity in applications supporting concurrent users.

## Object-Oriented Design

The application separates responsibilities across several classes:

| Class | Responsibility |
|---|---|
| Product | Stores product information and inventory quantities |
| Catalog | Manages available products and stock |
| ShoppingCart | Handles selected products and totals |
| User | Provides shared account attributes and behavior |
| RegularUser | Implements standard membership privileges |
| PremiumUser | Implements premium discounts |
| VIPUser | Implements VIP discounts |

Encapsulation protects class attributes from unauthorized modification, while inheritance and polymorphism reduce duplicated code and support future expansion.

## Technologies Used

- C++17
- Microsoft Visual Studio
- Standard Template Library (STL)
- Object-Oriented Programming
- Multithreading with `std::thread`
- Synchronization with `std::mutex`
- Exception handling and input validation

## Installation and Usage

1. Clone or download this repository.
2. Open the C++ project in Microsoft Visual Studio.
3. Ensure the C++17 language standard is enabled.
4. Build and run the application.
5. Enter your account information and select a membership type.
6. Use the console menu to browse products, manage your cart, complete purchases, or test multithreading.

## Future Development

Although the current application provides a functional shopping experience, several features could be introduced in future versions:

- Player-to-player trading and buy/sell offers.
- Dynamic pricing influenced by supply and demand.
- Persistent user accounts and purchase histories.
- Database integration for inventory management.
- Graphical interface inspired by the actual Grand Exchange.

## Conclusion

This project allowed me to combine my interest in Old School RuneScape with practical C++ software development. It strengthened my understanding of object-oriented design, inheritance, encapsulation, error handling, and concurrency.

More importantly, it demonstrated how these concepts work together in a functional application rather than existing as isolated programming exercises.

The Grand Exchange Shopping System serves as a foundation for future development and demonstrates my ability to design, implement, and expand a structured C++ application.

---

*Disclaimer: This is an independent educational project inspired by Old School RuneScape. It is not affiliated with or endorsed by Jagex.*
