# Database

`mutable` means mutable data.

## Table: Staff List

- [Integer] Primary Key: Generated ID
- [Integer] Key(Student List)
- [String] [mutable] Password
- [String] [mutable] Authority: such as `Transaction Operator`, `Admin`
- [DateTime] [mutable] Last login time

## Table: Student List

- [Integer] Primary Key: Generated ID
- [String] Student ID
- [String] [mutable] Name
- [String] [mutable] College
- [Short] [mutable] poor level: `not poor`, `poor`, `very poor`.
- [String?] [mutable] Phone number // null for not yet recorded
- [Integer] [mutable] Current point

## Table: Point Changes

- [Integer] Primary Key: Generated ID
- [Integer] Key(Student List) of subject
- [Integer] Key(Staff List) of operator
- [String?] Reason: such as `redeem`, `rental`, `yearlyCost`, `volunteer` or null.
- [Integer] Point before change
- [Integer] Point after change
- [DateTime] Creation Time

## Table: Transaction Records

For gift records, price is 0.

- [Integer] Primary key: Generated ID
- [Integer] Key(Student List) of customer
- [Integer] Key(Staff List) of operator
- [DateTime] Creation Time
- [Integer] Key(Item List) of item
- [Integer] Amount of item
- [Integer] Unit price
- [Decimal] price factor
- [Integer] Final total price

## Table: Item List

- [Integer] Primary key: Generated ID
- [String] [mutable] Name
- [String] [mutable] Description
- [String?] [mutable] Internal note // only for staff
- [Integer] [mutable] Amount in stock
- [Integer?] [mutable] Price  // null if not for sale
- [Integer?] [mutable] Rent   // null if not rentable
- [Decimal] [mutable] price factor for poor student
- [DateTime] Creation time

## Table: Item Amount Changes

- [Integer] Primary key: Generated ID
- [Integer?] Key of related table:
  - `redeemed` for Transcation Records;
  - `rented` for Rental Records;
  - `returned` for Rental Records;
  - `ownUse`for internal consumption.
  - null for nothing related
- [Integer] Key(Item List) of item
- [Integer] Amount before
- [Integer] Amount after
- [DateTime] Creation time
- [String?] Note
- [String?] Reason: such as `redeemed`, `rented`,`missing`, `ownUse` or null.

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
- [Json] [mutable] Renewal list

  ```json
  [
    {
      "from":"yyyy-MM-dd-hh:mm:ss",
      "to":"yyyy-MM-dd-hh:mm:ss,
    }
  ]
  ```

- [DateTime] [mutable] Deadline
- [DateTime] Creation time
- [DateTime?] [mutable] Return time // null for not yet returned
