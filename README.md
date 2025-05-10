# 🎵 Vinyl Collection Database System

A comprehensive Oracle Database solution for managing vinyl record collections, built as part of my CST2355 Database Systems course.
***Developed by**: Fiona Ang, Smriti Kohli, Olivier Niyonshima*

## ✨ Features
- **Artist Management**: Track bands and solo artists with validation
- **Album Cataloging**: Store release years, genres, and track listings
- **Temporal Relationships**: Track how artists, albums and recordings relate over time
- **Packaged Procedures**: Easy-to-use interfaces for common operations
- **View Triggers**: Automatic handling of complex data relationships

## 🛠️ Technical Highlights
- Oracle Database 19c implementation
- Temporal data modeling with start/end timestamps
- INSTEAD OF triggers for updatable views
- Data validation with regular expressions
- Sequence-based ID generation

## 🚀 Getting Started
1. Run the setup script as SYSDBA:
```sql
@setup_vinyl_db.sql
```

2. Connect as application user:
```sql
CONNECT groupAssignment2_admin/GroupAssignment2Password123
```
3. Use the packaged procedures:
```sql
-- Add a new artist with an album
DECLARE
  v_id NUMBER;
BEGIN
  v_id := artist_pkg.new_artist(
    'Pink Floyd', 
    'Band',
    'The Dark Side of the Moon',
    1973,
    1
  );
END;
/
```

## 📚 Academic Context
Developed as part of CST2355 Database Systems at Algonquin College, this group project demonstrates:
- Advanced Oracle PL/SQL programming
- Temporal database concepts
- Database design patterns
- Application encapsulation techniques
