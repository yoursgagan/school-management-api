# School Management API

## Requirements

- Node.js
- MySQL

## Setup Instructions

1. Clone or extract the project.
2. Run `npm install` to install dependencies.
3. Set your MySQL credentials in `.env`.
4. Create MySQL DB with:

```sql
CREATE DATABASE school_db;
USE school_db;
CREATE TABLE schools (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  address VARCHAR(255),
  latitude FLOAT,
  longitude FLOAT
);
```

5. Run `node index.js` to start the server.

## API Endpoints

### POST /addSchool

Payload:
```json
{
  "name": "ABC School",
  "address": "123 Street",
  "latitude": 21.12,
  "longitude": 81.34
}
```

### GET /listSchools?latitude=21.15&longitude=81.36
Returns schools sorted by proximity.

