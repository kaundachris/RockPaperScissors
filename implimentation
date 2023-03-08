import random


class RockPaperScissors:
    choices = ['rock', 'paper', 'scissors']

    def __init__(self, best_of: int):
        self.best_of = best_of
        self.player_wins = 0
        self.computer_wins = 0
        self.num_rounds = 0

    def rounds(self):
        while self.num_rounds < self.best_of:
            user_input = input('pick between rock, paper or scissors: ').lower()
            while user_input not in self.choices:
                user_input = input('pick between rock, paper or scissors: ').lower()
            computer_choice = random.choice(self.choices)
            print(computer_choice)
            if user_input == 'scissors' and computer_choice == 'paper':
                print('Scissors cut paper. Player wins the round')
                self.player_wins += 1
            elif user_input == 'paper' and computer_choice == 'rock':
                print('Paper covers rock. Player wins the round')
                self.player_wins += 1
            elif user_input == 'rock' and computer_choice == 'scissors':
                print('Rock crushes scissors. Player wins the round')
                self.player_wins += 1
            elif user_input == computer_choice:
                print("That's a draw")
            else:
                print(f'{computer_choice} trumps {user_input}. Computer wins the round')
                self.computer_wins += 1
            self.num_rounds += 1

    def winner(self):
        self.rounds()
        if self.player_wins > self.computer_wins:
            message = 'Player wins the game'
        elif self.player_wins < self.computer_wins:
            message = 'Computer wins the game'
        else:
            message = 'The game ends in a draw'
        return message
