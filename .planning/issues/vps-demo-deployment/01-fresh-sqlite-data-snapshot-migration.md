# Issue 01: Fresh SQLite Data Snapshot Migration
Status: done
Type: AFK

## What to build

Execute the data extraction migration pipeline from the live local MSSQL database into a clean, modern SQLite snapshot (`demo_data/attendance.db`). The snapshot must capture up-to-date **Employee**, **Shift Definition**, **Shift Rule**, **Attendance Log**, and **Meal Tracking** records, ensuring compatibility with current schema additions (including shift categories, supervisor privileges, and lunch break tracking fields).

## Acceptance criteria

- [x] Connection to the local MSSQL source databases (`MIS` and `NY_VDS_DB`) is established successfully.
- [x] Fresh SQLite database `demo_data/attendance.db` is initialized with all latest table schemas.
- [x] Core tables (`EmployeeLocalRegistry`, `ShiftDefinitions`, `ShiftRules`, `AttendanceLogs`, `EmployeeDailyShifts`, `EmployeeMetadata`, `MealTrackingHistory`, `HR_MEAL_ORDER`, `HR_MEAL_PICKUP_LOG`) are populated with real or sampled data.
- [x] Automated query verification confirms tables are readable and non-empty.

## Blocked by

None - can start immediately.
