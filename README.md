def calculate_grade(marks):
    """Calculates the total marks, average percentage, and assigns a grade.

    Args:
        marks: A list of marks obtained in each subject.

    Returns:
        A tuple containing the total marks, average percentage, and grade.
    """
    if not marks:
        return 0, 0, 'No Grade'  # Handle the case of an empty list gracefully

    total_marks = sum(marks)
    average_percentage = total_marks / len(marks)

    if average_percentage >= 90:
        grade = 'A+'
    elif average_percentage >= 80:
        grade = 'A'
    elif average_percentage >= 70:
        grade = 'B'
    elif average_percentage >= 60:
        grade = 'C'
    else:
        grade = 'F'

    return total_marks, round(average_percentage, 2), grade

# Example usage:
marks = [85, 92, 78, 89, 95]
total, average, grade = calculate_grade(marks)

print("Total Marks:", total)
print("Average Percentage:", average)
print("Grade:", grade)
