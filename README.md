# Text-Based-Game-Using-Python-Packages-Flask
Text Based Game
Group - 4
https://replit.com/@GeoHan1/A-Quiet-Weekend-v22
Contents:
1.	Introduction
1.1.	Storyboard
1.1.1.	Streamline-project
2.	Design Documentation
2.1.	Structure
2.2.	Flowchart
3.	Testing
3.1.	Error handling techniques
3.2.	Run through Debug mode
4.	Evaluation
4.1.	Formative
4.2.	Summative
5.	Reflection
6.	Code


Introduction:
1.1 Story board:
Let me begin with a lovely quote:
This morning,
I woke up to the sounds of the birds singing,
Giving us their morning song that they love.
I look out through the open window to feel the breeze, 
The wind dances everywhere as the sun rises. 
It’ll be a beautiful day, because God made it this way.

![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/0626f085-af6c-4a3b-99a8-c4e41ff4c0fa)







1.1.1.	Streamline- Project
George narrated a story to our project storyline which is a Text-Based-Game-Project
You hear songbirds outside cheerfully chirping in morning song as the golden light graciously paints the room.
Thank God it's a Saturday", you smirk, as you turn to your side and close your eyes just as slowly as you'd opened them.
...Ten minutes pass
You wake up suddenly...
Wake up! I'll be out today and it's your turn to babysit!
You sense by an overwhelming feeling of dread and realization in equal measure, as you remember that peace and quiet is a thing of the past.
"Well?"
"Alright, Dear."
Accepting defeat, you get up and make your way to the living room...'
You see Bob Junior slouched on the sofa, flicking through the TV channels.
He almost seems to be falling asleep himself, just as you were a few minutes ago.
"I'm bored!" he proclaimed out loud.
"Why not play some games?" I suggest.
"OK."
"What do you want to play?
Now Bob chooses his choice of games to play as he wishes to have a wonderful and quiet weekend.
![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/e5d39902-c2bb-4a58-a07e-f88728186f85)

2.	Design Documentation
2.1.	Structure of project:
Our objective is to create different minigames like Quiz, Puzzle games, Dice games. So, we create a Packages of modules imported in a main python file and entry code run fast and Packages are an essential building block in programming. 
Why do we use packages?
Without packages, imagine having to write code from scratch every time you wanted to parse a file in a particular format. You would never get anything done! That’s why we always want to use packages.

![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/3a6f8bea-853b-4733-b332-e2637495a23a)





2.2.	Flowchart-Project:



![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/471fb5f5-eefa-4468-bbc1-c87a7c9a3f2b)








3.	Testing
3.1.	Error handling Techniques:
As it is Text-Based-Project our group we added Try and except statements, which are used to catch and handle exceptions in Python. Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause.
For example, dice_game.py
while True:
    try:
        number_input = int(input("Type an integer between 1 and 10: "))
        if(number_input > 0 and number_input < 10):
            break
        else:
            print("Invalid input. Try again.")

    except:
        print("Please provide an Integer")
3.2.	Run through the debug mode:
We can test the code by clicking the code line and clicking the Debug mode button, it checks the code to see what’s happening inside the for loop by pressing some alt+shift+F7 or F7 into the code.
For example,

4.	Evaluation
4.1.	Formative:
In our project, we checked multiple times of evaluation while running a code especially gaming programs to identify the problems. 
For example, Minesweeper.py
I run function check_mines to check the iterations are correctly placed in their respective row column of a 3*3 matrix.
def check_mines(row, col):
    t = 0       #total mines around spot
    i = row-1
    while i <= row+1:
        if i>=0 and i< 3:
            j = col-1
            while j <= col + 1:
                if j>=0 and j<3:
                    t = t+board[i][j]
                j = j+1
        i = i+1
    return t

4.2.	Summative:
Summation evaluation evaluates the objectives and overall text-based-game. In our project, main.py imports the minigames modules and runs the program without flaws.
We use imported Flask app in our python project through webserver.
  ![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/8e531a5e-aa49-4e39-a470-6b2b62a65af3)






