## Normalization of Library Management System
## UNF (Unnormalized Form)

A single table containing all data with repeating groups.

| MemberID | MemberName | Email                                   | BookTitles (repeating)   | BorrowDates (repeating) |
| -------- | ---------- | --------------------------------------- | ------------------------ | ----------------------- |
| 1        | Juan Cruz  | [juan@email.com](mailto:juan@email.com) | Noli Me Tangere, El Fili | 2025-03-01, 2025-03-02  |

Problems:

Multiple values in one column (not atomic)
Data redundancy (member info repeated)
Hard to update and search
Prone to inconsistencies

## 1NF (First Normal Form)

Convert repeating groups into separate rows (atomic values).

| MemberID | MemberName | Email                                   | BookTitle       | BorrowDate |
| -------- | ---------- | --------------------------------------- | --------------- | ---------- |
| 1        | Juan Cruz  | [juan@email.com](mailto:juan@email.com) | Noli Me Tangere | 2025-03-01 |
| 1        | Juan Cruz  | [juan@email.com](mailto:juan@email.com) | El Fili         | 2025-03-02 |

## Improvements:

No repeating groups
Each field contains only one value

## Remaining Issue:

MemberName and Email depend only on MemberID → partial dependency

## 2NF (Second Normal Form)

Remove partial dependencies by separating tables.
Members Table
| MemberID | MemberName | Email                                   |
| -------- | ---------- | --------------------------------------- |
| 1        | Juan Cruz  | [juan@email.com](mailto:juan@email.com) |

## Borrow Table (Still not final)
| MemberID | BookTitle       | BorrowDate |
| -------- | --------------- | ---------- |
| 1        | Noli Me Tangere | 2025-03-01 |
| 1        | El Fili         | 2025-03-02 |

## Improvements:

Member details stored only once
Reduced redundancy

Remaining Issue:

BookTitle is still text → repeated and not normalized
No separate book entity (transitive dependency)

## 3NF (Third Normal Form)

Remove transitive dependencies by introducing proper tables.

Members
| MemberID | Name      | Email                                   |
| -------- | --------- | --------------------------------------- |
| 1        | Juan Cruz | [juan@email.com](mailto:juan@email.com) |

Books

| BookID | Title             | Author     |
| ------ | ----------------- | ---------- |
| 1      | Noli Me Tangere   | Jose Rizal |
| 2      | El Filibusterismo | Jose Rizal |

Borrow
| BorrowID | MemberID | BookID | BorrowDate |
| -------- | -------- | ------ | ---------- |
| 1        | 1        | 1      | 2025-03-01 |
| 2        | 1        | 2      | 2025-03-02 |

Staff (independent table)
| StaffID | Name        |
| ------- | ----------- |
| 1       | Maria Lopez |

## Final Result (3NF)

Tables:

Members
Books
Borrow
Staff

Benefits:

No redundancy
No partial or transitive dependencies
Data is consistent and easy to maintain
Efficient querying using JOIN operations