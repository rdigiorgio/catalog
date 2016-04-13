# PostgreSQL

This stack creates a PostgreSQL node on host with matching scheduling label.
The service should not be scaled to more than one.

## Data persistence

Persistent data will be stored in data directory, which is mapped to specified host directory.

## Networking

The service exposes the default PostgreSQL port: 5432.