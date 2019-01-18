# hello-world
This is my first repository, my first try.
I am new to this coding world. All I did before was accounting, financial analysis and so on.
Now I am determined to be a skilled computer master.

# 17/01/2019

# Question 1: 
# Design a program that asks users to input their name and print"Hello, name!"
# Answer 1: 
x=input("Please input your name:")
print("Hello, %s"%x)
print("Hello, {}".format(x))

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
# Answer 3:
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
