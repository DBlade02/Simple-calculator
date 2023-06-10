# Simple-calculator
I make the simple calculator (Iron man edition)

import random
ironman_quotes = [
    "Genius, billionaire, playboy, philanthropist.",
    "Sometimes you gotta run before you can walk.",
    "I am Iron Man.",
    "I prefer the weapon you only have to fire once.",
    "I'm a huge fan of the way you lose control and turn into an enormous green rage monster.",
    "Jarvis, sometimes you gotta run before you can walk.",
    "I'm Tony Stark. I build neat stuff, got a great girl, and occasionally save the world. So why can't I sleep?",
]

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Error: Division by zero!"

print("--------------------------------------------------")
print("Welcome to the Iron Man Calculator!")
print("--------------------------------------------------")

while True:
    print("\nIron Man Quote: ", random.choice(ironman_quotes))
    print("\nSelect operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Exit")

    choice = input("Enter your choice (1/2/3/4/5): ")

    if choice == '5':
        print("Exiting Iron Man Calculator. Goodbye!")
        break

    if choice in ['1', '2', '3', '4']:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))

        if choice == '1':
            print("Iron Man says:", num1, "+", num2, "=", add(num1, num2))
        elif choice == '2':
            print("Iron Man says:", num1, "-", num2, "=", subtract(num1, num2))
        elif choice == '3':
            print("Iron Man says:", num1, "*", num2, "=", multiply(num1, num2))
        else:
            print("Iron Man says:", num1, "/", num2, "=", divide(num1, num2))
    else:
        print("Invalid input. Please enter a valid choice (1/2/3/4/5).")
