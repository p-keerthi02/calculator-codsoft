# Define functions for arithmetic operations
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Cannot divide by zero"
    else:
        return x / y

# Map operation symbols to functions
operations = {
    '+': add,
    '-': subtract,
    '*': multiply,
    '/': divide
}

# Function to perform calculations
def calculate():
    while True:
        # Prompt user for input
        try:
            num1 = float(input("Enter first number: "))
            operation = input("Enter operation (+, -, *, /): ")
            num2 = float(input("Enter second number: "))
            
            # Perform calculation
            if operation in operations:
                result = operations[operation](num1, num2)
                print("Result:", result)
            else:
                print("Invalid operation")
        except ValueError:
            print("Invalid input. Please enter a valid number.")
        
        # Ask user if they want to continue
        continue_calculation = input("Do you want to calculate again? (yes/no): ")
        if continue_calculation.lower() != 'yes':
            break

# Start the calculator
calculate()

