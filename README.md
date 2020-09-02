# hello-world
learning python and github

import random

#function to shuffle all the characters of a string
def shuffle(string):
  tempList = list(string)
  random.shuffle(tempList)
  return ''.join(tempList)
 
#Main 
uppercaseLetter1=chr(random.randint(65,90)) #Generate a random Uppercase letter  ASCII code
uppercaseLetter2=chr(random.randint(65,90)) #Generate a random Uppercase letter  ASCII code


lowercaseLetter1=chr(random.randint(97,122))
lowercaseLetter2=chr(random.randint(97,122))

digit1=chr(random.randint(48,57))
digit2=chr(random.randint(48,57))

punctuationSign1=chr(random.randint(32,152))
punctuationSign2=chr(random.randint(32,152))


password = uppercaseLetter1 + uppercaseLetter2 +lowercaseLetter1+lowercaseLetter2+digit1+digit2+punctuationSign1+punctuationSign2
password = shuffle(password)

#Ouput
print("Random password generated:",password)










from random import randint

#create list of play options
t = ["Rock","Paper","Scissors"]

#assign a random play to the computer
computer = t[randint(0,2)]

#set player to False
player=False

while player==False:
#set player to True
    player=input("Rock, Paper, Scissors?")
    if player == computer:
        print("Tie!")
    elif player == "Rock":
        if computer == "Paper":
            print("You lose!",computer,"covers",player)
        else:
            print("You win!",player,"smashes",computer)
    elif player == "Paper":
        if computer == "Scissors":
            print("You lose!",computer,"cut",player)
        else:
            print("You win!",player,"covers",computer)
    elif player == "Scissors":
        if computer == "Rock":
            print("You lose!",computer,"smashes",player)
        else:
            print("You win!",player,"cut",computer)
    else:
        print("That is not a valid play. Check your spelling!") 
    player = False
    computer=t[randint(0,2)]
