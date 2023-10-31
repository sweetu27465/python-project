# python-project
import random
def start_game():
    print("Welcome to the Text-Based Adventure Game!")
    print("You find yourself in a dark forest with two paths ahead.")
    while True:
        print("\nChoose your path:")
        print("1. Go left into a cave.")
        print("2. Go right towards a mysterious mansion.")
        print("3. Quit")
        choice = input("Enter your choice: ")
        if choice == "1":
            cave_path()
        elif choice == "2":
            mansion_path()
        elif choice == "3":
            print("Thanks for playing!")
            break
        else:
            print("Invalid choice. Please select a valid option.")
def cave_path():
    print("You enter the cave and discover a hidden treasure chest!")
    outcome = random.choice(["You found a valuable gem!", "The cave is collapsing! You barely escape."])
    print(outcome)
def mansion_path():
    print("You approach the mansion, but it looks abandoned. Do you want to enter?")
    while True:
        print("1. Enter the mansion.")
        print("2. Turn back.")
        choice = input("Enter your choice: ")
        if choice == "1":
            mansion_interior()
        elif choice == "2":
            print("You decide to turn back.")
            break
        else:
            print("Invalid choice. Please select a valid option.")
def mansion_interior():
    print("Inside the mansion, you encounter a ghost. You must make a choice!")
    print("1. Converse with the ghost.")
    print("2. Run away.")
    choice = input("Enter your choice: ")

    if choice == "1":
        print("The ghost reveals a secret and guides you to safety. You've won the game!")
    elif choice == "2":
        print("You flee from the mansion, narrowly escaping the ghost. You survive.")
    else:
        print("Invalid choice. Please select a valid option.")
start_game()
