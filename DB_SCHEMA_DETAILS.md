# Database Schema Details

## Owners Table
- **id**: A unique identifier for each owner (auto-incremented).
- **phone_number**: The phone number of the owner (unique and required).
- **full_name**: The full name of the owner.
- **id_card_photo**: The file path or URL to the owner's ID card photo.
- **selfie**: The file path or URL to the owner's selfie.
- **created_at**: The timestamp when the owner record was created.
- **updated_at**: The timestamp when the owner record was last updated.

## Tenants Table
- **id**: A unique identifier for each tenant (auto-incremented).
- **phone_number**: The phone number of the tenant (unique and required).
- **full_name**: The full name of the tenant.
- **id_card_photo**: The file path or URL to the tenant's ID card photo.
- **selfie**: The file path or URL to the tenant's selfie.
- **created_at**: The timestamp when the tenant record was created.
- **updated_at**: The timestamp when the tenant record was last updated.

## Rooms Table
- **id**: A unique identifier for each room (auto-incremented).
- **owner_id**: The ID of the owner (foreign key referencing `owners(id)`).
- **name**: A unique name for the room entry (required).
- **address**: The address of the room (required).
- **pin_code**: The postal code of the room's location (required).
- **latitude**: The latitude coordinate of the room's location.
- **longitude**: The longitude coordinate of the room's location.
- **photo_folder_id**: The unique ID for the folder containing the room's photos.
- **type**: The type of room (ENUM: 'student', 'family').
- **monthly_rent**: The monthly rent for the room.
- **security_deposit**: The security deposit for the room.
- **status**: The rental status of the room (ENUM: 'rented', 'free').
- **created_at**: The timestamp when the room record was created.
- **updated_at**: The timestamp when the room record was last updated.
