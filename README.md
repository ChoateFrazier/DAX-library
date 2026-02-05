# DAX-library
A collection of reusable DAX code for use in Microsoft Power BI.

The code used here has been developed primarily in the Marketing Analytics context, particulary for marketers and analysts in the Professional Services industry.

## How to use

1. Browse the folders by topic (M-Code, Measure, Calculated Columns, etc).
2. Open the file for the particular code you need.
3. For DAX, copy the code into Power BI:
   - Modeling → New measure / New column / New table
4. For M, copy the code into Power Query:
   - Home → Advanced Editor
4. Replace placeholder table and column names (e.g. `<table1>`, `<column1>`).

## Assumptions

Many of these entries assume:

1. A star schema data model
2. A dedicated Date table, marked as a Date Table
3. Measures (not column dumps) for dynamic calculations
4. Proper relationships between fact and dimension tables

## Naming Conventions

Measures | Uses descriptive, business-friendly names:
   - Total Sales
   - Sales YTD
   - Sales YoY %

Calculated Columns | Descriptive and singular:
   - Is Client
   - Industry

Calculated Tables | Identify purpose:
  - Rank Bands
  - Date

## License

This project is open source — use it freely in your BI work, tools, and models.

