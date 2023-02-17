# Database

## Table: Point Changes
- [Integer] Primary Key: Generated ID
- [String] Student ID of subject
- [Integer] Point before change
- [Integer] Point after change
- [DateTime] Timestamp
- [String] Student ID of operator

## Table: Transcation Records
- [Integer] primary key: Generated ID
- [String] Student ID of subject
- [String] Student ID of operator
- [DateTime] Timestamp
- [Integer] Key of item
- [Integer] Amount of item
- [Decimal] Discount factor
- [Integer] Original price
- [Integer] Final price

## Table: Item List
- [Integer] primary key: Generated ID
- [String] Name
- [String] Description
- [URL] Image URL
- [Integer] Pirce
- [Boolean] Discount for poor student

## Table: 