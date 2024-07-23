# codsoft_taskno.3
new repo
import random

def determine_winner(player_choice, computer_choice):
    # Determine the winner based on the choices
    if player_choice == computer_choice:
        return "It's a tie!"
    elif (player_choice == 'rock' and computer_choice == 'scissors') or \
         (player_choice == 'paper' and computer_choice == 'rock') or \
         (player_choice == 'scissors' and computer_choice == 'paper'):
        return "You win!"
    else:
        return "Computer wins!"

def main():
    choices = ['rock', 'paper', 'scissors']

    print("Welcome to Rock, Paper, Scissors!")
    print("Available choices: rock, paper, scissors")

    while True:
        # Player's choice
        player_choice = input("Enter your choice: ").lower()
        if player_choice not in choices:
            print("Invalid choice! Please enter rock, paper, or scissors.")
            continue
        
        # Computer's choice
        computer_choice = random.choice(choices)
        print("Computer chooses:", computer_choice)

        # Determine and print the winner
        result = determine_winner(player_choice, computer_choice)
        print(result)

        # Ask if the player wants to play again
        play_again = input("Do you want to play again? (yes/no): ").lower()
        if play_again != 'yes':
            print("Thanks for playing!")
            break

if __name__ == "__main__":
    main()
