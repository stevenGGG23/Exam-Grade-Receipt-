def main():
    filename = input("Enter the input file: ")
    try:
        with open(filename, 'r') as file:
            grades = [int(line.strip()) for line in file if line.strip().isdigit()]
    except FileNotFoundError:
        print(f"{filename} does not exist!")
        return

    number_grades = len(grades)
    total_points = sum(grades)
    max_points = number_grades * 100

    if number_grades == 0:
        final_percentage = 0
        final_grade = 'F'
    else:
        final_percentage = (total_points / max_points) * 100
        final_grade = determine_letter_grade(final_percentage)

    print()
    print(f"Number of Grades:       {number_grades:>5}")
    print(f"Total Points Earned:    {total_points:>5}")
    print(f"Max Possible Points:    {max_points:>5}")
    print()

    for grade in grades:
        percent = (grade / max_points) * 100
        print(f"{grade:>20}{percent:>9.1f}%")

    print()
    print(f"{'Final Grade:':<8}{final_grade:>8}     {final_percentage:.1f}%")


def determine_letter_grade(percentage):
    if 90 <= percentage <= 100:
        return 'A'
    elif 80 <= percentage < 90:
        return 'B'
    elif 70 <= percentage < 80:
        return 'C'
    elif 60 <= percentage < 70:
        return 'D'
    else:
        return 'F'


if __name__ == "__main__":
    main()
