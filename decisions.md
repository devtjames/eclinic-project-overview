# Technical Decisions

This document explains some of the choices made during the development of eClinic.

---

## PHP for Backend

PHP was chosen because:

- It is widely supported by hosting providers
- It works well with MySQL
- It allows rapid development of server side logic

The system uses plain PHP with structured modules to keep the code simple and readable.

---

## MySQL Database

MySQL was used as the database because:

- It integrates easily with PHP
- It handles relational data well
- It is reliable for transactional systems

---

## TailwindCSS for UI

TailwindCSS was used to design the interface.

Reasons:

- Fast UI development
- Responsive design support
- Clean and consistent styling

---

## Role Based Access Control

The system uses role based permissions.

Roles include:

- Admin
- Doctor
- Patient

Each role only has access to the features required for their tasks.

This reduces security risks and keeps the interface simple.

---

## Digital Prescription System

Prescriptions are stored digitally and can be printed.

This approach allows:

- Easy patient access
- Record keeping
- Faster consultations

---

## Calendar Dashboard

A calendar view was added to the dashboard to help users visualize appointments.

Benefits include:

- Better schedule awareness
- Clear appointment overview
- Easier planning for doctors
