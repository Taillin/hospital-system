# Hospital Management System

> A console-based Java application for managing hospital operations — patients, doctors, and appointments — built with core OOP principles.

## Features

- **Patient management** — Add patients, admit and discharge them
- **Doctor management** — Add doctors, assign and free them from appointments
- **Appointment tracking** — Create appointments linking patients and doctors
- **Interactive menu** — Console UI for real-time data entry and display
- **Input validation** — Setters validate age, names and other fields

## Tech Stack

- **Language:** Java
- **Paradigm:** Object-Oriented Programming (OOP)
- **I/O:** Java Scanner (console)

### Menu

```
=== HOSPITAL SYSTEM ===
1. Add Patient
2. View All Patients
3. Add Doctor
4. View All Doctors
0. Exit
```

## Project Structure

```
src/model/
├── Main.java          # Entry point + interactive menu
├── Patient.java       # Patient entity (admit/discharge logic)
├── Doctor.java        # Doctor entity (assign/free logic)
└── Appointment.java   # Links Patient and Doctor with a date
```

## Class Overview

### `Patient`
| Field | Type | Description |
|-------|------|-------------|
| id | int | Unique identifier |
| name | String | Patient's full name |
| age | int | Age (validated ≥ 0) |
| illness | String | Diagnosis |
| admitted | boolean | Hospital admission status |

**Methods:** `admitPatient()`, `dischargePatient()`

### `Doctor`
| Field | Type | Description |
|-------|------|-------------|
| id | int | Unique identifier |
| name | String | Doctor's name |
| specialization | String | Medical specialization |
| experienceYears | int | Years of experience |
| isFree | boolean | Availability status |

**Methods:** `assignPatient()`, `finishAppointment()`

### `Appointment`
| Field | Type | Description |
|-------|------|-------------|
| id | int | Unique identifier |
| patient | Patient | Associated patient |
| doctor | Doctor | Assigned doctor |
| date | String | Appointment date |
| completed | boolean | Completion status |

**Methods:** `startAppointment()`, `completedAppointment()`

## Key Learnings

- Encapsulation and input validation through setters
- Object relationships and composition (`Appointment` holds `Patient` + `Doctor`)
- Interactive console application design with `Scanner`
- Use of `ArrayList` for dynamic data storage

## Author

**Yermakov Ilya** — IT-2503
