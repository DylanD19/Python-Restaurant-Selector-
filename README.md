# Lab 1 Restaurant Selector
# Objective: Using the input from the user
# The program will run through a series of
# if and else statements to determine
# which restaurants are suitable for your needs!
# Date 9/21/2023
# Group Members Dylan Dias , Kyle Talerico
print('Welcome to the Restaurant Selector Program')
print("|------------------------------|")
print("|   *  Restaurant Display   *  |")
print("|------------------------------|")
print("|    * Joe's Gourmet Burgers   |")
print("|    *  Main Street Pizza Co   |")
print("|    *  Mama's Fine Italian    |")
print("|    *  Corner Cafe            |")
print("|    *  The Chef's Kitchen     |")
print("--------------------------------")
# Sources:
# Python Text Book / Slides
# https://www.w3schools.com/python/gloss_python_else.asp
message = ""  # Message can be better than print for concatenation purposes
# vegetarian, vegan, gluten_free are User Inputs
vegetarian = input("Is anyone in your party Vegetarian? Type yes/no: ")

if vegetarian == "yes" or vegetarian == "no":
    vegan = input("Is anyone in your party Vegan? Type yes/no: ")

    if vegan == "yes" or vegan == "no":
        gluten_free = input("Does anyone in your party have a Gluten allergy? Type yes/no: ")

        if gluten_free == "yes" or gluten_free == "no":
            message = "\nHere are the restaurant choices to fit your need: \n"

            if vegetarian == "yes":

                if vegan == "yes":

                    if gluten_free == "yes" or gluten_free == "no":
                        message += "Corner Cafe\n" + \
                                   "The Chef's Kitchen\n"
                else:  # vegetarian == "No"
                    if vegan == "yes":
                        if gluten_free == "yes" or gluten_free == "no":
                            message += "Corner Cafe\n The Chef's Kitchen\n"
                    else:
                        if gluten_free == "yes" or gluten_free == "no":
                            message += "Joe's Gourmet Burgers\n" + \
                                       "Main Street Pizza Co\n" + \
                                       "Corner Cafe\n" + \
                                       "Mama's Fine Italian\n" + \
                                       "The Chef's Kitchen\n"
            else:
                message += "Main Street Pizza Co\n" + \
                           "Corner Cafe\n" + \
                           "Mama's Fine Italian\n" + \
                           "The Chef's Kitchen\n"
        else:
            message = "Enter either 'yes' or 'no'. \nReRun the program and try again. "
    else:
        message = "Enter either 'yes' or 'no'.\nRerun the program and try again. "
else:
    message = "Enter either 'yes' or 'no'.\nRerun the program and try again. "

print(message)

#  Indentation Matters for the last 30 minutes my code didn't print anything
#  because I needed to move the print statement back more!
