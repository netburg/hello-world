# Hello, world!<br> 
This is my first repository, my first try.   
I am new to this coding world. All I did before was accounting, financial analysis and MBA stuff.    
Now I am determined to be a skilled computer master.    
[My LinkIn](https://www.linkedin.com/in/jin-zhang-412b8516b/)

# 17/01/2019
## Question 1 
Design a program that asks users to input their name and print"Hello, name!"
## Answer 1 
    x=input("Please input your name:")   
    print("Hello, %s"%x)  
    print("Hello, {}".format(x))   

## Question 2 
Design a program that asks users to input numbers between 1 to 100, and print "Good choice" if they did so, otherwise print "Please think for a while"
## Answer 2 
    number1=int(input("Please input a number between 1 and 100:"))   
    if 1<=number1<=100:  

        print("Good choice")    
    else: 

        print("Please think for a while")  

## Question 3 
Design a program: randomize an integer from 1 to 10, and let users guess what it is. If users' guess is right, print "Good Luck You!", otherwise print "Oh sorry it's too large/small!", then let users input again and remind users "you have n chances left!". Maximum 3 chances.
## Answer 3
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

## Question 4
Let users input an positive integer and list all the positive integers less than or equal to this one. Each listed integer is in one line.
## Answer 4:
    temp = int(input("Please input an positive integer:"))    
    i=1    
    while temp:
        print(i)    
        i+=1   
        temp-=1   
    
## Question 5
Let users input a positive integer and draw a picture as following:(for example users input 5)
         
        *****   
       ****   
      ***   
     **   
    *   
## Answer 5

    temp = int(input("Please input a positive integer:"))   
    while temp:   

        print(" " * (temp-1) + '*'* temp)   
        temp-=1   
## A more complicated version of Answer 5:
    temp = input("Please input a positive integer:")   
    number = int(temp)   
    while number:   

        i = number - 1   
        while i:</br>
            print(' ', end = '')   
            i = i - 1   
        j = number   
        while j:   
            print('*', end = '')   
            j = j - 1   
        print()   
        number = number - 1   
# 18/01/2019    
## Question 6
Design a program to judge whether a particular year is a leap year.
## Anaswer 6
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

## Question 7
There is a long ladder, if you take 2 steps each time, and finally 1 step left;If once take 3 steps, you end up with 2 steps ;If 5 steps each time, 4 steps left.If 6 steps a time, you end up with 5 steps left. If you take 7 steps each time, you finish climbing with no steps left. How many steps does the ladder have?
## Answer 7
    i=1
    while not ((i%2==1) and (i%3==2) and (i%5==4) and (i%6==5) and (i%7==0)):
        i+=1
    print(i)
## Question 8
What does "if not (i<100)" mean？
## Answer 8
It means:  
      if i>=100  
## Question 9
x=1, y=2, z=3. How to exchange values of x, y, z?
## Answer 9
For example: x, y, z= z, x, y
# 19/01/2019
## Question 10
In the final example of Baruch College, if your score is between 90 and 100: you get A; between 80 and 90: you get B; between 60 and 80, you get C;  below 60, you get F. According to statistical law, grades is normally distributed, so most students get 60-80. Design an effective program to relize: when you input your score, you get A, B, C, or F printed out.   
## Answer 10
    Score=float(input("Please input your score:"))
    if 60<=Score<80:
        print("C")
    elif 90<=Score<=100:
        print("A")
    elif 80<=Score<90:
        print("B")
    elif 0<=Score<60:
        print("F")
    else:
        print("Illegal Input!")
# 20/01/2019
## Question 11
Rewrite the following codes to make it more efficient.(Using Ternary operators).

    x, y, z = 6, 5, 4    
    if x < y:    
        small = x
    if z < small:
        small = z
    elif y < z:
        small = y
    else:
        small = z
## Answer 11
    small=x if(x<y and x<z) else (y if y<z else z)
