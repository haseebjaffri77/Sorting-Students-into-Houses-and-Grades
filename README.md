readme_content = """
# Sorting Students into Houses and Grades
#### Video Demo:https://youtu.be/Auf-W86oxF8
#### Description: An automated system that assigns students to Hogwarts houses and calculates their grades based on CSV input data.

This project is designed to process student data, assign each student to a fictional "house" based on their personality characteristics, and calculate their school grade based on their birth year. The project reads data from an input CSV file, processes it, and generates an output CSV file with the updated information.

---

### **Features**

1. **House Assignment:**
   - Assigns students to one of four houses: Gryffindor, Hufflepuff, Ravenclaw, or Slytherin, based on specific personality characteristics.
   - If a characteristic doesn’t match any predefined category, the student is labeled as belonging to "No House."

2. **Grade Calculation:**
   - Calculates the student’s school grade based on their birth year, assuming they began school at the age of 5.

3. **Error Handling:**
   - Ensures only valid CSV files are processed.
   - Checks for correct command-line arguments and handles file-not-found errors gracefully.

---

### **How It Works**

1. **Input File:**
   The program reads a CSV file (e.g., `new_students.csv`) containing:
   - `name`: The student’s name.
   - `characteristic`: A key personality trait of the student.
   - `birthdate`: The student’s year of birth.

2. **Processing:**
   - `select_house`: Assigns a house based on the `characteristic` column.
   - `select_grade`: Calculates the student’s grade based on the `birthdate` column.

3. **Output File:**
   A new CSV file (e.g., `after.csv`) is created containing:
   - `name`: The student’s name.
   - `house`: The house assigned based on their characteristic.
   - `grade`: The calculated grade.

---

### **File Overview**

1. **`project.py`:**
   - The main Python script that performs the data processing.
   - Functions include:
     - `check_correct_args`: Ensures the script is run with proper command-line arguments.
     - `select_house`: Assigns a house based on characteristics.
     - `select_grade`: Calculates grades based on the birth year.

2. **`test_project.py`:**
   - Contains unit tests to verify the functionality of `select_house` and `select_grade`.

3. **`new_students.csv`:**
   - Input file containing sample student data to be processed.

4. **`after.csv`:**
   - Output file containing the processed student data, with houses and grades.

---

### **How to Run**

1. **Run the Program:**
   Execute the script from the command line, specifying the input and output CSV file names:
   ```bash
   python project.py new_students.csv after.csv
