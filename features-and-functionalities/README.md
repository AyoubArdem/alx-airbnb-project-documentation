
#  Entity Association for Airbnb Clone

This document outlines the core entities and their relationships within the Airbnb Clone backend system. It serves as the foundation for designing the database schema, API logic, and system interactions.



##  Objective

To identify and associate key entities involved in the Airbnb Clone platform, including users, properties, bookings, payments, and reviews. These associations guide the creation of ERD diagrams, use case flows, and backend models.


##  Key Entities

| Entity     | Description                                      |
|------------|--------------------------------------------------|
| User       | Represents guests and hosts and admin with login credentials and profile data |
| Property   | Listings created by hosts, including location, price, and availability |
| Booking    | Reservation records linking users to properties and dates |
| Payment    | Transactions associated with bookings            |
| Review     | Feedback left by users for properties   |
| Admin      | System-level user with moderation and management privileges |



##  Entity Relationships

- User  ↔ Booking: A user can make multiple bookings; each booking belongs to one user.
- User ↔ Review: A user can leave multiple reviews; each review is linked to one user.
- Host (User)  ↔  Property: A host can manage multiple properties; each property belongs to one host.
- Property  ↔  Booking: A property can be booked multiple times; each booking is for one property.
- Booking ↔  Payment: Each booking triggers one payment; each payment is linked to one booking.
- Property  ↔ Review: A property can have multiple reviews; each review is linked to one property.



##  Usage

This entity association supports:
- Backend model design (e.g., Django models)
- API endpoint planning
- Data validation and integrity rules


