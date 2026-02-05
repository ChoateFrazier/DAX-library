# DAX Library – Guidance & Standards

This document defines the conventions, assumptions, and best practices used in this
repository. All DAX code should follow these guidelines to ensure consistency,
readability, and reliable reuse across your Power BI models.

---

## 1. Scope of This Repository

This repository is intended to store:

- Reusable **DAX measures**
- Reusable **calculated columns**
- Reusable **calculated tables**
- General-purpose **DAX snippets**

This repository is **not** intended to store:
- Full Power BI reports (`.pbix`)
- Model-specific hard-coded logic
- Power Query (M) transformations (unless explicitly labeled)

---

## 2. When to Use DAX vs Power Query (M)

Use **DAX** when:
- Calculations depend on filter context
- Logic must respond to slicers or visuals
- You are aggregating model data
- You are implementing time intelligence

Use **Power Query (M)** when:
- Cleaning or standardizing text
- Splitting or exploding delimited fields
- Shaping or normalizing data
- Creating Date or helper dimension tables

---

## 3. Modeling Assumptions

Unless otherwise noted, DAX in this repository assumes:

- A **star schema** data model
- Fact tables contain numeric measures only
- Dimension tables contain descriptive attributes
- A single, dedicated **Date table**
- The Date table is marked as a Date table
- One active relationship between fact tables and the Date table

Any code submitted to this library that deviates from these assumptions will be explicitly labeled.

---

## 4. Naming Conventions

### Measures
- Use business-friendly names
- Use title case
- Prefix with nouns or actions

Examples:
- `Total Billings`
- `Revenue YTD`
- `Lawyer Headcount`

### Calculated Columns
- Use singular nouns
- Use `Is` or `Has` for boolean columns

Examples:
- `Is Active Customer`
- `Customer Segment`

### Calculated Tables
- Name tables by their business purpose

Examples:
- `Date`
- `Customer Rank Bands`

### Snippets
- Prefix code snippets with `_`

Examples:
- `_Base Revenue`
- `_Selected Date`

---

## 5. Code Style & Formatting

- Use variables (`VAR`) to improve readability
- One logical step per variable
- Avoid deeply nested expressions when possible
- Prefer explicit formatting over clever shortcuts

## 6. Feedback and Contributions

- Find Choate Frazier on LinkedIn; we welcome any and all feedback
- Reach out to the Choate Frazier team if you have additional code you would like added to this repository
