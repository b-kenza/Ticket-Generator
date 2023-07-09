#Kenza

import re

 

#text file

DVLA = [['AA11 AAA','Andy Smith', '100 Over there','Norwich','NR5 5AR'],

['BB22 BBB','Frank Fapp','13 Not here','Liverpool','L1 4AS'],

['CC33 CCC','David Williams','99 This way','Nottingham','NG11 7BY'],

['DD44 DDD','Thomas Engine','15 Flappy Drive','Wolverhampton','WV13 5RE']]

 

#function to check speeding

def speeding(time, distance):

    speed = distance/time

    if (speed > 1):

        return True

    else:

        return False

 

#function to check if number plate is standard

def numberPlateStandard(numberPlate):

    regex = r'^[A-Z]{2}\d{2} [A-Z]{3}$'

    if re.match(regex, numberPlate):

        return True

    else:

        #return False

        print("Your number plate is not valid")

        print("Please try again")

        quit()

 

#getting the name, address and printing them a letter.

def getOffenderName(numberPlate):

    for item in DVLA:

        if numberPlate == item[0]:

            name = item[1]

            addLine1 = item[2]

            addLine2 = item[3]

            addLine3 = item[4]

            with open("letter.txt", "w") as f:

                f.write(addLine1 + "\n" + addLine2 + "\n" + addLine3 + "\n")

                f.write("Dear " + name + ",\n\n")

                f.write("Your car was caught speeding and you must pay a fine of £100.\n\n")

                f.write("Yours Sincerely,\n")

                f.write("Islington Council Ticket Office")

 

#questions/ main

distance = input("How far did you travel (in km)?")

time = input("How long did it take you to travel that distance (in minutes?")

numberPlate = input("Enter your number plate please.")

numberPlateStandard(numberPlate)

 

#function to make checks and act accordingly

if speeding(float(time), float(distance)):

    getOffenderName(numberPlate)

else:

    print("You are have traveled within the speed limit.") 
