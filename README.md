# python-file-handling-exceptions
Python programs demonstrating text file reading/writing, runtime error handling using try-except-finally, and custom exceptions.
# Reading and Writing Text Files with Exception Handling
ile.write("Welcome to Python File Handling.")
    file.close()

    print("Data written successfully.")

    # Reading data from the file
    file = open("sample.txt", "r")
    conte
try:
    # Writing data to a file
    file = open("sample.txt", "w")
    file.write("Hello Deepak!\n")
    fnt = file.read()
    print("\nFile Content:")
    print(content)

except FileNotFoundError:
    print("Error: File not found.")

except PermissionError:
    print("Error: Permission denied.")

finally:
    print("\nFile operation completed.")
    # Custom Exception Example

class NegativeNumberError(Exception):
    pass

try:
    num = int(input("Enter a positive number: "))

    if num < 0:
        raise NegativeNumberError("Negative numbers are not allowed.")

    print("You entered:", num)

except NegativeNumberError as e:
    print("Custom Exception:", e)

except ValueError:
    print("Error: Invalid input. Please enter a number.")

finally:
    print("Program executed successfully.")
