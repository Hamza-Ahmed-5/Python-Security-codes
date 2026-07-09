# Python-password-checker
A python program to check a password has length = 12 , a number , upper , lower and special chrachters


import random
import string
import re
booleanFlag1 = re.compile("[@!#$%^&*-_:?]")
booleanFlag2 = re.compile("[1234567890]")
booleanFlag3 = re.compile("[ABCDEFGHIGKLMNOPQRSTUVWXYZ]")


def evaluate_password(password):
    length = 12
    special_characters = "@!#$%^&*()-=+:}]/" 
    numbers = "1234567890"
    upper_characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    lower_characters = upper_characters.lower()

  
    special = False
    num = False
    up = False
    low = False

    for X in password:
        if X in special_characters:
            special = True
        if X in numbers:
            num = True
        if X in upper_characters:
            up = True
        if X in lower_characters:
            low = True

    return special and num and up and low


password = input("Enter your password: ")
print(evaluate_password(password))


if booleanFlag2 .search(password):
    print("There is a digit")
else:
    print("digit is missed")
if booleanFlag3.search(password):
    print("There is an upper_case letter")
else:
    print("upper_case letter is missed")

if booleanFlag1.search(password):
    print("There is a special chrachter")
else:
    print("special chrachter is missed")
length =len(password) 
if len(password)==12 :
    print("length is correct")
else:
    print("length is incorrect and doesn't equal 12")
#user input is the password

