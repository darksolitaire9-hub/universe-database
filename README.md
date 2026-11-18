# Universe Database

A PostgreSQL relational database project for modeling galaxies, stars, planets, moons, and constellations.

## Schema

- `galaxy`: galaxies, with age, description, and type
- `star`: stars linked to a galaxy
- `planet`: planets linked to a star
- `moon`: moons linked to a planet
- `constellation`: constellations with descriptions

Primary keys use auto-incrementing integer sequences. Names are required and unique within each table. The schema also uses foreign keys to connect stars to galaxies, planets to stars, and moons to planets.

## Sample data

The database dump contains 6 galaxies, 6 stars, 12 planets, 20 moons, and 3 constellations.

## Restore

The plain SQL dump is in [`universe.sql`](./universe.sql). In the FreeCodeCamp PostgreSQL environment, restore it with:

```sh
psql -U freecodecamp -d postgres -f universe.sql
```

The dump drops and recreates the `universe` database, so only restore it when replacing that database is intended.
