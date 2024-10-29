import math

def display_menu():
    print("Select the operation you want to perform:")
    print("1. Standard Arithmetic")
    print("2. Trigonometry")
    print("3. Exponents")
    print("4. Square Root")
    print("5. Percentage")
    print("6. Exit")

def standard_arithmetic():
    operation = input("Select operation (+, -, *, /): ")
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        
        if operation == '+':
            result = num1 + num2
        elif operation == '-':
            result = num1 - num2
        elif operation == '*':
            result = num1 * num2
        elif operation == '/':
            if num2 == 0:
                print("Error: Division by zero is not allowed.")
                return
            result = num1 / num2
        else:
            print("Invalid operation selected.")
            return
        
        print(f"The result is: {result}")
    
    except ValueError:
        print("Error: Invalid input. Please enter numeric values.")