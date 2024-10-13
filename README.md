## Student Information

- *Name*: Mohamuud Muhiidin cabdullahi
- *Class ID*: C1210601
- *Class Name*: CA213

---
# Project Title: **Calculate Total Target**

## Description
This project provides a function that calculates a total annual target, distributing it evenly across months while excluding Fridays from the working days. The function returns a detailed breakdown of days worked (excluding Fridays) and monthly targets.

## Instructions to Run the Code
1. Clone the repository from GitHub:
   ```bash
   git clone https://github.com/yourusername/repository-name.git
   cd repository-name
   ```
2. Open the project in any JavaScript environment (e.g., Node.js):
   - To run the project using Node.js, ensure Node.js is installed on your system. Run the following command:
   ```bash
   node calculateTarget.js
   ```

## Explanation of Function and How It Works
The function `calculateTotalTarget(startDate, endDate, totalAnnualTarget)` takes three inputs:
- `startDate`: The beginning of the period (e.g., '2024-01-01').
- `endDate`: The end of the period (e.g., '2024-03-31').
- `totalAnnualTarget`: The total target to be achieved within the year (e.g., 5220).

The function:
1. Calculates the number of working days in each month (excluding Fridays).
2. Distributes the `totalAnnualTarget` across 12 months evenly.
3. Filters months without workdays and adjusts targets for months that contain workdays.
4. Outputs the data as a JSON object containing:
   - `daysWorkedExcludingFridays`: An array showing the number of workdays (excluding Fridays) per month.
   - `monthlyTargets`: An array showing the target assigned for each month with workdays.
   - `totalTarget`: The sum of the monthly targets.

## Example of Usage
```js
const result = calculateTotalTarget('2024-01-01', '2024-03-31', 5220);
console.log(result);
```

The output for this example will be:
```json
{
  "daysWorkedExcludingFridays": [21, 20, 20],
  "monthlyTargets": [435, 435, 435],
  "totalTarget": 1305
}
```

## Assumptions and Limitations
- The function assumes that the year is a standard year with no leap year adjustments.
- It distributes the total target equally across months, which may not reflect real-world fluctuations in workload or target requirements.
- The current implementation does not consider holidays other than Fridays.

