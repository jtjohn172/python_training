Learning Python with Mike Dane:   https://www.youtube.com/watch?v=rfscVS0vtbw&t=3204s 



# Working with Variables

character_name = "Tom"
character_age = "70"

print("The once was a man named " + character_name + ",")
print("He was " + character_age + " years old. ")

character_name = "Jerry"
print("He really liked the name " + character_name + ", ")
print("but didn't like being " + character_age + " .")





# Working with String

# Same line
print("Hello world")

# New Line Escape
print("Hello\nworld")

# Quotation Escape with Strings
print("Hello \"world\"")

# String Variable
phrase = "Learning to code"
print(phrase)

# Concatenation
phrase = "Learning to code"
print(phrase + " is cool.")

# Functions to modify Strings
phrase = "Learning to Code"
print(phrase.lower()) # Lowercase
print(phrase.upper()) # Uppercase
print(phrase.isupper()) # T/F value if entire string is uppercase
print(phrase.islower()) # T/F value if entire string is lowercase
print(phrase.upper().isupper()) # Changed to all uppercase and tested T/F
print(phrase.__len__()) # How many characters are in the string
print(phrase[0]) # [0] will bring back first letter in the variable "L"
print(phrase.index("r")) # tell us where a specific character is located "passing a parameter"
print(phrase.replace("Learning", "Teaching")) # Replace words in your variable





# Working with Numbers


# Random Math in Python
print(2, 2.0987, -7)
print(3 + 4.5)
print(3 * (4 + 5))


print(10 % 3) # "%" gives the remainder

# Numbers stored in Variables
my_num = 5
print(my_num)

# Change number into a String
my_num = 5
print(str(my_num) + " is my favorite number.")

# Absolute Value (abs)
my_num = -5
print(abs(my_num))

# Powers 3^2 (pow)
my_num = 5
print(pow(3, 2))

# Max & Min (returns largest/smallest of the two numbers
my_num = -5
print(max(4, 6))
print(min(4, 6))

# Round numbers
my_num = -5
print(round(3.2)) # = 3
print(round(3.5)) # = 4

from math import *      # This is a Python math function

# Floor Method (rounds down no matter whatr)
print(floor(3.7)) # = 3

# Ceil Method (rounds up no matter what)
print(ceil(3.7)) # = 4

# sqrt (square root)
print(sqrt(36)) # = 6





# Getting Input from Users!

# Hello, Jordan! You are 25
name = input("what is your name: ")
age = input("Enter your age: ")
print("Hello, " + name + "! You are " + age)





# Building a Basic Calculator

num1 = input("Enter a number: ")
num2 = input("Enter another number: ")
result = (float(num1) + float(num2))  # Must convert string #'s into actual numbers by using int() or float()

print(result)



# Building a better calculator

num1 = float(input("Enter first number: "))
op = input("Enter your operator: ")
num2 = float(input("Enter Second number: "))

if op == "+":
    print(num1 + num2)
elif op == "-":
    print(num1 - num2)
elif op == "*":
    print(num1 * num2)
elif op == "/":
    print(num1 / num2)
else:
    print("Invalid Operator")







# Madlibs Game

color1 = input("Enter a color: ")
color2 = input("Enter another color color: ")
animal = input("Enter an animal: ")


print("Roses are " + color1)
print("Violets are " + color2)
print("I love " + animal)





# Lists

friends = ["Kevin", "Karen", "Jim"]

print(friends) # = ['Kevin', 'Karen', 'Jim']
print(friends[1]) # = Karen
print(friends[2]) # = Jim
print(friends[-1]) # = Jim
print(friends[1:]) # = ['Karen', 'Jim']

friends = ["Kevin", "Karen", "Jim"]
friends[0] = "Mike" # This eliminates "kevin" and adds "mike
print(friends[0:])





# List Functions

lucky_numbers = [4, 8, 15, 16, 23, 42]
friends = ["Kevin", "Karen", "Jim", "Oscar", "Toby"]

friends.extend(lucky_numbers) # This fuction joins "lucky_numbers" to the end of the "friends" list
print(friends)

friends.append("Creed") # This will add "Creed" to the end of the "friends" list
print(friends)

friends.insert(1, "Kelly") # used to insert things into the list
print(friends)

friends.remove("Jim") # used to remove specific things from the list
print(friends)

friends.pop()  # removes the last element on the list
print(friends)



lucky_numbers = [4, 8, 15, 16, 23, 42]
friends = ["Kevin", "Karen", "Jim", "Oscar", "Toby", "Toby"]

print(friends.index("Jim")) # index tells you if there is something in the list and where
print(friends.count("Toby")) # This counts how many times data is repeated

