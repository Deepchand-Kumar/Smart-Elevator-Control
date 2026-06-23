This is DB Design for builds intelligent elevator control platforms for large commercial buildings across India.
This backend system manages multi-building elevator operations, ensuring safe, efficient, and reliable movement for thousands of passengers daily.

The platform supports:

Multiple buildings and zones

Floor-level request tracking

Intelligent ride allocation

Elevator status monitoring

Maintenance tracking

Usage history logging

System Architecture
The platform is designed to handle real-time elevator requests across complex infrastructures like corporate towers, malls, airports, hospitals, and residential complexes.

Key Features
Multi-building support – Manage elevators across multiple sites.

Floor management – Track requests and assignments per floor.

Elevator allocation – Assign requests dynamically to available elevators.

Status monitoring – Idle, moving, maintenance, or disabled.

Maintenance tracking – Record service history without overwriting logs.

Ride logging – Store trip data for analytics and performance insights.

Entity-Relationship (ER) Design
Core Entities
Building – Contains multiple floors and elevator shafts.

Floor – Belongs to a building, generates requests.

ElevatorShaft – Physical shaft housing one elevator.

Elevator – Operates within a shaft, serves multiple floors.

Operational Entities
FloorRequest – User-generated request from a floor.

RideAssignment – Links a request to an elevator.

RideLog – Records completed trips for analytics.

MaintenanceRecord – Tracks service and downtime history.

Relationships
One Building → Floors (1:N)

One Building → ElevatorShafts → Elevators (1:1 per shaft)

Elevator ↔ Floor (M:N via ElevatorFloorMap)

Floor → FloorRequest (1:N)

FloorRequest → RideAssignment → Elevator (1:1 mapping)

Elevator → RideLogs (1:N)

Elevator → MaintenanceRecords (1:N)


