# Database

## Table: Staff List

- [Integer] Primary Key: Generated ID
- [Integer] Key(Student List)
- [String] Password
- [String] Authority: such as `Transaction Operator`, `Admin`
- [DateTime] Last login time

## Table: Student List

- [Integer] Primary Key: Generated ID
- [String] Student ID
- [String] Name
- [Boolean] is poor student
- [String?] Phone number // null for not yet recorded
- [Integer] Current point

## Table: Point Changes

- [Integer] Primary Key: Generated ID
- [Integer] Key(Student List) of subject
- [Integer] Key(Staff List) of operator
- [String?] Reason: such as `redeem`, `rental`, `yearlyCost`, `volunteer` or null.
- [Integer] Point before change
- [Integer] Point after change
- [DateTime] Creation Time

## Table: Transcation Records

- [Integer] Primary key: Generated ID
- [Integer] Key(Student List) of subject
- [Integer] Key(Staff List) of operator
- [DateTime] Creation Time
- [Integer] Key(Item List) of item
- [Integer] Amount of item
- [Decimal] Discount factor
- [Integer] Original price // the forzeen price from item
- [Integer] Final price

## Table: Item List

- [Integer] Primary key: Generated ID
- [String] Name
- [String] Description
- [Integer] Amount in stock
- [Integer] Price
- [Integer] Rent
- [Boolean] Has discount for poor student
- [Boolean] Rentable
- [Boolean] For sale
- [DateTime] Creation time

## Table: Item Amount Changes

- [Integer] Primary key: Generated ID
- [Integer?] Key of related table:
  - `redeemed` for Transcation Records;
  - `rented` for Rental Records;
  - null for nothing related
- [Integer] Key(Item List) of item
- [Integer] Amount before
- [Integer] Amount after
- [DateTime] Creation time
- [String?] Reason: such as `redeemed`, `rented`, `missing` or null.

## Table: Donation List

- [Integer] Primary key: Generated ID
- [Integer] Key(Student List) of donator
- [Integer] Key(Staff List) of operator
- [String] Note
- [DateTime] Creation Time

## Table: Rental Records

- [Integer] Primary key: Generated ID
- [Integer] Key(Student List) of borrower
- [Integer] Key(Staff List) of operator
- [Integer] Key(Item List) of item
- [Sting] Name // might be different from the actually borrower
- [String] Phone number // might be different from the actually borrower
- [DateTime] Deadline
- [DateTime] Creation time
- [DateTime?] Return time // null for not yet returned

## Table: Gift Records

- [Integer] Primary key: Generated ID
- [Integer] Key(Student List) of receiver
- [Integer] Key(Staff List) of operator
- [String] Phone number of receiver
- [Integer] Key(Item List) of item
- [Integer] Amount of item
- [DateTime] Creation Time
