# Historical Data Transformation

This Python script transforms columnar employee data into a historical, row-based versioning format suitable for database storage.

## methodology 

1. **Data Reading:** The input CSV file containing employee data is read using Pandas library.
2. **Data Preprocessing:** Date columns are converted to datetime format to facilitate date calculations.
3. **Historical Record Generation:** For each employee, historical records are generated for compensation, review, and engagement based on join dates, exit dates, and relevant date columns in the input file.
4. **Data Transformation:** The historical records are then transformed into a row-based format suitable for database storage, ensuring that each row represents a specific period with consistent data.
5. **Output Generation:** The transformed data is written to a new CSV file as per the required output format.

## Assumptions

1. **Data Consistency:** It is assumed that the input CSV file is properly structured and does not contain irregularities or inconsistencies.
2. **Date Format Consistency:** All date columns are assumed to have consistent formats that can be directly converted to datetime objects.
3. **Maximum Records:** It is assumed that each employee has at most two records for compensation, review, and engagement, as indicated by the columns present in the input file.
4. **Missing Values Interpretation:** Missing values for compensation, review, and engagement are interpreted as no changes occurring during that period, and values are inherited from the most recent past record for the same employee.

## Usage

1. Clone the repository.
2. Install the required dependencies (`pandas`).
3. Run the `Historical Data Transformation.ipynb` script to perform the transformation.
4. Transformed data will be saved in a new CSV file.