lucky_numbers = [4, 8, 23, 15, 16, 42]
friends = ["Kevin", "Karen", "Jim", "Oscar", "Toby", "Toby"]
friends.sort() # This puts the strings in alphabetical order
lucky_numbers.sort() # This puts the numbers in numerical order
lucky_numbers.reverse() # This puts the numbers in reverse numerical order
print(friends)
print(lucky_numbers)

lucky_numbers = [4, 8, 23, 15, 16, 42]
friends = ["Kevin", "Karen", "Jim", "Oscar", "Toby", "Toby"]

friends2 = friends.copy() # this will copy the "friends" list

print(friends2)





# Tuples

# Tuples CANNOT be changed
coordinates = (4, 5)
#coordinates[1] = 10 *** This will not work
print(coordinates[1])





# Functions


def say_hi(): # name functions in lowercase and use _ to separate
    print("Hello User") # the indentation is used to structure the code

say_hi()


def say_hi(name, age): # include parameters to make the code more powerful
    print("Hello " + name + ", you are " + str(age))

say_hi("Jordan", 25)
say_hi("Steve", 60)





# Return Statements

def cube(num):
    return num*num*num # Must include "return" when doing math


print(cube(3)) # = 27

# OR

def cube(num):
    return num*num*num # Must include "return" when doing math


result = cube(4)
print(result) # = 64





# If Statements


is_male = True

if is_male:
    print("You are a male")   #This will print the statement since it is "is_male = true"


# Two variable IF program:

is_male = True
is_tall = True


if is_male and is_tall:
    print("You are a tall male") # the first statement should be "if"
elif is_male and not(is_tall):
    print("You are a short male") # body statements should be "elif"
elif not(is_male) and is_tall:
    print("you are a tall female") # body statements should be "elif"
else:
    print("You are either not male or not tall or both") # the opposite of true should be "else:" means non of the variables are true


#  Using functions in IF statements to meet conditions

def max_num(num1, num2, num3):
    if num1 >= num2 and num1 >= num3:
        return num1
    elif num2 >= num1 and num2 >= num3:
        return num2
    else:
        return num3

print(max_num(300, 40, 5)) #  =300







# Dictionaries

# This program converts 3 digit month name into the full month name

monthConversions = {  # curly brackets enclose the "Key Value Pairs"
    "Jan": "January",
    "Feb": "February",
    "Mar": "March",
    "Apr": "April",
    "May": "May",
    "Jun": "June",
    "Jul": "July",
    "Aug": "August",
    "Sep": "September",
    "Oct": "October",
    "Nov": "November",
    "Dec": "December",
}

print(monthConversions["Dec"])  # = December








# While Loop

i = 1 # set the variable
while i <= 10: # "while" function will loop forever until a condition is/isn't met
    print(i) # This will print "1"
    i += 1 # This will add "1" to every loop until the value is greeater than 10.

print("done with loop")







# Building a Guessing Game (2:20:03)

# Variables
secret_word = "giraffe"  # Secret word variable
guess = "" # Guess Variable
guess_count = 0 # Guess count, starting at 0
guess_limit = 3 # Guess limit, ending at 3 attempts
out_of_guesses = False # this interacts with "else" and as long as it is false, more guesses are availabe



while guess != secret_word and not(out_of_guesses):
 if guess_count < guess_limit:
    guess = input("Enter Guess: ")
    guess_count += 1
 else:
     out_of_guesses = True

if out_of_guesses:
    print("Out of guesses, YOU LOSE!")
else:
    print("Congrats, you guessed correct!")






# For Loop (2:32:00)

#
friends = ["Jim", "Karen", "Kevin"] # example array
for friend in friends: # *"friend" can be anything* but must be printed below the same
    print(friend)

#
for index in range(10):
    print(index) # Prints all #'s 0-9

#
for index in range(3, 10):
    print(index) # Prints all #'s between 3-10 not including 10

#
friends = ["Jim", "Karen", "Kevin"]
for index in range(len(friends)):
    print(friends[index])

#
for index in range(5):
    if index == 0:
        print("First Iteratation")
    else:
        print("Not First")




# Exponent Functions

def raise_to_power(base_num, pow_num):
    result = 1
    for index in range(pow_num):
        result  = result * base_num

    return result


print(raise_to_power(3, 4)) # 81








# 2D Lists & Nested Loops

number_grid = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
    [0]
]

#
print(number_grid[2]) # prints the 3rd row
print(number_grid[2][1]) # prints the 2nd number in the 3rd row




number_grid = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
    [0]
]

#
for row in number_grid:
    for col in row:
        print(col)







# Build a Translator

def translate(phrase):
    translation = ""
    for letter in phrase:
        if letter.lower() in "aeiou":
            if letter.isupper():
                translation = translation + "G"
            else:
                translation = translation + "g"
        else:
            translation = translation + letter
    return translation



print(translate(input("Enter a Phrase: ")))








# Comments


#
or
'''
'''






