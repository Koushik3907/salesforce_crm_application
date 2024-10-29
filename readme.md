# EduConsultPro: Salesforce CRM Solution for Educational Institutions  
*By Koushik*

## Overview

EduConsultPro is a specialized Salesforce CRM tailored for educational institutions, designed to simplify and unify the student lifecycle—from initial inquiry through enrollment and ongoing support. The platform manages courses, consultants, student information, appointments, and communications in one central location, enhancing efficiency and transparency.

## Demonstration

[![EduConsultPro Demo](http://img.youtube.com/vi/tdC1aOKQyfY/0.jpg)](https://youtu.be/l89XjMdGYac)

Explore EduConsultPro’s capabilities by watching the demonstration video above.

## Key Features

* **Student Admission Management**
  - End-to-end application and course registration process automation
  - Streamlined student data organization
  - Automated notifications for admissions, updates, and course registration

* **Appointment Scheduling**
  - Consultant booking with a built-in approval workflow
  - Calendar integration and email notifications for all scheduled appointments

* **Case Management**
  - Comprehensive immigration and visa application support
  - Student support ticketing to manage assistance requests

* **Course Management**
  - Detailed course catalog with registration tracking and enrollment management tools

## Technical Architecture

### Custom Objects

- **Student**
- **Course**
- **Consultant**
- **Appointment**
- **Registration**

### Object Relationships

- **Appointment → Student** (Lookup)
- **Appointment → Consultant** (Lookup)
- **Registration → Student** (Lookup)
- **Registration → Course** (Lookup)
- **Student → Case** (Lookup)

### Automation

* **Flows**
  - **Student Admission Flow**: Collects student details, manages course selection, registration, and sends notifications.
  - **Appointment Booking Flow**: Verifies student eligibility, checks consultant availability, schedules appointments, and initiates approval.
  - **Combined Master Flow**: Routes new or returning students seamlessly through the appropriate processes.

* **Approval Processes**: Manages appointment approvals, including automated routing to managers and email updates for each action taken.

* **Apex Triggers**
  - **StudentTrigger**: Creates a welcome case for each new student, guiding them through onboarding.
  - **AppointmentTrigger**: Confirms appointment scheduling within business hours (9 AM–5 PM), validates consultant availability, and sends email confirmations.

### User Interface

- **Lightning Components**
  - Custom "EduConsultPro" Lightning App
  - Optimized home page for user-friendly navigation
  - Streamlined tabs for quick access to essential functions

## Setup Instructions

1. **Object Creation**
   - Import `Course`, `Consultant`, and `Student` objects and data.
   - Establish necessary relationship fields between objects.

2. **User Configuration**
   - Create users with the "Standard Platform User" profile.
   - Configure user hierarchies for approval processes.

3. **Flow Deployment**
   - Deploy `Student Admission Flow`, `Appointment Booking Flow`, and `Combined Master Flow`.

4. **Lightning App Setup**
   - Deploy the `EduConsultPro` Lightning App.
   - Configure home page layouts and assign user permissions.

## Custom Settings

- **Case Object Configuration**
  - **Type Field Values**: `Immigration`, `Visa Application`
  - **Status Field Values**: `Open`, `In-Progress`, `Closed`

## Feature Details

### Student Admission Process

1. Students submit the admission form and select courses.
2. The system automatically creates a registration record and sends a confirmation email.
3. The student’s data is saved as a new Salesforce record.

### Appointment Management

1. System verifies student information and consultant availability.
2. Appointment is scheduled and submitted for manager approval.
3. Notifications are sent to the student and consultant at each step.

## System Requirements

- Salesforce Enterprise Edition or higher
- System Administrator profile for initial setup
- Standard Platform User licenses for end users

---

*Note: This README is part of an academic project by Koushik, showcasing a Salesforce CRM solution for educational institutions.*
