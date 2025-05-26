# Data-Preprocessing
Data Wrangling, Data Cleaning, Data Manipulation

This repository contains a step-by-step guide to preprocess the Marketing Campaign dataset using Microsoft Excel. It is ideal for beginners and involves cleaning, structuring, and preparing the dataset for analysis.
asks Performed

1. Open and Inspect the Dataset

Open the marketing_campaign.csv file in Excel.
Use Data > Text to Columns if all data appears in a single column (choose comma as delimiter).
Ensure headers are in Row 1, and each column has a clear, unique name.

2. Structure the Raw Data

Delete empty rows or irrelevant cells.
Format the range as a Table: Go to Home > Format as Table and select a style. Make sure “My table has headers” is checked.

3. Identify Missing Values

Select the dataset and apply Filter from the toolbar.
Check each column's dropdown filter to look for (Blanks).

4. Fill Missing Income Values with Median

Insert a new row below the income column and calculate the median:
=MEDIAN(E2:E2241) or =MEDIAN(FILTER([Income], ISNUMBER([Income])))
Copy the result.
Filter Income for blanks and paste the median into those cells.

5. Rename Column Headers (Lowercase)

Manually edit each header in Row 1.
Convert to lowercase, replace spaces with underscores (_), and remove special characters.
Example: Year_Birth ➝ year_birth

6. Remove Duplicate Rows

Select all data.
Go to Data > Remove Duplicates.
Check all columns and click OK.
Excel will report how many duplicates were removed.

7. Standardize Text Entries

Use filters to find inconsistent text values.
Manually fix inconsistent spellings or capitalization (e.g., divorced, Divorced, DIVORCED ➝ divorced).

8. Convert Date Formats

Select the date column (e.g., Dt_Customer).
Right-click > Format Cells > Date.
Choose or create a dd-mm-yyyy format.

9. Check and Fix Data Types

Make sure:
Numbers (e.g., age, income) are formatted as Number.
Dates are formatted correctly.
Text columns are formatted as Text.

10. Save the Cleaned Dataset

Go to File > Save As.
Save as: marketing_campaign cleaned file.xlsx
File Type: Excel Workbook (.xlsx)
