# rentkhojo System Documentation

## Overview

The Tenant and Owner Management System is designed to manage the information and photo records of tenants and owners. The system maintains a structured directory for storing photos of ID cards, selfies, and room photos for both tenants and owners. It also includes tables for storing detailed information about tenants, owners, and rooms.

## Directory Structure

### Primary Folders
- `tenant/`
- `owner/`

### Tenant Folder Structure
Each tenant's folder is named after their first name. Inside each tenant folder, there are two subfolders:
- `id/`: Contains ID card photos.
- `selfie/`: Contains selfie photos.

Example:
```
tenant/Carl/├── id/
│   └── carl_id.jpg
└── selfie/
    └── carl_selfie.jpg
```

### Owner Folder Structure
Each owner's folder is named after their first name. Inside each owner's folder, there are three subfolders:
- `id/`: Contains ID card photos.
- `selfie/`: Contains selfie photos.
- `room/`: Contains subfolders for each room managed by the owner, which further contain room photos.

Example:
```
owner/John/├── id/
│   └── john_id.jpg
├── selfie/
│   └── john_selfie.jpg
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
| full_name         | STRING  | Full name of the owner.                       |
| id_card_photo     | STRING  | Path to the owner's ID card photo.            |
| selfie            | STRING  | Path to the owner's selfie photo.             |
| created_at        | DATETIME| Timestamp when the record was created.        |
| updated_at        | DATETIME| Timestamp when the record was last updated.   |

### Tenants Table
This table stores information about the tenants.

| Column            | Type    | Description                                   |
|-------------------|---------|-----------------------------------------------|
| id                | INT     | Unique identifier for the tenant.             |
| phone_number      | STRING  | Phone number of the tenant.                   |
| full_name         | STRING  | Full name of the tenant.                      |
| id_card_photo     | STRING  | Path to the tenant's ID card photo.           |
| selfie            | STRING  | Path to the tenant's selfie photo.            |
| created_at        | DATETIME| Timestamp when the record was created.        |
| updated_at        | DATETIME| Timestamp when the record was last updated.   |

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

