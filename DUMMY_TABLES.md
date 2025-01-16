# Database Dummy Entries

## Owners Table
| id  | phone_number | full_name    | id_card_photo                        | selfie                                 | created_at          | updated_at          |
| --- | ------------ | ------------ | ------------------------------------ | -------------------------------------- | ------------------- | ------------------- |
| 1   | 1234567890   | John Doe     | /owner/John/id/john_id.jpg           | /owner/John/selfie/john_selfie.jpg     | 2025-01-01 10:00:00 | 2025-01-01 10:00:00 |
| 2   | 2345678901   | Jane Smith   | /owner/Jane/id/jane_id.jpg           | /owner/Jane/selfie/jane_selfie.jpg     | 2025-01-02 10:00:00 | 2025-01-02 10:00:00 |
| 3   | 3456789012   | Bob Johnson  | /owner/Bob/id/bob_id.jpg             | /owner/Bob/selfie/bob_selfie.jpg       | 2025-01-03 10:00:00 | 2025-01-03 10:00:00 |
| 4   | 4567890123   | Alice Brown  | /owner/Alice/id/alice_id.jpg         | /owner/Alice/selfie/alice_selfie.jpg   | 2025-01-04 10:00:00 | 2025-01-04 10:00:00 |
| 5   | 5678901234   | Tom White    | /owner/Tom/id/tom_id.jpg             | /owner/Tom/selfie/tom_selfie.jpg       | 2025-01-05 10:00:00 | 2025-01-05 10:00:00 |
| 6   | 6789012345   | Lisa Green   | /owner/Lisa/id/lisa_id.jpg           | /owner/Lisa/selfie/lisa_selfie.jpg     | 2025-01-06 10:00:00 | 2025-01-06 10:00:00 |
| 7   | 7890123456   | Peter Black  | /owner/Peter/id/peter_id.jpg         | /owner/Peter/selfie/peter_selfie.jpg   | 2025-01-07 10:00:00 | 2025-01-07 10:00:00 |
| 8   | 8901234567   | Mary King    | /owner/Mary/id/mary_id.jpg           | /owner/Mary/selfie/mary_selfie.jpg     | 2025-01-08 10:00:00 | 2025-01-08 10:00:00 |
| 9   | 9012345678   | Mark Knight  | /owner/Mark/id/mark_id.jpg           | /owner/Mark/selfie/mark_selfie.jpg     | 2025-01-09 10:00:00 | 2025-01-09 10:00:00 |
| 10  | 0123456789   | Eva Queen    | /owner/Eva/id/eva_id.jpg             | /owner/Eva/selfie/eva_selfie.jpg       | 2025-01-10 10:00:00 | 2025-01-10 10:00:00 |

## Tenants Table
| id  | phone_number | full_name    | id_card_photo                          | selfie                                 | created_at          | updated_at          |
| --- | ------------ | ------------ | -------------------------------------- | -------------------------------------- | ------------------- | ------------------- |
| 1   | 2234567890   | Carl Cooper  | /tenant/Carl/id/carl_id.jpg            | /tenant/Carl/selfie/carl_selfie.jpg    | 2025-01-01 10:00:00 | 2025-01-01 10:00:00 |
| 2   | 3345678901   | Anna Bell    | /tenant/Anna/id/anna_id.jpg            | /tenant/Anna/selfie/anna_selfie.jpg    | 2025-01-02 10:00:00 | 2025-01-02 10:00:00 |
| 3   | 4456789012   | Sam Hill     | /tenant/Sam/id/sam_id.jpg              | /tenant/Sam/selfie/sam_selfie.jpg      | 2025-01-03 10:00:00 | 2025-01-03 10:00:00 |
| 4   | 5567890123   | Linda Fox    | /tenant/Linda/id/linda_id.jpg          | /tenant/Linda/selfie/linda_selfie.jpg  | 2025-01-04 10:00:00 | 2025-01-04 10:00:00 |
| 5   | 6678901234   | Mike Wolf    | /tenant/Mike/id/mike_id.jpg            | /tenant/Mike/selfie/mike_selfie.jpg    | 2025-01-05 10:00:00 | 2025-01-05 10:00:00 |
| 6   | 7789012345   | Nancy Bear   | /tenant/Nancy/id/nancy_id.jpg          | /tenant/Nancy/selfie/nancy_selfie.jpg  | 2025-01-06 10:00:00 | 2025-01-06 10:00:00 |
| 7   | 8890123456   | Kevin Fox    | /tenant/Kevin/id/kevin_id.jpg          | /tenant/Kevin/selfie/kevin_selfie.jpg  | 2025-01-07 10:00:00 | 2025-01-07 10:00:00 |
| 8   | 9901234567   | Laura Hart   | /tenant/Laura/id/laura_id.jpg          | /tenant/Laura/selfie/laura_selfie.jpg  | 2025-01-08 10:00:00 | 2025-01-08 10:00:00 |
| 9   | 1012345678   | Gary Ray     | /tenant/Gary/id/gary_id.jpg            | /tenant/Gary/selfie/gary_selfie.jpg    | 2025-01-09 10:00:00 | 2025-01-09 10:00:00 |
| 10  | 1123456789   | Rachel Moon  | /tenant/Rachel/id/rachel_id.jpg        | /tenant/Rachel/selfie/rachel_selfie.jpg | 2025-01-10 10:00:00 | 2025-01-10 10:00:00 |