# Try / Except (3:04:00)


try:
    answer = 10 / 0
    number = int(input("Enter a Number: "))
    print(number)

except ZeroDivisionError as err:
    print(err)
except ValueError:
    print("Invalid Input")







# Reading Files

open("employees.txt", "r")
open("employees.txt", "w")
open("employees.txt", "a")
open("employees.txt", "r+")


employee_file = open("employees.txt", "r")

print(employee_file.readlines()[0:])

employee_file.close()







# Writing to files

#
employee_file = open("employees.txt", "a") # "a" means append to the file.
print(employee_file.write("Toby - HR"))    # ".write" allows you to add more to the file in Python
employee_file.close()                      # Always .close when working with files in python

#
employee_file = open("employees.txt", "a")
print(employee_file.write("\nKelly - Customer Service")) # \n will append the file on a new line each time you run it
employee_file.close()

#
employee_file = open("employees1.txt", "w") # "w" for "write" a file. changing the file name to a non-existing file will create a new file!
print(employee_file.write("\nKelly - Customer Service"))
employee_file.close()

# creating an HTML file in Python
employee_file = open("index.html", "w")
print(employee_file.write("<p>This is HTML</p>"))
employee_file.close()







# Python Modules and Pip (3:30:00)

import useful_tools # import the name of the external file and use the code within it in your existing Python file.
print(useful_tools.roll_dice(100))

""" ** For more lists of modules, google 
list by going to official Pythons module index list **
"""

""" ** Python has 2 types of Modules:
1) Built in Modules (inside python)
2) External Modules (must be imported)
"""

""" ** On Python 3.7, to access built in modules,
go to "External Libraries" > "Python 3.7" > 
"Python 3.7 (library root)" **
"""

#

# importing Pip  ** get more info via youtube/book resources







# Classes & Objects

# The below code is to on a seperate python file
class Student:

   def __init__(self, name, major, gpa, is_on_probation):
        self.name = name
        self.major = major
        self.gpa = gpa
        self.is_on_probation = is_on_probation




# The below code is to on a seperate python file than the above

from Student import Student # This imports the above code to be called

student1 = Student("Jim", "Business", 3.1, False)
student2 = Student("Pam", "Art", 2.5, True)


# print(student1.name) prints "Jim"
# print(student1.gpa) prints gpa
# print(student2.name) prints "Pam"
# print(student2.major) prints gpa










# Building a Multiple Choice Quiz


# below is a class that is on a seperate python file
class Question:
    def __init__(self, prompt, answer):
        self.prompt = prompt
        self.answer = answer



# The below code is to on a seperate python file than the above

from Question import Question


question_prompts = [
    "What colors are apples?\n(a) Red/Green\n(b) Purple\n(c) Orange\n\n",
    "What color are Bananas?\n(a) Teal\n(b) Magenta\n(c) Yellow\n\n",
    "What color are strawberries?\n(a) Yellow\n(b) Red\n(c) Blue\n\n"

]

questions = [
    Question(question_prompts[0], "a"),
    Question(question_prompts[1], "c"),
    Question(question_prompts[2], "b"),
]

def run_test(questions):
    score = 0
    for question in questions:
        answer = input(question.prompt)
        if answer == question.answer:
            score += 1
    print("\nYou got " + str(score) + "/" + str(len(questions)) + " correct")


run_test(questions)








# Object Functions

# Below is a class with functions in a seperate file
class Student:
    def __init__(self, name, major, gpa):
        self.name = name
        self.major = major
        self.gpa = gpa

    def on_honor_roll(self):
        if self.gpa >= 3.5:
            return True
        else:
            return False


# Below is are the student1 & student2

from Student import Student


student1 = Student("Oscar", "Accounting", 3.1)
student2 = Student("Phyllis", "Business", 3.8)

print(student2.on_honor_roll()) # this wil;l print true b/c Phyllis has a gpa above 3.5









# Inheritance

# ------ Regular Chef Class
class Chef:

    def make_chicken(self):
        print("The chef makes a chicken")

    def make_salad(self):
        print("The chef makes a salad")

    def make_special_dish(self):
        print("The chef makes a bbq ribs")

# ----- Chinese Chef Class

from Chef import Chef

class ChineseChef(Chef):

    def make_special_dish(self):
        print("The chef makes orange chicken")

    def make_fried_rice(self):
        print("The chef cna make fried rice")

# -----

from Chef import Chef
from ChineseChef import ChineseChef

myChef = Chef()

myChef.make_special_dish() #prints bbq chicken
myChef.make_salad() #prints salad
myChef.make_chicken() #prints chicken

myChineseChef = ChineseChef()
myChineseChef.make_special_dish()

# -----







# Python Interpreter (4:20:00)

"""
Open up terminal. type "python 3". you can use 
this as a pyhton environment.
"""




