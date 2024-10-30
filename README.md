# Target Calculation Excluding Specific Days.

## Project Overview:
This project calculates the proportional distribution of an annual target across multiple months while excluding specific days (Fridays by default). The program accounts for only the valid working days within a specified date range and dynamically handles different months, years, and edge cases like mid-month start/end dates. The solution ensures accurate time-sensitive calculations without hard-coding specific date ranges or making assumptions about the number of days in each month.

## Features:

- Excludes Fridays: By default, the function excludes Fridays when calculating the working days for each month.
- Proportional Distribution: The annual target is distributed proportionally across the valid working days in the specified date range.
- Handles multiple months, leap years, and edge cases like mid-month starts and ends.
- Flexible Time Ranges: Can compute targets for any date range within the year, without hard-coded values for specific months.

## How the Program Works

- The function calculateTotalTarget(startDate, endDate, totalAnnualTarget) performs the following:

- Step 1: Loops through the months between the startDate and endDate.
- Step 2: For each month, calculates the total number of working days (excluding Fridays) and counts how many valid working days fall within the provided date range.
- Step 3: Distributes the totalAnnualTarget proportionally across the calculated working days for each month.

## How to Run the project

- 1. Clone the repository.
- 2. Run `node calculateTotalTarget.js` in the terminal.
- 3. Modify the function parameters for different date ranges.

## The output includes:

- daysExcludingFridays: Total working days for each month, excluding Fridays.
- daysWorkedExcludingFridays: Number of valid working days within the date range, excluding Fridays.
- monthlyTargets: The target assigned to each month, based on the number of valid working days.
- totalTarget: The total calculated target based on the valid working days.

## Assumptions:

- The annual target is distributed only among valid working days, and Fridays are considered non-working days by default.
- The date range can span multiple months and years, and the program correctly handles leap years and different month lengths.
- The user inputs valid dates in YYYY-MM-DD format.

## Limitations

- This implementation excludes only Fridays by default. Future improvements could involve excluding other non-working days, which could be passed as parameters.
- Currently, the code does not account for holidays or weekends other than Fridays.

## Possible Extensions

- Add support for excluding other days (e.g., Sundays or custom holidays) via additional parameters.
Optimize for larger date ranges to reduce time complexity.
- Implement a frontend interface for easier interaction with the functionality.