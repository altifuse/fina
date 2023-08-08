# fina
**Multicurrency zero-based budgeting system**

## Overview

This project is the implementation of my personal budgeting system, which implements a version of envelope and zero-based budgeting techniques. Main characteristics:

* Built from the ground up with multiple currency support within budgets
* Leverages simplified double-entry accounting
* Extensible budgeting and planning system with various contribution types

I am currently keeping the full documentation of this project in a private environment, as I synthesize the system I use into a sensible structure.

### Background

From my experiences with YNAB, I replicated the set of features I used in Excel and evolved the system according to my needs. I have since then reached a point where UX and flexiblity in a spreadsheet-based system are too limited - this inspired the creation of **fina**.

My budgeting needs - and, therefore, the guiding requirements for this project - are determined by a few facts:

* I have fixed, predictable income
* I regularly handle operations with multiple currencies (online shopping, investing, traveling)
* I have an investment plan

Furthermore, I enjoy working with Python and want to take the opportunity to learn and apply project management skills.

## Roadmap

### v0.1 | MVP - Accounting foundations

- CLI only
- File-based storage
- Single User
- Single Budget
- New actions:
    - Create Currency
    - Create Asset/Liability
    - Create Category (no Currency specified, multiple instances are created automatically as Transactions occur)
    - Create Income/Expense (automatically create Source/Sink)
    - Create Physical Transfer
    - Create Logical Transfer
    - List and describe all Balances

### v0.2 | Budgeting foundations

- New actions:
    - Create Target Balance
    - List and describe all Target Balances
    - Create Exchange
    - List and describe all Currencies (including amounts)

### v0.3 | Scheduling foundations

- Budget is now time-aware
- New actions:
    - Set reporting period (select month and year)
    - Create Scheduled Contribution
    - Create Target Balance by Date
    - List and describe all Contributions
    - Edit Currency
    - Edit Balance
    - Edit Transaction

### v0.4 | Multi-tenancy foundations

- Multiple Budgets are supported
- Multiple Users are supported (no authentication - a User is just a set of Budgets)
- New actions:
    - Create/edit Budget
    - Select Budget at startup
    - Create/edit User
    - Select User at startup

### v0.5 | API foundations

- REST API without authentication 
- APIs:
    - CRUD for Budget
    - CRUD for Currency
    - CRUDs for all types of Balance
    - CRUDs for all types of Transaction
    - CRUDs for all types of Contributions

### v0.6 | GUI foundations

### v0.7 | More GUI & API work

### TBD...

### v1.0 | Beta release

- Database with optional per-tenant encryption
- Basic authentication system
- Ledger export as CSV
