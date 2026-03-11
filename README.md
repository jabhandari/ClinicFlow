# Clinic Management System

A small command-line application in C for managing patient records and clinic appointments.

## Why This Project Matters

This project is a compact example of writing structured, modular C code for a real-world workflow. It focuses on record management, input validation, scheduling logic, and file-based data import.

## What It Demonstrates

- Modular C design with separated headers and source files
- Use of `struct` types to model patients, phones, dates, times, and appointments
- Console-based menu flows for CRUD-style operations
- Input validation for numeric, character, string, phone, and date fields
- File I/O for importing persisted patient and appointment data
- Appointment sorting and schedule lookup by date

## Project Structure

- `clinic.c`: patient and appointment management logic
- `clinic.h`: shared data structures and function declarations
- `core.c`: reusable input, formatting, and date utilities
- `core.h`: shared utility declarations and constants

## Key Features

- View all patient records in table format
- Search patients by patient number or phone number
- Add, edit, and remove patient records
- View all appointments or appointments for a specific date
- Add and remove appointments with date and time validation
- Format phone numbers consistently for display

## Build Notes

This repository currently contains the application modules and helper functions. If you add or restore the program entry point (`main`), the project can be compiled with:

### GCC

```bash
gcc -Wall -Wextra -pedantic -std=c11 clinic.c core.c -o clinic
```

### MSVC

```powershell
cl /W4 /std:c11 clinic.c core.c /Fe:clinic.exe
```

## Future Improvements

- Add automated tests for validation and scheduling logic
- Replace fixed-size arrays with dynamic memory management
- Persist record updates back to data files
- Add a dedicated `main.c` driver with sample data files for easier setup
