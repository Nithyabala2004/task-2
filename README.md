# Employee Bonus and Compensation Management System

This project calculates employee bonuses and total compensation based on department-specific rules and generates a summary report grouped by department.

## Features

1. **Remove Duplicates:**  
   Removes duplicate employees based on their unique `id` using a `Set`.

2. **Filter Employees by Department:**  
   Filters employees based on their department.

3. **Calculate Total Compensation:**  
   - Computes the base salary and bonus based on department-specific rules.
   - Calculates the total compensation (`salary + bonus`) for each employee.

4. **Generate Report:**  
   Produces a detailed report grouped by department, showing each employee's:
   - Name
   - Salary
   - Bonus
   - Total compensation

5. **Update Employee Details:**  
   Updates each employee's record to include the computed `bonus` and `totalCompensation`.

## Department Bonus Rules

- **HR:**  
  Employees with a salary below ₹50,000 receive an additional 10% bonus.  

- **Engineering:**  
  Employees with more than 2 years of experience receive a 15% bonus.  

- **Sales:**  
  Bonus is determined based on sales targets:
  - Sales below ₹1,00,000: 5% bonus.
  - Sales between ₹1,00,000 and ₹5,00,000: 10% bonus.
  - Sales above ₹5,00,000: 20% bonus.

## Technical Highlights

- **Array Processing:** Utilizes `map` and `filter` for handling employee data.
- **Duplicate Removal:** Uses a `Set` to ensure unique employee entries based on `id`.
- **Bonus Calculation:** Leverages `switch` or `if...else` for applying department-specific bonus rules.
- **Iteration:** Implements `for...of` and `for...in` loops for traversing employee lists and department rules.
- **Bonus and Compensation Calculation:** Uses compound assignment operators (e.g., `+=`, `*=`) for efficient computations.

## Example Usage

### Input:
```javascript
const department = "Engineering";

{
  report: {
    Engineering: [
      { name: 'Bob', salary: 60000, bonus: 9000, totalCompensation: 69000 },
      { name: 'Eve', salary: 70000, bonus: 10500, totalCompensation: 80500 }
    ]
  },
  updatedEmployees: [
    { id: 1, name: 'Bob', department: 'Engineering', salary: 60000, bonusPercentage: 15, bonus: 9000, totalCompensation: 69000 },
    { id: 2, name: 'Eve', department: 'Engineering', salary: 70000, bonusPercentage: 15, bonus: 10500, totalCompensation: 80500 },
    
  ]
}