## Rooms Table
| id  | owner_id | name       | address        | pin_code | latitude   | longitude  | photo_folder_id | type     | monthly_rent | security_deposit | status  | created_at          | updated_at          |
| --- | -------- | ---------- | -------------- | -------- | ---------- | ---------- | --------------- | -------- | ------------ | ---------------- | ------- | ------------------- | ------------------- |
| 1   | 1        | Room1      | 123 Main St    | 123456   | 12.9716    | 77.5946    | /owner/John/room/room1 | student  | 8000         | 12000            | free    | 2025-01-01 10:00:00 | 2025-01-01 10:00:00 |
| 2   | 2        | Room2      | 234 Elm St     | 654321   | 28.7041    | 77.1025    | /owner/Jane/room/room2 | family   | 10000        | 15000            | rented  | 2025-01-02 10:00:00 | 2025-01-02 10:00:00 |
| 3   | 3        | Room3      | 345 Oak St     | 112233   | 19.0760    | 72.8777    | /owner/Bob/room/room3  | student  | 9000         | 14000            | free    | 2025-01-03 10:00:00 | 2025-01-03 10:00:00 |
| 4   | 4        | Room4      | 456 Pine St    | 221122   | 13.0827    | 80.2707    | /owner/Alice/room/room4 | family   | 9500         | 14500            | rented  | 2025-01-04 10:00:00 | 2025-01-04 10:00:00 |
| 5   | 5        | Room5      | 567 Birch St   | 334455   | 22.5726    | 88.3639    | /owner/Tom/room/room5  | student  | 8500         | 13000            | free    | 2025-01-05 10:00:00 | 2025-01-05 10:00:00 |
| 6   | 6        | Room6      | 678 Maple St   | 556677   | 17.3850    | 78.4867    | /owner/Lisa/room/room6 | family   | 11000        | 16000            | rented  | 2025-01-06 10:00:00 | 2025-01-06 10:00:00 |
| 7   | 7        | Room7      | 789 Cedar St   | 778899   | 23.2599    | 77.4126    | /owner/Peter/room/room7 | student  | 8700         | 13500            | free    | 2025-01-07 10:00:00 | 2025-01-07 10:00:00 |
| 8   | 8        | Room8      | 890 Walnut St  | 990011   | 21.1702    | 72.8311    | /owner/Mary/room/room8 | family   | 9200         | 13800            | rented  | 2025-01-08 10:00:00 | 2025-01-08 10:00:00 |
| 9   | 9        | Room9      | 901 Chestnut St | 101010  | 26.8467    | 80.9462    | /owner/Mark/room/room9 | student  | 7600         | 12200            | free    | 2025-01-09 10:00:00 | 2025-01-09 10:00:00 |
| 10  | 10       | Room10     | 102 Ash St     | 202020   | 30.7333    | 76.7794    | /owner/Eva/room/room10 | family   | 10700        | 15700            | rented  | 2025-01-10 10:00:00 | 2025-01-10 10:00:00 |
