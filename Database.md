# Database

## Table: Student List
- [Integer] Primary Key: Generated ID
- [String] Student ID
- [String] Name
- [Boolean] Whether is poor student
- [Integer] Current point

## Table: Point Changes
- [Integer] Primary Key: Generated ID
- [String] Student ID of subject
- [String] Student ID of operator
- [Integer] Point before change
- [Integer] Point after change
- [DateTime] Timestamp

`Student ID of subject` and `Student ID of operator` might be replaced with its primary key in *Student List*

## Table: Transcation Records
- [Integer] Primary key: Generated ID
- [String] Student ID of subject
- [String] Student ID of operator
- [DateTime] Timestamp
- [Integer] Key of item
- [Integer] Amount of item
- [Decimal] Discount factor
- [Integer] Original price
- [Integer] Final price

`Student ID of subject` and `Student ID of operator` might be replaced with its primary key in *Student List*

## Table: Item List
- [Integer] Primary key: Generated ID
- [String] Name
- [String] Description
- [URL] Image URL
- [Integer] Pirce
- [Boolean] Discount for poor student
- [DateTime] Creation time
- [String] Student ID of creator

`Student ID of creator` might be replaced with its primary key in *Student List*

## Table: Donation List
- [Integer] Primary key: Generated ID
- [String] Student ID of donator
- [String] Content
- [DateTime] Timestamp

`Student ID of donator` might be replaced with its primary key in *Student List*

## Table: Rental Records
- [Integer] Primary key: Generated ID
- [String] Student ID of borrower
- [String] Student ID of operator
- [String] Phone number of borrower
- [DateTime] Deadline
- [DateTime] Timestamp

`Student ID of borrower` and `Student ID of operator` might be replaced with its primary key in *Student List*

## Table: Gift Records
- [Integer] Primary key: Generated ID
- [String] Student ID of receiver
- [String] Student ID of operator
- [String] Phone number of receiver
- [Integer] Key of item
- [Integer] Amount of item
- [DateTime] Timestamp

`Student ID of receiver` and `Student ID of operator` might be replaced with its primary key in *Student List*
