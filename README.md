 Python program is designed to read a list of grades from a file, calculate the total points earned, maximum possible points, and determine the final grade and percentage. Here's a breakdown of how the code works and what it accomplishes:

Functionality Overview
File Input:

The program prompts the user to enter the name of an input file containing grades.
It attempts to open the file and read the grades, ensuring that only valid integers are processed. If the file doesn't exist, it catches a FileNotFoundError and prints an error message.
Grade Calculation:

It calculates the number of grades, total points earned, and maximum possible points (assuming each grade is out of 100).
If no grades are found, it sets the final percentage to 0 and assigns a letter grade of F.
Otherwise, it computes the final percentage by dividing the total points by the maximum points and multiplying by 100.
The determine_letter_grade function is called to determine the final letter grade based on the final percentage.
Output:

The program prints a summary of the grades, including:
The number of grades.
The total points earned.
The maximum possible points.
For each grade, it prints the grade and its percentage relative to the maximum possible points.
Finally, it displays the final letter grade and percentage.
