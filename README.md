# DiviStay - Hotel Group Booking & Payment Splitting System 🏨💳

> **Note:** This repository showcases the **Software Architecture, System Design, and Requirements Engineering** of the DiviStay platform. It focuses on Object-Oriented Design (OOD), UML modeling, and applied Design Patterns.

## 📌 Project Overview
DiviStay is an interactive hotel booking system designed to simplify group reservations. It solves the common problem where a single group organizer assumes all financial risk by booking rooms. Instead, DiviStay provides an advanced payment-splitting mechanism, allowing each group member to pay their share independently via secure, personalized links. 

The system handles complex real-time business logic, including a 30-minute room-locking timer to prevent overbooking, automated transaction synchronization with external payment gateways, and automated cancellations if the funding goal is not met.

## ✨ Key Features Handled in the Design
* **Smart Payment Splitting:** Supports equal split, room-based proportional split, and custom manual split.
* **Concurrency & Overbooking Prevention:** A strict 30-minute room lock mechanism (TTL) upon group creation.
* **Automated Lifecycle Management:** Background system processes for final reservation confirmation with the hotel PMS or automated group cancellation and payment voids.
* **Role Flexibility:** A dynamic user model where a user can seamlessly act as an organizer in one group and a regular member in another.

## 🏗️ Architecture & System Design
The system is designed using a layered architecture (MVC) with a strong emphasis on clean, scalable, and maintainable Object-Oriented principles.

### Applied Design Patterns
1. **Strategy Pattern:** Implemented to handle the flexible payment splitting logic (`EqualSplitStrategy`, `RoomBasedSplitStrategy`, `CustomSplitStrategy`). This isolates the complex calculation logic from the `BookingGroup` class.
2. **Adapter Pattern:** Used to integrate external payment gateways (`PaymentGatewayAdapter`), ensuring the core domain remains decoupled from third-party APIs.
3. **Factory Method:** Utilized for instantiating diverse room types (`RoomFactory`) and the correct payment split strategies (`SplitStrategyFactory`).

### UML Diagrams
The architectural design is fully documented using UML diagrams. *(You can view the full architecture document in the `docs` folder).*

**1. Class Diagram (Domain Model)**
The architectural design is fully documented using UML diagrams. *(You can view the full architecture document linked in the Documentation section below).*
![Class Diagram](Software_Architecture_Document.pdf)

**2. Sequence Diagram - Payment Processing**
*Demonstrates the exact message flow between the Client App, DiviStay Server, Database, and the External Payment Gateway.*
![Sequence Diagram](Software_Architecture_Document.pdf)

**3. Activity Diagram - Group Creation & Room Locking**
*Maps the system's decision-making process when locking rooms and handling edge cases like unavailable inventory.*
![Activity Diagram](Software_Architecture_Document.pdf)

## 🛠️ Skills & Concepts Showcased
* **System Architecture & Design**
* **Software Requirements Specification (SRS)**
* **Object-Oriented Design (OOD) & Design Patterns**
* **UML Modeling (Use Case, Activity, Sequence, Class Diagrams)**
* **Edge-case Analysis & Concurrency Planning**

## 📄 Documentation
You can find the comprehensive project documents in this repository:
* [Software Requirements Specification (SRS)](Software_Requirements_Specification.pdf)
* [Software Architecture Document (SAD)](Software_Architecture_Document.pdf)

---
*This project was designed as part of a Software Engineering course by Noya, Amit, and Amir.*
