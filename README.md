# Airbnb Clone Project

## 🏠 Overview
This project is a simplified clone of the Airbnb platform, built as part of the ALX Software Engineering program. It aims to demonstrate core full-stack development skills including front-end design, back-end logic, data modeling, and version control.

## 🎯 Project Goals
- Recreate the basic functionality of Airbnb’s web application
- Apply object-oriented programming principles
- Implement persistent storage using file and database backends
- Build web interfaces using HTML/CSS and Flask
- Practice collaborative software development with Git and GitHub

## 🛠️ Tech Stack
- **Languages**: Python, HTML, CSS, JavaScript
- **Frameworks**: Flask (for web), unittest (for testing)
- **Database**: MySQL
- **Version Control**: Git, GitHub
- **Tools**: VS Code, Linux, Pep8

## 📂 Directory Structure (Coming Soon)
The repo will include modules for the console, models, views, and static assets.

---

✅ Initial commit complete. Future updates will include implementation and documentation.

| Role                             | Description & Responsibilities                                                                                                                                                      |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Backend Developer**            | Responsible for building the core application logic, APIs, and server-side integration. Implements models, views, and handles business logic in Python using frameworks like Flask. |
| **Frontend Developer**           | Designs and implements the user interface using HTML, CSS, and JavaScript. Ensures responsive, intuitive, and user-friendly designs aligned with Airbnb’s style.                    |
| **Database Administrator (DBA)** | Manages the project's data schema and ensures data integrity. Sets up MySQL databases, writes optimized queries, and configures data storage solutions.                             |
| **DevOps Engineer**              | Sets up and manages the deployment pipeline, ensures CI/CD integration, handles containerization (e.g., Docker), and manages server environments.                                   |
| **Project Manager**              | Coordinates tasks across the team, sets timelines, ensures milestone tracking, and communicates progress. Keeps the project aligned with its goals.                                 |
| **QA/Test Engineer**             | Develops unit tests and automated testing scripts to ensure features work as expected. Tracks bugs and ensures quality across releases.                                             |
| **UI/UX Designer**               | Focuses on user flows, visual design, and interaction models. Delivers mockups/wireframes to guide frontend development.                                                            |


## Technology Stack Overview
| Technology     | Purpose in the Project                                                                                           |
| -------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Python**     | Primary programming language used for developing backend logic, data models, and the console application.        |
| **Flask**      | A lightweight web framework for building RESTful APIs and rendering HTML templates for the web interface.        |
| **MySQL**      | Relational database system used to store user data, listings, bookings, and reviews.                             |
| **SQLAlchemy** | ORM (Object Relational Mapper) used to interact with the MySQL database using Python classes.                    |
| **HTML/CSS**   | Used to build and style the static frontend pages of the Airbnb clone.                                           |
| **JavaScript** | Adds interactivity to the frontend, such as dynamic filters, pop-ups, and form validation.                       |
| **Git**        | Version control system for tracking changes and enabling collaboration among developers.                         |
| **GitHub**     | Online repository hosting service where the project is managed, including code collaboration and issue tracking. |
| **Unittest**   | Python’s built-in testing framework used to write unit tests and ensure code correctness.                        |



## 🗃️ Database Design
The project database is designed using a relational structure, with tables representing real-world entities such as users, properties, and bookings. Below is an overview of the core entities and their relationships.

Entities and Key Fields
Users

id: Unique identifier

name: Full name of the user

email: Unique email address

password: Encrypted user password

role: User role (guest or host)

Properties

id: Unique property identifier

user_id: Foreign key referencing the property owner

title: Title or name of the property

description: Detailed description of the property

location: Address or general location

Bookings

id: Unique booking identifier

user_id: Foreign key referencing the guest

property_id: Foreign key referencing the booked property

check_in: Date of check-in

check_out: Date of check-out

Reviews

id: Unique review identifier

user_id: Reviewer (guest) ID

property_id: Reviewed property ID

rating: Numerical rating (1–5)

comment: Review text

Payments

id: Unique payment ID

booking_id: Foreign key referencing the booking

amount: Payment amount

status: Payment status (e.g., pending, paid)

payment_date: Date of payment

Entity Relationships
A User can own multiple Properties (1-to-many)

A User can make multiple Bookings (1-to-many)

A Booking is associated with one Property and one User (many-to-1)

A Property can have multiple Reviews (1-to-many)

A Booking is linked to one Payment (1-to-1)


## 🧩 Feature Breakdown
The Airbnb Clone project replicates key functionalities of the Airbnb platform. Below is a list of core features that form the backbone of the system:

1. User Management
Allows users to sign up, log in, and manage their profiles. Users can be guests or hosts, each with role-specific permissions and dashboards.

2. Property Management
Enables hosts to list new properties, update details (such as title, description, location, price), and upload images. Each property is linked to the host’s account and viewable by guests.

3. Booking System
Facilitates reservation of properties by guests. It manages availability checks, date selections, and links bookings to users and properties.

4. Payment Integration
Handles payment processing for confirmed bookings. Ensures secure transactions, generates receipts, and tracks payment statuses for both hosts and guests.

5. Review & Rating System
Lets guests leave reviews and rate properties after completing their stay. Helps other users make informed booking decisions based on previous experiences.

6. Search and Filter Functionality
Users can search for properties by location, date, price range, and property type. This improves the user experience and makes property discovery seamless.

7. Admin Dashboard (Optional)
An interface for system administrators to manage users, oversee listings, resolve disputes, and monitor platform activity.
