# hello-world
This is my first repository, my first try.  
I am new to this coding world. All I did before was accounting, financial analysis and so on.</br>
Now I am determined to be a skilled computer master.</br>

# 17/01/2019

# Question 1: 
# Design a program that asks users to input their name and print"Hello, name!"
# Answer 1: 
x=input("Please input your name:")</br>
print("Hello, %s"%x)</br>
print("Hello, {}".format(x))</br>

# Question 2: 
# Design a program that asks users to input numbers between 1 to 100, and print "Good choice" if they did so, otherwise print "Please think for a while"
# Answer 2: 
number1=int(input("Please input a number between 1 and 100:"))  
if 1<=number1<=100:  
    print("Good choice")  
else:
    print("Please think for a while")

# Question 3: 
# Design a program: randomize an integer from 1 to 10, and let users guess what it is. If users' guess is right, print "Good Luck You!", otherwise print "Oh sorry it's too large/small!", then let users input again and remind users "you have n chances left!". Maximum 3 chances.
# Answer 3A:
import random  
temp1 = random.randint(1,10)  
temp2 = int(input("Please input an integer between 1 and 10, you have 3 chances:"))  
i=3  

while i:

    if temp1==temp2:
        print("Good Luck You!")
        i=0

    else:
        if temp2 > temp1:
            print("Oh sorry it's too large!")
           
        else:
            print("Oh sorry it's too small!")

        if i-1>0:
            temp2 = int(input("Please input an integer between 1 and 10, you have %d chances left:"%(i-1)))
            i-=1
        else:
            print("No chances left!")
            i=0
print('Game Over')

# Question 4:
# Let users input an positive integer and list all the positive integers less than or equal to this one. Each listed integer is in one line.
# Answer 4:
temp = int(input("Please input an positive integer:"))  
i=1  
while temp:
    print(i)
    i+=1
    temp-=1
    
# Question 5
# Let users input a positive integer and draw a picture as following:(for example users input 5)
    *****
   **** 
  ***
 **
*
# Answer 5
temp = int(input("Please input a positive integer:"))
while temp:
    print(" " * (temp-1) + '*'* temp)
    temp-=1
# A more complicated version of Answer 5:
temp = input("Please input a positive integer:")
number = int(temp)
while number:
    i = number - 1
    while i:
        print(' ', end = '')
        i = i - 1
    j = number
    while j:
        print('*', end = '')
        j = j - 1
    print()
    number = number - 1
    
    # Question 5:
    # Design a program to judge whether a particular year is a leap year.
    # Anaswer 5:
    Judge = 'Y'
while (Judge=='Y') or (Judge=='y'):
    temp = input("Please input year:")
    while not temp.isdigit():
        temp = input("Sorry! Incorrect input. Please input an integer:")
    year=int(temp)
    if year/400 == int(year/400):
        print(temp + " is a leap year!")
    else:
        if year/4 == int(year/4):
            print(temp + " is a leap year!")
        else:
            print(temp + " is NOT a leap year!")
    Judge = input("Go on or not? Y/N:")
    
print("User has terminated the program.")
