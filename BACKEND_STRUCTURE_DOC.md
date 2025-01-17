# rentkhojo System Documentation

## Overview

The Tenant and Owner Management System is designed to manage the information of tenants and owners. The system maintains a structured directory for storing room photos for owners

## Directory Structure

### Primary Folders
- `tenant/`
- `owner/`

### Owner Folder Structure
Each owner's folder is named after their firstname_phone. Inside each owner's folder, there are three subfolders:
- `room/`: Contains subfolders for each room managed by the owner, which further contain room photos.

Example:
```
owner/John_1234567890/
│
└── room/
    ├── room1/
    │   ├── room1_photo1.jpg
    │   └── room1_photo2.jpg
    └── room2/
        ├── room2_photo1.jpg
        └── room2_photo2.jpg
```

## Database Tables

### Owners Table
This table stores information about the owners.

| Column            | Type    | Description                                   |
|-------------------|---------|-----------------------------------------------|
| id                | INT     | Unique identifier for the owner.              |
| phone_number      | STRING  | Phone number of the owner.                    |
| firstname         | STRING  | First name of the owner.                      |
| lastname          | STRING  | Last name of the owner.                       |
| PIN               | STRING  | Login PIN                                     |
| created_at        | DATE    | Date when the record was created.             |

### Tenants Table
This table stores information about the tenants.

| Column            | Type    | Description                                   |
|-------------------|---------|-----------------------------------------------|
| id                | INT     | Unique identifier for the tenat.              |
| phone_number      | STRING  | Phone number of the tenat.                    |
| firstname         | STRING  | First name of the tenat.                      |
| lastname          | STRING  | Last name of the tenat.                       |
| PIN               | STRING  | Login PIN                                     |
| created_at        | DATE    | Date when the record was tenat.               |

### Rooms Table
This table stores information about the rooms managed by the owners.

| Column            | Type    | Description                                   |
|-------------------|---------|-----------------------------------------------|
| id                | INT     | Unique identifier for the room.               |
| owner_id          | INT     | Foreign key linking to the owner's ID.        |
| name              | STRING  | Name of the room.                             |
| address           | STRING  | Address of the room.                          |
| pin_code          | STRING  | Pin code of the room's location.              |
| latitude          | FLOAT   | Latitude coordinate of the room's location.   |
| longitude         | FLOAT   | Longitude coordinate of the room's location.  |
| photo_folder_id   | STRING  | Path to the room's photo folder.              |
| type              | STRING  | Type of room (e.g., student, family).         |
| monthly_rent      | FLOAT   | Monthly rent for the room.                    |
| security_deposit  | FLOAT   | Security deposit amount for the room.         |
| status            | STRING  | Status of the room (e.g., free, rented).      |
| created_at        | DATETIME| Timestamp when the record was created.        |
| updated_at        | DATETIME| Timestamp when the record was last updated.   |

## Usage

The system is designed to efficiently manage and retrieve information about tenants, owners, and their associated photos. By following the structured directory and database design, users can ensure easy access and organization of data.

For each new tenant or owner added to the system, their respective directories and database entries should be updated accordingly to maintain consistency.

