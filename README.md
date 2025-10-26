CS-320 Project Two — Unit Testing for Contact, Task, and Appointment Services

Author: Mubasil Choudhry
Course: Southern New Hampshire University — CS-320: Software Testing
Date: October 19, 2025

📋 Project Overview

This project focuses on developing and testing three independent service classes — ContactService, TaskService, and AppointmentService — using JUnit 5.
Each service manages corresponding model objects (Contact, Task, and Appointment) and enforces strict input validation rules aligned with customer requirements.
The goal of the project was to ensure that all functionality worked correctly and that invalid data could not be introduced into the system.

🧪 Testing Objectives

The primary objective was to use unit testing to verify that each service and class adhered to the functional and data validation requirements.
Testing was conducted using JUnit 5 and emphasized the following principles:

Validation testing for field constraints (string lengths, null checks, and format enforcement)

Boundary testing for maximum/minimum character limits

Exception testing to confirm that invalid inputs triggered appropriate errors

Service-level testing to confirm CRUD functionality (Create, Read, Update, Delete)

Duplicate prevention testing for unique IDs across services

🧩 Components Tested
1. Contact Service

Fields Tested: Contact ID, First Name, Last Name, Phone Number, and Address

Constraints Enforced:

ID must be unique, non-null, and ≤10 characters

Names must be non-null and ≤10 characters

Phone number must be exactly 10 digits

Address must be non-null and ≤30 characters

JUnit Classes: ContactTest, ContactServiceTest

2. Task Service

Fields Tested: Task ID, Name, Description

Constraints Enforced:

ID must be non-null, ≤10 characters, and immutable

Name must be non-null and ≤20 characters

Description must be non-null and ≤50 characters

JUnit Classes: TaskTest, TaskServiceTest

3. Appointment Service

Fields Tested: Appointment ID, Date, Description

Constraints Enforced:

Date must not be null or in the past

ID must be unique, non-null, and ≤10 characters

Description must be ≤50 characters

JUnit Classes: AppointmentTest, AppointmentServiceTest

🧠 Testing Approach
Methodology

Unit Testing: Verified isolated methods for correctness

Boundary Testing: Checked edge cases for string length and input validation

Exception Testing: Used assertThrows() to validate error handling for invalid inputs

Example
assertThrows(IllegalArgumentException.class, () -> contact.setPhone("12345"));


This ensures that invalid phone numbers are properly rejected.

✅ Key Achievements

Achieved 80%+ test coverage across all classes

Fully validated happy-path and failure scenarios

Identified edge cases early in development

Developed helper methods (e.g., futureDate()) for efficient and consistent test data generation

💡 Reflection

This project reinforced the importance of parallel testing and development.
By writing tests alongside the code, defects and logical gaps were discovered early, improving reliability and maintainability.
Adopting a black-box testing mindset helped ensure objectivity when validating my own code.
The experience emphasized the long-term benefits of disciplined testing practices in reducing technical debt and maintaining code quality.

🧱 Technologies Used

Java 17

JUnit 5

Eclipse IDE / IntelliJ IDEA

Git & GitHub for version control

📚 References

García, B. (2022). JUnit 5: Basics and best practices. Springer.

Myers, G. J., Sandler, C., & Badgett, T. (2011). The Art of Software Testing (3rd ed.). Wiley.

IEEE. (2017). IEEE Standard for Software and System Test Documentation (IEEE 829-2017). IEEE Computer Society.
