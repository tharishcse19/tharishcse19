# Simple Calculator using if-else in Python

def calculator():
    try:
        # Input first number
        num1 = float(input("Enter first number: "))
        # Input second number
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("Invalid input! Please enter numeric values.")
        return

    # Input operation choice
    print("\nSelect operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    
    choice = input("Enter choice (1/2/3/4): ").strip()

    # Perform calculation using if-else
    if choice == '1' or choice == '+':
        result = num1 + num2
        print(f"Result: {num1} + {num2} = {result}")
    elif choice == '2' or choice == '-':
        result = num1 - num2
        print(f"Result: {num1} - {num2} = {result}")
    elif choice == '3' or choice == '*':
        result = num1 * num2
        print(f"Result: {num1} * {num2} = {result}")
    elif choice == '4' or choice == '/':
        if num2 == 0:
            print("Error: Division by zero is not allowed.")
        else:
            result = num1 / num2
            print(f"Result: {num1} / {num2} = {result}")
    else:
        print("Invalid choice! Please select 1, 2, 3, or 4.")

# Run the calculator
if __name__ == "__main__":
    calculator()
