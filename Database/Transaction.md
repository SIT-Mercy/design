# Transaction

## Table: Student List

- [Integer] Primary Key: Generated ID
- [String] Student ID
- [String] Name
- [Boolean] Whether is poor student
- [Integer] Current point

## Table: Point Changes

- [Integer] Primary Key: Generated ID
- [Integer] Key of subject
- [Integer] Key of operator
- [Integer] Point before change
- [Integer] Point after change
- [DateTime] Timestamp

## Table: Transcation Records

- [Integer] Primary key: Generated ID
- [Integer] Key of subject
- [Integer] Key of operator
- [DateTime] Timestamp
- [Integer] Key of item
- [Integer] Amount of item
- [Decimal] Discount factor
- [Integer] Original price
- [Integer] Final price

## Table: Item List

- [Integer] Primary key: Generated ID
- [String] Name
- [String] Description
- [URL] Image URL
- [Integer] Pirce
- [Boolean] Discount for poor student
- [DateTime] Creation time
- [Integer] Key of creator

## Table: Donation List

- [Integer] Primary key: Generated ID
- [Integer] Key of donator
- [String] Content
- [DateTime] Timestamp

## Table: Rental Records

- [Integer] Primary key: Generated ID
- [Integer] Key of borrower
- [Integer] Key of operator
- [String] Phone number of borrower
- [DateTime] Deadline
- [DateTime] Timestamp

## Table: Gift Records

- [Integer] Primary key: Generated ID
- [Integer] Key of receiver
- [Integer] Key of operator
- [String] Phone number of receiver
- [Integer] Key of item
- [Integer] Amount of item
- [DateTime] Timestamp
