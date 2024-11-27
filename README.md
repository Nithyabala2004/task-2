# Employee Bonus and Compensation Management System

This project calculates employee bonuses and total compensation based on predefined department-specific rules. It also generates a comprehensive summary report grouped by department and updates employee records with the calculated data.

## Table of Contents
- [Features](#features)
- [Department Bonus Rules](#department-bonus-rules)
- [Technical Highlights](#technical-highlights)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Example Output](#example-output)
- [File Structure](#file-structure)
- [How It Works](#how-it-works)
- [Contributions](#contributions)
- [License](#license)



## Features

1. **Remove Duplicates**  
   - Eliminates duplicate employee entries based on their unique `id` using a `Set`.

2. **Filter Employees by Department**  
   - Allows filtering of employees based on the specified department.

3. **Calculate Total Compensation**  
   - Computes the base salary and bonus based on department-specific rules.
   - Calculates the total compensation (`salary + bonus`) for each employee.

4. **Generate Report**  
   - Produces a detailed report grouped by department.
   - Displays each employee's:
     - Name
     - Department
     - Salary
     - Bonus
     - Total compensation

5. **Update Employee Details**  
   - Updates the employee objects with the computed `bonus` and `totalCompensation`.



## Department Bonus Rules

- **HR**:  
  Employees with a salary below ₹50,000 receive an additional 10% bonus.

- **Engineering**:  
  Employees with more than 2 years of experience receive a 15% bonus.

- **Sales**:  
  Bonus is determined based on sales targets:
  - Sales below ₹1,00,000: 5% bonus.
  - Sales between ₹1,00,000 and ₹5,00,000: 10% bonus.
  - Sales above ₹5,00,000: 20% bonus.



## Technical Highlights

- **Array Processing**  
  Utilizes JavaScript `map` and `filter` for processing employee data.

- **Duplicate Removal**  
  Uses a `Set` to remove duplicate employee entries based on their `id`.

- **Bonus Calculation**  
  Implements `switch` or `if...else` statements for conditional bonus calculations.

- **Iteration**  
  Employs `for...of` and `for...in` loops to iterate over employee lists and department rules.

- **Efficient Computation**  
  Leverages compound assignment operators (`+=`, `*=`) for efficient calculations.



## Installation and Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```

2. Install dependencies (if required):
   ```bash
   npm install
   ```

3. Run the application:
   ```bash
   node app.js
   ```



## Usage

1. Initialize the employee data and department rules in the script.
2. Call the functions to:
   - Remove duplicates
   - Filter employees by department
   - Calculate bonuses and total compensation
   - Generate a report grouped by department
3. Output the updated employee list and summary report.



## Example Output

### Input
```javascript
const department = "Engineering";
```

### Output
```javascript
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
    ...
  ]
}
```



## File Structure

```
/project-directory
├── app.js          # Main entry point for the application
├── data.js         # Contains employee list and department rules
├── utils.js        # Helper functions for data processing
├── README.md       # Documentation for the project
└── package.json    # Project metadata and dependencies (if applicable)
```



## How It Works

1. **Initialization**  
   - Define an array of employee objects with details such as `id`, `name`, `department`, `salary`, `bonusPercentage`, etc.
   - Specify department-specific bonus rules.

2. **Data Processing**  
   - **RemoveDuplicates**: Use a `Set` to ensure unique employee entries based on `id`.
   - **FilterEmployees**: Filter the list of employees based on the selected department.
   - **CalculateBonusAndCompensation**: Use conditional logic to compute bonuses and total compensation.

3. **Report Generation**  
   - Group the employees by department.
   - Format the report to include `name`, `department`, `salary`, `bonus`, and `totalCompensation`.

4. **Output**  
   - Return the grouped report and the updated employee list.




