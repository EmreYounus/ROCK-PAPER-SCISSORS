# ROCK-PAPER-SCISSORS
A simple, first to three, Rock, Paper, Scissors game created in Python 

# This line hides the user's input prompt
from getpass import getpass as input

print("ROCK, PAPER, SCISSORS ")
print()
print("Select your move (R, P or S)")
print()

# Create these variables outside loop and then add += with correct player to keep score throughout
Player1_Score = 0
Player2_Score = 0

# initialise the round counter
round_counter = 1 

# The while loop needs to go around all code 
while True:
  print (f"ROUND {round_counter}")

  print()
  player_1 = input("Player 1 > ")
  print()
  player_2 = input("Player 2 > ")
  print()
  
  if(player_1 == "R"):
    if(player_2 == "R"):
      print("You both picked Rock, draw!")
    elif(player_2=="S"):
      print("Player 1 smashed Player 2's Scissors into dust with their Rock!")
      Player1_Score += 1
    elif(player_2 == "P"):
      print("Player 1's Rock is smothered by Player 2's Paper!")
      Player2_Score += 1
  elif(player_1 == "P"):
    if(player_2 == "R"):
      print("Player 2's Rock is smothered by Player 1's Paper!")
      Player1_Score += 1
    elif(player_2 == "S"):
      print("Player 1's Paper is cut into tiny pieces by Player 2's Scissors!")
      Player2_Score += 1
    elif(player_2 == "P"):
      print("Two bits of paper flap at each other. Dissapointing. Draw.")
  elif(player_1 == "S"):
    if(player_2 == "R"):
      print("Player 2's Rock makes metal-dust out of Player 1's Scissors")
      Player2_Score += 1
    elif(player_2 == "S"):
      print("Ka-Shing! Scissors bounce off each other like a dodgy sword fight! Draw.")
    elif(player_2 == "P"):
      print("Player 1's Scissors make confetti out of Player 2's paper!")
      Player1_Score += 1
  
# Make sure to add player scores at the end of all the options but still inside the while loop.
  print ()
  print("Player 1 has", Player1_Score, "wins.")
  print("Player 2 has", Player2_Score, "wins.")

  print ()
  if Player1_Score == 3 or Player2_Score == 3:
    print("Thanks for playing!")
    exit()
  else:
    print()
    round_counter += 1 # increment the round counter