5.	Reflections:
About the project, Text-based-game-group package which includes Minigames-Modules, main.py and __inti__.py. George and I have done testing using error handling techniques to run the code smoothly in the main.py. We added some choices of different gaming list that the boy can play. George added interesting storylines and code looks wells. George shared his idea of importing flask app in Text-based-project python file to create a webpage through HTML. We raised some web-server error, and the response is not clear. I tried some java script techniques, but it didn’t work well. We decided to integrate our project this flask with webserver without response HTML in Replit.

6.	Code: (Appendix A)

![image](https://github.com/SasiLeburi/Text-Based-Game-Using-Python-Packages-Flask/assets/142025947/39cada90-8f3f-4c76-98a0-1bd2d0fc75c3)














# main.py (This is the main file from which the game can be played. It runs code from the module files located at 'Minigames_Module')

import Minigames_Module.tic_tac_toe as ttt
import Minigames_Module.dictionaries_capitals_quiz as quiz
import Minigames_Module.dice_game as dice
import Minigames_Module.minesweeper3_3 as mine
#import replit
from flask import Flask, render_template, request

app = Flask(__name__)

"""

A Quiet Weekend: A Text-Based Game with Mini-Games

"""

# CHAPTER_0: TITLE
Chapter_0 = r'''         ⁺˚⋆｡ °✩₊                 *        ⁺˚⋆｡ °✩₊         *
                     __________________________________
   ⁺˚⋆｡ °✩₊        / \                                  \           *                *
                  |   |     Group 4 proudly presents    |
           *       \_ |                                 |
                      |         A QUIET WEEKEND:        |      *        
                      |        A text-based game        |                 ⁺˚⋆｡ °✩₊
       *              |                                 |
                   ⁺˚⋆|     ~~~~~~~~~~~~~~~~~~~~~~~~    |
                      |                                 |                *
                      |                                 |                              *
                      |                                 |⋆｡ °✩₊                      
   ⁺˚⋆｡ °✩₊           | ________________________________|_
                      | \                                  \
             ⁺˚⋆｡ °✩₊ |  |                                  |          ⁺˚⋆｡ °✩₊
      *               \_/__________________________________/
                                                  ⁺˚⋆｡ °✩₊                                *
                              *
____________________________________________________________________________________________
'''

# CHAPTER 1: INTRODUCTION
Chapter_1 = str(
  '____________________________________________________________________________________________\n'
  'You hear songbirds outside cheerfully chirping in morning song as golden beams of \nspring sunshine paint the room.\n'
  '\"Thank God it\'s a Saturday\", you smirk, as you turn to your side and close your eyes \njust as slowly as you\'d'
  ' opened them.\n\n'
  '...Ten minutes pass\n'
  'You wake up suddenly...\n\n'
  '\"Wake up! I\'ll be out today and it\'s your turn to babysit!\"\n'
  'You sense an overwhelming feeling of dread and realisation in equal measure,\n'
  'as you remember that peace and quiet is a thing of the past.\n\n'
  '\"Well?\"\n'
  '\"Alright, Dear.\"\n\n'
  'Accepting defeat, you get up and make your way to the living room...\n'
  '____________________________________________________________________________________________\n'
)

# CHAPTER 2: LET THE GAMES BEGIN!
Chapter_2 = str(
  '____________________________________________________________________________________________\n'
  'You see Bob Junior slouched on the sofa, flicking through the TV channels.\n'
  'He almost seems to be falling asleep himself, just as you were a few minutes ago.\n'
  '\"I\'m bored!\" he proclaims loudly.\n'
  '\"Why not play some games?\" I suggest.\n'
  '\"OK.\"\n'
  '\"What do you want to play?\"\n'
  '____________________________________________________________________________________________\n'
)

# CHAPTER 3: BOREDOM STRIKES AGAIN
Chapter_3 = str(
  '____________________________________________________________________________________________\n'
  'Bob Junior\'s smile has started to fade\n'
  '\"I\'m getting bored again. Can we play something else?\"\n'
  '____________________________________________________________________________________________\n'
)


# Post-game dialogue function
def change_game():
  text = input('\nPress the ENTER key on your keyboard to continue...')
  if text == '':
    print(Chapter_3)
  else:
    print('Please only press the ENTER key. Try again.')


# Function to direct players towards their selected mini-game from their respective modules which contain
# a __main__ function, using the main() call. A number from 1-4 must be selected, else the player is
# redirected to choose again.
def game_selection_prompt():
  while True:
    try:
      #replit.clear()
      user_input = int(
        input('Please select a game to play:\n\n'
              '1 - Tic-Tac-Toe\n'
              '2 - Quiz\n'
              '3 - Dice \n'
              '4 - Minesweeper\n'
              'Your Choice: '))
      if user_input == 1:
        #replit.clear()
        print('\n\"Let\'s play Tic-Tac-Toe!\"\n')
        print(
          '____________________________________________________________________________________________\n'
        )
        print(
          '\nYou hurry to the nearby table to grab a pen and a sheet of paper.\n'
        )
        print(
          '____________________________________________________________________________________________\n'
        )
        ttt.main()
        change_game()
      elif user_input == 2:
        #replit.clear()
        print('\n\"Let\'s have a quiz!\"\n')
        print(
          '____________________________________________________________________________________________\n'
        )
        print(
          '\nYou pause for a minute as you try to recall the questions and answers '
          'to the last pub quiz \nthat you went to.\n')
        print(
          '____________________________________________________________________________________________\n'
        )
        quiz.main()
      elif user_input == 3:
        #replit.clear()
        print('\n\"Let\'s roll dice!\"\n')
        print(
          '____________________________________________________________________________________________\n'
        )
        print(
          '\nAfter searching for a few minutes, you find the dice between the sofa cushions, \nalongside some change and some chewing gum.\n'
        )
        print(
          '____________________________________________________________________________________________\n'
        )
        dice.main()
        change_game()
      elif user_input == 4:
        #replit.clear()
        print('\n\"Let\'s play Minesweeper!\"\n')
        print(
          '____________________________________________________________________________________________\n'
        )
        print(
          '\nDespite tiredly mistyping your password twice, \nyou finally manage to boot up your laptop and launch Minesweeper.\n'
        )
        print(
          '____________________________________________________________________________________________\n'
        )
        print('\n\"Alert! You must avoid hitting the mines...!\"\n')
        mine.main()
        change_game()
      elif user_input != range(1, 4):
        replit.clear()
        print('\nPlease type a whole number between 1 and 4!\n')
        game_selection_prompt()
        break

    except ValueError:
      print('\nYou have not typed a number.\n')
      play_again = input("\nWould you like take a break? (Y/N)").upper()
      if play_again == "N":
        game_selection_prompt()
        continue
      else:
        play_game()
        continue


# The following are functions that are called upon later; they switch between the dialogue chapters.
def next_chapter_1():
  text = input()
  if text == '':
    print(Chapter_1)
  else:
    print('Please only press the ENTER key. Try again.')
    next_chapter_1()


def next_chapter_2():
  text = input('Press the ENTER key on your keyboard to continue...')
  if text == '':
    print(Chapter_2)
  else:
    print('Please only press the ENTER key. Try again.')
    next_chapter_2()


def next_chapter_gsp():
  text = input('Press the ENTER key on your keyboard to continue...')
  print(
    '____________________________________________________________________________________________'
  )
  if text == '':
    game_selection_prompt()
  else:
    print('Please only press the ENTER key. Try again.')
    game_selection_prompt()


# Python decorator to connect URL endpoints with code contained in functions:
@app.route('/PlayGame', methods=['POST', 'GET'])
def play_game():
  #replit.clear()
  print(Chapter_0)
  print('Press the ENTER key on your keyboard to continue...')
  next_chapter_1()
  next_chapter_2()
  next_chapter_gsp()
  return

play_game()

# Defining the index.html as what should be executed if the URL endpoint is requested by a user:
@app.route('/')
def index():
  return render_template('index.html')


if __name__ == '__main__':
  app.run(host='0.0.0.0', port=8080)

Minigames_Modules
		Tic_tac_toe.py
import emoji


def main(args=None):

  class Board:

    def __init__(self):
      self.cells = [" ", " ", " ", " ", " ", " ", " ", " ", " ", " "]

    def display(self):
      print(" %s | %s | %s " % (self.cells[1], self.cells[2], self.cells[3]))
      print("___________")
      print(" %s | %s | %s " % (self.cells[4], self.cells[5], self.cells[6]))
      print("___________")
      print(" %s | %s | %s " % (self.cells[7], self.cells[8], self.cells[9]))

    def update_cell(self, cell_no, player):
      if self.cells[cell_no] == " ":
        self.cells[cell_no] = player
      else:
        print("Cell already filled")
      refresh_screen()

    def is_winner(self, player):
      if self.cells[1] == player and self.cells[2] == player and self.cells[
          3] == player:
        return True
      if self.cells[4] == player and self.cells[5] == player and self.cells[
          6] == player:
        return True
      if self.cells[7] == player and self.cells[8] == player and self.cells[
          9] == player:
        return True
      if self.cells[1] == player and self.cells[5] == player and self.cells[
          9] == player:
        return True
      if self.cells[3] == player and self.cells[5] == player and self.cells[
          7] == player:
        return True
      if self.cells[1] == player and self.cells[4] == player and self.cells[
          7] == player:
        return True
      if self.cells[2] == player and self.cells[5] == player and self.cells[
          8] == player:
        return True
      if self.cells[3] == player and self.cells[6] == player and self.cells[
          9] == player:
        return True

    def reset(self):
      self.cells = ["", "", "", "", "", "", "", "", "", ""]

    def is_tie(self):
      used_cells = 0
      for cell in self.cells:
        if cell != " ":
          used_cells += 1
      if used_cells == 9:
        return True
      else:
        return False

  board = Board()

  def print_header():
    print("Welcome to tic-tac-toe\n")
    print("Board data Structure\n")
    print(" 1 | 2 | 3")
    print("___________")
    print(" 4 | 5 | 6")
    print("___________")
    print(" 7 | 8 | 9")

  def refresh_screen():
    #show the board
    board.display()
    
    
  print_header()

  
  while True:
    
    #get X input
    x_choice = int(input("\nPLAYER 1 (X)\nPlease choose a number between 1-9: "))
      
    #update board
    board.update_cell(x_choice, "X")
    # check for X win
    if board.is_winner("X"):
      print("\nPLAYER 1 (X) WINS!\n")
      print(emoji.emojize(":grinning_face_with_big_eyes:"))
      play_again = input("Would like to play again? (Y/N)").upper()
      if play_again == "Y":
        board.reset()
        continue
      else:
        break
    
    #get O input
    o_choice = int(input("\nPLAYER 2 (O)\nPlease choose a number between 1-9: "))

    #update board
    board.update_cell(o_choice, "O")
    # check for O win
    if board.is_winner("O"):
      print("\nPLAYER 2 (O) WINS!\n")
      print(emoji.emojize(":grinning_face_with_big_eyes:"))
      play_again = input("Would like to play again? (Y/N)").upper()
      if play_again == "Y":
        board.reset()
        continue
      else:
        break

  # check for a tie
    if board.is_tie():
      print("\nTie game\n")
      play_again = input("Would like to play again? (Y/N)").upper()
      if play_again == "Y":
        board.reset()
        continue
      else:
        break


if __name__ == '__main__':
  main()

dice_game.py
# dice.py
import random


def main(args=None):
  print("Welcome to the dice!")
  print("-------------------------------------------------")
  print("How many dice would you like to roll? \n")
  # add validate input
  while True:
    try:
      number_input = int(input("Type a number between 1 and 10: "))
      if (number_input > 0 and number_input <= 10):
        break
      else:
        print("Invalid input. Try again.")

    except:
      print("Please provide an integer")

  
  def rollDice(dice_input):
    totalSum = 0
    possible_facts = [1, 2, 3, 4, 5, 6]
    for die in range(dice_input):
      roll = random.choice(possible_facts)
      print("Die ", die + 1, ": ", roll)
      totalSum += roll
    average = int(totalSum / dice_input)
    print("Total Sum ", totalSum)
    print("Average roll: ", round(average))
    return totalSum


  # To make the game a two-player game:
  num_players = 2
  scores = [0] * num_players
  for player in range(num_players):
    if player == 1:
      while True:
        next_roll = input('\nPress ENTER for the next player to roll the dice!')
        if next_roll == '':
          break
    print(f'\nPLAYER {player + 1}\'s turn:')
    scores[player] = rollDice(number_input)

  # To determine the winner:
  winner = scores.index(max(scores)) + 1
  print('\n\n')
  print(f'PLAYER {winner} WINS!')
  


if __name__ == '__main__':
  main()
  

dictionaries_capitals_quiz.py
#!/usr/bin/env python
# coding: utf-8

# In[21]:

#Must type in answer exactly as it appears in the dictionary

import random
import time
import emoji


def main(args=None):
  dictionary = {  #dictionary/key/value pairs for definitions
    "Afghanistan": "Kabul",
    "Australia": "Canberra",
    "Belarus": "Minsk",
    "England": "London",
    "Chile": "Santiago",
    "Sweden": "Stockholm"
  }

  print("Capitals Quiz. What is the Capital City...?")
  print("_" * 39, "\n")

  answer = input("Play game? ('Y' to continue) ")

  print(" ")

  while answer == "y":

    keywords = list(dictionary.keys())  #turns words into a list

    random.shuffle(keywords)  #shuffle keywords
    correct = 0
    wrong = 0
    for keyword in keywords:
      display = "{}"
      print("\n", display.format(keyword))
      user_answer = input("Your answer: ").capitalize()
      time.sleep(1)
      print("Correct answer:", dictionary[keyword])
      print(" ")

      if user_answer == (dictionary[keyword]):
        print("CORRECT")
        print(emoji.emojize(":grinning_face_with_big_eyes:"))
        correct += 1
      else:
        print("WRONG")
        print("\N{pensive face}")
        wrong += 1
      print('_' * 25)  #line separator

    # final score
    display_score = "SCORE: {} correct and {} wrong"
    print(display_score.format(correct, wrong))
    answer = input("Play again? ('Y' to continue) ")
  print(" ")
  print("Thanks for playing")

  # In[ ]:

  # In[ ]:


if __name__ == '__main__':
  main()

minesweeper3_3.py
#board user can NOT see (solution)
import random
import emoji


# Resets the board in case Minesweeper is chosen to be played again
def reset_board():
  global board
  global boardDisplay
  board = [
  [0, 0, 0],  # 0=no bomb
  [0, 0, 0],  #1=bomb
  [0, 0, 0]
  ]
#board user can see
  boardDisplay = [
  [-1, -1, -1],  #-1=Unknown
  [-1, -1, -1],
  [-1, -1, -1]
  ]

reset_board()

def main(args=None):
  def check_mines(row, col):
    t = 0  #total mines around spot
    i = row - 1
    while i <= row + 1:
      if i >= 0 and i < 3:
        j = col - 1
        while j <= col + 1:
          if j >= 0 and j < 3:
            t = t + board[i][j]
          j = j + 1
      i = i + 1
    return t

    # add mines

  numMines = int(input("How many mines in the field?"))
  num = 0  # num mines
  while num < numMines:
    row = random.randint(0, 2)
    col = random.randint(0, 2)
    if board[row][col] == 0:
      board[row][col] = 1  # add mine
      num = num + 1

  def display_solution():
    for row in range(0, 3):
      for col in range(0, 3):
        print(board[row][col], end=" ")
      print("")

  def display_board():
    print("-" * 10)
    for row in range(0, 3):
      print("| ", end="")
      for col in range(0, 3):
        if boardDisplay[row][col] == -1:
          print(" ", end="| ")
        else:
          print(board[row][col], end="|")
      print(" ")
      print("-" * 10)

  #display_solution()
  display_board()

  guess = 0
  while True:
    try:
      if guess < (9 - numMines):
        row = int(input("Guess a row (1-3): ")) - 1
        col = int(input("Guess a col (1-3): ")) - 1
        if board[row][col] == 1:
          print("BOOOMmmm!!!  You hit a mine.")
          print("\N{face with head-bandage}")
        else:
          boardDisplay[row][col] = check_mines(row, col)
          display_board()
          print(emoji.emojize(":grinning_face_with_big_eyes:"))
        guess = guess + 1
      else:
        print("You are out of guesses")
        display_solution()
        reset_board()
        break
    except:
      print("Enter a guess within range")


if __name__ == '__main__':
  try:
    main()
  except KeyboardInterrupt:
    print('\nEnd of Game. Bye Bye!')
