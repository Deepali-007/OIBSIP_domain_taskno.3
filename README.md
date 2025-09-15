# OIBSIP_domain_taskno.3

**Data Cleaning Project**

This project focuses on cleaning a deliberately messy dataset of 1000 rows in Excel. The dataset was designed with common real-world data quality issues, and the goal was to systematically detect and fix them using Excel tools and formulas.

**Step 1:** Dataset
The dataset contains the following columns with intentional problems:

CustomerID: 200 unique IDs repeated, causing duplicates.

Name: Inconsistent capitalization and typos.

Age: Missing values, negative ages, and unrealistic values (e.g., 150).

Gender: Mixed formats like M/F, male/female, etc.

JoinDate: Mixed date formats such as 2024/01/15, 15-01-2024, Jan 15, 24.

Product: Typos and inconsistent naming like "Shoes", "shoe", "Shoe.".

Price: Missing values, currency symbols, and negative prices.

Quantity: Includes zero or negative values.

Total: Contains mismatches that don’t equal Price × Quantity.

**Step 2:** Data Cleaning Tasks in Excel
These tasks were performed to clean the dataset:

Handle Missing Data

Used Filter to find blanks in Age, Price, or Quantity.

Filled missing values using Average or Median formulas.

Left blanks where appropriate.

Remove Duplicates

Applied Data → Remove Duplicates on CustomerID and Name (or all fields).

Ensured only unique records remained.

Standardize Formats

Converted inconsistent dates using =DATEVALUE().

Normalized Gender with formulas like =IF(OR(A2="M",A2="Male"),"Male","Female").

Corrected Product names using =PROPER() for consistent capitalization.

Correct Invalid Values

Highlighted unrealistic Ages (<0 or >100) with Conditional Formatting.

Flagged negative or invalid Price/Quantity values.

Recalculated Total using =Price*Quantity to ensure accuracy.

Detect Outliers

Used Conditional Formatting → Top/Bottom Rules → Above 2 Std Dev.

Applied on Age and Price to detect extreme values.
