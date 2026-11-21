# Industrial Manufacturing & Production Control System

## Overview
The Industrial Manufacturing & Production Control System is a console-based manufacturing management application written in C. The system simulates factory operations including raw material inventory, finished product management, production processes, and production cost analytics.

It also includes authentication, activity logging, and file-based storage to maintain manufacturing records.

## Features

### Authentication System
- Admin login with username and password
- Passwords stored as djb2 hashes (a simple teaching hash, not secure for real credentials)
- Automatic administrator initialization

### Raw Material Management
- Add raw materials
- View raw material inventory
- Track quantity and cost per unit
- Automatic reorder alerts when stock falls below reorder level

### Finished Product Management
- Add finished products
- Track produced quantities
- Maintain product production cost records

### Production Process
- Consume raw materials during production
- Increase finished product quantity after manufacturing
- Record production transactions with timestamps
- Calculate production costs

### Production Analytics
The system analyzes production records and provides statistical insights including:

- Total production records
- Average production cost
- Variance
- Standard deviation

### Activity Logging
All system activities are logged including:

- Admin login
- Raw material additions
- Product creation
- Production execution
- Analytics generation
- System exit

## Technologies Used
- C Programming Language
- Standard C Libraries
- File-based persistent storage

## System Data Files

| File | Purpose |
|-----|-----|
| manufacturing_users.dat | User authentication records |
| raw_materials.dat | Raw material inventory |
| finished_products.dat | Finished product records |
| production_records.dat | Production transaction records |
| manufacturing_logs.txt | System activity logs |

## Build and Run

Needs a C compiler (gcc or clang).

```bash
gcc manufacturing_system.c -o manufacturing_system -lm
./manufacturing_system
```

On macOS, `-lm` is optional. The program creates its `.dat` data files and log file on first run.

## Project Report

Design and feature walkthrough: [docs/IMPCS-project-report.pdf](docs/IMPCS-project-report.pdf)

## Default Admin Login

Created automatically on first run.

Username: admin  
Password: admin123

## Program Menu

1. Add Raw Material  
2. View Raw Materials  
3. Add Finished Product  
4. Produce  
5. Production Analytics  
6. Exit  

## Learning Objectives

This project demonstrates:

- Manufacturing system simulation
- File handling in C
- Inventory management
- Production workflow management
- Cost analysis
- Statistical analytics
- Console-based industrial management applications

## Author
Jisan
