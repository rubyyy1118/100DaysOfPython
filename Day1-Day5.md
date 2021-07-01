```python
#Day1 band name generator
#https://band-name-generator-end.appbrewery.repl.run/

print("Welcome to the Band Name Generator!")
city = input("What's name of the city you grew up in?\n")
pet = input("What's your pet's name?\n")
print("Your band name is: "+city+" "+pet)
```

    Welcome to the Band Name Generator!
    What's name of the city you grew up in?
    Taipei
    What's your pet's name?
    Haru
    Your band name is: Taipei Haru
    


```python
#Day2 Your Life in Weeks 
#https://replit.com/@appbrewery/day-2-3-exercise#README.md

age = input("What is your current age?\n")

year = 90 - int(age)
age_d = int(year)*365
age_w = int(year)*52
age_m = int(year)*12

print(f"You have {age_d} days, {age_w} weeks, and {age_m} months left.")
```

    What is your current age?
    22
    You have 24820 days, 3536 weeks, and 816 months left.
    


```python
#Day2 Tip Calculator
#If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60

print("Welcome to the tip calculator.")
dollar =float(input("what was the total bill? $"))
tip = int(input("What percentage tip would you like to give? 10, 12, or 15? "))
people = int(input("How many people to split the bill?"))
split = round(dollar/people*(1+tip/100),2)
print(f"Each person should pay: ${split}")
```

    Welcome to the tip calculator.
    what was the total bill? $100
    What percentage tip would you like to give? 10, 12, or 15? 10
    How many people to split the bill?2
    Each person should pay: $55.0
    


```python
#Day3 BMI Calculator 2.0
#https://replit.com/@appbrewery/day-3-2-exercise#README.md


height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
bmi = weight/(height**2)

if bmi <= 18.5:
  print(f"Your BMI is {round(bmi)} , you are underweight.")
elif 18.5 <= bmi < 25:
  print(f"Your BMI is {round(bmi)} , you are a normal weight.")
elif 25<= bmi < 30:
  print(f"Your BMI is {round(bmi)} , you are slightly overweight.")
elif 30 <= bmi <35:
  print(f"Your BMI is {round(bmi)} , you are obese.")
else:
  print(f"Your BMI is {round(bmi)} , you are clinically obese.")
```

    enter your height in m: 1.6
    enter your weight in kg: 55
    Your BMI is 21 , you are a normal weight.
    


```python
#Day3 Leap Year Calculation

year = int(input("Which year do you want to check? "))

if year % 4 == 0 :
  if year % 100 == 0:
    if year % 400 == 0:
      print ("Leap year.")
    else:
      print("Not leap year.") 
  else:
    print("Leap year.")
else:
  print("Not leap year.")
```

    Which year do you want to check? 2020
    Leap year.
    


```python
#Day3 Love Calculator
#https://replit.com/@appbrewery/day-3-5-exercise#README.md

print("Welcome to the Love Calculator!")

name1 = input("What is your name? \n")
name2 = input("What is their name? \n")

combined_string = name1 + name2

combined_string_lower= combined_string.lower()

count_T = combined_string_lower.count("t")
count_R = combined_string_lower.count("r")
count_U = combined_string_lower.count("u")
count_E = combined_string_lower.count("e")

count_L = combined_string_lower.count("l")
count_O = combined_string_lower.count("o")
count_V = combined_string_lower.count("v")
count_E_1 = combined_string_lower.count("e")

total_TRUE = count_T + count_R + count_U + count_E
total_LOVE = count_L + count_O + count_V + count_E_1

Love_Score0 = str(total_TRUE) + str(total_LOVE)

Love_Score = int(Love_Score0)

if Love_Score < 10 or Love_Score > 90:
  print(f"Your score is {Love_Score}, you go together like coke and mentos.")
elif 40 <= Love_Score <= 50:
  print(f"Your score is {Love_Score}, you are alright together.")
else:
  print(f"Your score is {Love_Score}.")
```

    Welcome to the Love Calculator!
    What is your name? 
    Ruby
    What is their name? 
    Allen
    Your score is 33.
    


