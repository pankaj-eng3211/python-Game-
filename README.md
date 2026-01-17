# python-Game-
A  simple Python console game where the computer randomly selects a number between 1 and 100, and the player tries to guess it. The game provides hints like "Too high" or "Too low" until the correct number is guessed. It also tracks the number of attempts taken.
import random

print("🎮 Welcome to Number Guessing Game!")
print("I have chosen a number between 1 and 100.")

# Generate random number
secret_number = random.randint(1, 100)
attempts = 0

while True:
    guess = int(input("Enter your guess: "))
    attempts += 1
    
    if guess < secret_number:
        print("Too low! Try again.")
    elif guess > secret_number:
        print("Too high! Try again.")
    else:
        print(f"🎉 Correct! The number was {secret_number}.")
        print(f"You guessed it in {attempts} attempts.")
        break

