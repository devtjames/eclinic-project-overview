# System Architecture

This document explains the structure of the eClinic system and how the main components interact.

---

## Overview

eClinic follows a simple web application structure built with PHP and MySQL.

The system is divided into three major parts:

- Frontend (User Interface)
- Backend (Application Logic)
- Database (Data Storage)

Users interact with the frontend, which sends requests to the backend.  
The backend processes the request and communicates with the database.

---

## Application Structure


Each module handles a specific responsibility in the system.

---

## User Roles

The system supports three roles.

### Admin
Responsible for managing the entire platform.

Capabilities:

- Manage doctors
- Manage patients
- View all appointments
- Monitor consultations

### Doctor

Capabilities:

- View assigned appointments
- Conduct consultations
- Create prescriptions
- View consultation history

### Patient

Capabilities:

- Register and login
- Book appointments
- View consultation history
- View and print prescriptions

---

## Database Design

The database stores users, appointments, consultations, and prescriptions.

### users

Stores all system users.

| Field | Description |
|------|-------------|
| id | Primary key |
| fullname | User full name |
| email | Login email |
| password | Hashed password |
| role | admin / doctor / patient |
| specialty | Doctor specialty (if role is doctor) |
| phone | Contact number |
| created_at | Account creation time |

---

Stores appointment bookings.

| Field | Description |
|------|-------------|
| id | Primary key |
| patient_id | Patient user ID |
| doctor_id | Doctor user ID |
| appointment_date | Scheduled date |
| start_time | Start time |
| status | pending / confirmed / completed / cancelled |
| created_at | Booking timestamp |

---

### consultations

Stores consultation sessions.

| Field | Description |
|------|-------------|
| id | Primary key |
| appointment_id | Related appointment |
| doctor_notes | Consultation notes |
| created_at | Consultation time |

---

### prescriptions

Stores prescriptions created by doctors.

| Field | Description |
|------|-------------|
| id | Primary key |
| consultation_id | Related consultation |
| medication | Prescribed medication |
| dosage | Dosage instructions |
| notes | Additional notes |
| created_at | Prescription date |

---

## Security Approach

Basic security measures include:

- Password hashing
- Role based access control
- Session authentication
- Input validation
