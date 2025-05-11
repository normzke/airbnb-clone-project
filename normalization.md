# Database Normalization to 3NF

This document outlines how the Airbnb Clone project database schema was normalized to the Third Normal Form (3NF).

## First Normal Form (1NF)
- Ensured all attributes are atomic (no repeating groups or arrays).
- Example: Separated `location` into `address`, `city`, `state`, and `zip_code`.

## Second Normal Form (2NF)
- Removed partial dependencies by ensuring non-key attributes depend on the whole primary key.
- Example: In `Booking`, `total_price` depends on both `property_id` and `date range`, so it was retained.

## Third Normal Form (3NF)
- Removed transitive dependencies (non-key attributes depending on other non-key attributes).
- Example:
  - Originally, `User` table had `user_id`, `name`, `email`, and `property_count`.
  - `property_count` depends on the number of related rows in `Property`, not directly on `user_id`, so it was removed and can be computed as needed.

## Final Tables in 3NF

### User
- id (PK)
- name
- email
- password
- created_at

### Property
- id (PK)
- user_id (FK to User)
- title
- description
- location
- price_per_night

### Booking
- id (PK)
- user_id (FK to User)
- property_id (FK to Property)
- start_date
- end_date
- total_price

### Payment
- id (PK)
- booking_id (FK to Booking)
- amount
- status
- method

### Review
- id (PK)
- booking_id (FK to Booking)
- rating
- comment
- created_at

All tables now conform to 3NF with minimal redundancy and clear, normalized relationships.
