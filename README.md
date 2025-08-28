# python-calculator
A simple Python calculator project for learning Git basics
# Simple Python Calculator (CLI)
# Author: Sagar Bedre

def add(x, y): 
    return x + y

def sub(x, y): 
    return x - y

def mul(x, y): 
    return x * y

def div(x, y):
    if y == 0:
        return "Error: Division by zero"
    return x / y

def get_number(prompt):
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("Invalid number, please try again.")

def main():
    while True:
        print("\n=== Python Calculator ===")
        print("1) Add  2) Subtract  3) Multiply  4) Divide  5) Exit")
        choice = input("Choose (1-5): ").strip()

        if choice == "5":
            print("Goodbye!")
            break

        if choice not in {"1","2","3","4"}:
            print("Invalid choice, try again.")
            continue

        a = get_number("Enter first number: ")
        b = get_number("Enter second number: ")

        if choice == "1": 
            result = add(a, b)
        elif choice == "2": 
            result = sub(a, b)
        elif choice == "3": 
            result = mul(a, b)
        else: 
            result = div(a, b)

        print("Result:", result)

if __name__ == "__main__":
    main()