```python
#Day3 Treasure Island

print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 


direction = input('You\'re at a cross road. Where do you want to go? Type "left" or "right"\n').lower() #大小寫支援
if direction == "left":
  behavior = input('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.\n').lower() #大小寫支援
  if behavior == "wait":
    color = input('You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?\n').lower() #大小寫支援
    if color == "yellow":
      print("You found the treasure! You win!!!")
    elif color == "blue":
      print("You enter a room of beasts. Game Over.")
    else:
      print("Game Over!!!!!!")
  else:
    print("You got attacked by trout. Game Over.")
else:
  print("You fell into a whole. Game Over.")
```

    
    *******************************************************************************
              |                   |                  |                     |
     _________|________________.=""_;=.______________|_____________________|_______
    |                   |  ,-"_,=""     `"=.|                  |
    |___________________|__"=._o`"-._        `"=.______________|___________________
              |                `"=._o`"=._      _`"=._                     |
     _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
    |                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
    |___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
              |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
     _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
    |                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
    |___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
    ____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
    /______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
    ____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
    /______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
    ____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
    /______/______/______/______/______/______/______/______/______/______/_____ /
    *******************************************************************************
    
    Welcome to Treasure Island.
    Your mission is to find the treasure.
    You're at a cross road. Where do you want to go? Type "left" or "right"
    left
    You've come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.
    wait
    You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?
    yellow
    You found the treasure! You win!!!
    


```python
#Day4 Treasure Map
#https://replit.com/@appbrewery/day-4-3-exercise#README.md

row1 = ["⬜️","⬜️","⬜️"]
row2 = ["⬜️","⬜️","⬜️"]
row3 = ["⬜️","⬜️","⬜️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")

column = int(position[0])
row = int(position[1])

selected_row = map[row - 1]
selected_row[column - 1] = "X"
#or you can do like this
#map[column-1][row-1] = "X"

print(f"{row1}\n{row2}\n{row3}")
```

    ['⬜️', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    Where do you want to put the treasure? 23
    ['⬜️', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    ['⬜️', 'X', '⬜️']
    


```python
#Day4 Rock-Paper-Scissors

number = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

if number == 0:
  print(rock)
elif number == 1:
  print(paper)
elif number ==2:
  print(scissors)
else:
  print("You typed an invalid number ,you lose!")
print("Computer chose:")
import random
computer = random.randint(0,2)
if computer == 0:
  print(rock)
elif computer == 1:
  print(paper)
else:
  print(scissors)

if number == 0:
  if computer == 1:
    print("You lose.")
  if computer == 2:
    print("You win.")
  elif computer == 0 :
    print("It's a draw.")

if number == 1:
  if computer == 2:
    print("You lose.")
  if computer == 0:
    print("You win.")
  elif computer == 1 :
    print("It's a draw.")


if number == 2:
  if computer == 0:
    print("You lose.")
  if computer == 1:
    print("You win.")
  elif computer == 2:
    print("It's a draw.")
```

    What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.
    1
    
        _______
    ---'   ____)____
              ______)
              _______)
             _______)
    ---.__________)
    
    Computer chose:
    
        _______
    ---'   ____)
          (_____)
          (_____)
          (____)
    ---.__(___)
    
    You win.
    


```python
#Day5 Password Generator

#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
# password = ""
# for character in range(1, nr_letters+1):
#   password += random.choice(letters)
# for number in range(1,nr_numbers+1):
#   password += random.choice(numbers)
# for symbol in range (1,nr_symbols+1):
#   password += random.choice(symbols)

# print("Here is your password: " + password)

#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
password_list = []
for character in range(1, nr_letters+1):
  password_list.append(random.choice(letters))
for number in range(1,nr_numbers+1):
  password_list.append(random.choice(numbers))
for symbol in range (1,nr_symbols+1):
  password_list.append(random.choice(symbols))

random.shuffle(password_list)

password = ""
for char in password_list:
  password += char

print("Here is your password: " + password)



```

    Welcome to the PyPassword Generator!
    How many letters would you like in your password?
    2
    How many symbols would you like?
    3
    How many numbers would you like?
    4
    Here is your password: 8&4*h7)D3
    
