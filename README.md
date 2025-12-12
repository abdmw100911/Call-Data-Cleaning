Customer Call List – Data Cleaning Using Pandas

This project demonstrates a complete data-cleaning workflow applied to a messy customer call list. The goal is to transform inconsistent, duplicate, or incomplete information into a clean dataset ready for analysis or customer outreach.

The notebook includes step-by-step cleaning using Python and the Pandas library.

Dataset Issues Identified

The raw dataset contained several problems:

Duplicate rows

Missing (NaN) values

Inconsistent phone-number formats

Special characters in last names

Non-useful / irrelevant columns

Unstandardized Yes/No values in categorical columns

Non-uniform address formatting

Rows where customers marked Do Not Contact

Missing or invalid phone numbers

Cleaning Steps Performed

The following transformations were applied:

1. Remove duplicate entries

Duplicates were dropped to avoid repeated customer records.

2. Drop irrelevant columns

Columns labeled as not useful were removed.

3. Clean name fields

Special characters such as ".", "/", "_" were removed using string methods and regular expressions.

4. Standardize phone numbers

• Extracted digits using regex
• Converted numbers into the format 123-456-7890
• Marked invalid numbers as Missing
• Removed rows with no usable phone number

5. Split and clean address data

Addresses were separated into Street, State, and PIN for readability.

6. Standardize categorical values

Converted all “Yes/No/N/A” entries in Paying Customer and Do_Not_Contact to Y, N, or None.

7. Remove customers who marked “Do Not Contact”

Rows with Do_Not_Contact = Y were removed.

8. Reset index

The cleaned dataset was reindexed for clarity.
Technologies Used

• Python
• Pandas
• Jupyter Notebook

How to Use

Clone or download the repository

Open the notebook in Jupyter

Run the notebook to reproduce the cleaning steps
