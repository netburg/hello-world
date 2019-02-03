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
## Question 12
How many times will "Github" be printed in each of the following situation?
(1)    

    for i in range(0, 10, 2):  
        print('Github')
(2)    

    for i in 5:
        print('Github')    
## Answer 12
(1) 5 "Github"s will be printed, because we start from 0, and grow by 2, so we have: 0, 2, 4, 6, 8 and stop at 10.
(2) Traceback (most recent call last):
  File "C:\Users\Administrator\Desktop\domain-master\practices\hello.py", line 1, in <module>
    for i in 5:
TypeError: 'int' object is not iterable
## Question 13
(1) What will range(10) generate?    
(2) What will the following codes print?
     
     while True:
        while True:
            break
            print(1)
        print(2)
        break
    print(3)
## Answer 13
(1) If you type range(10) in python IDLE, it will generate range(0,10), and if you list(rang(0,10)), you will get: [0,1,2,3,4,5,6,7,8,9]. However, it does not include 10.    
(2) 2 3 will be printed. Because after break in the inside "while" loop, print(1) will not be executed.    
## Question 14
How to make the following codes more efficient?  
    
    i = 0
    string = 'Github'
    while i < len(string):
        print(i)
        i += 1
## Answer 14
    i=0
    string = 'Github'
    length = len('Github')
    while i < length:
        print(i)
        i += 1
## Question 15
Please design a program that can realize the following:
"Please input your password:******   
 Don't input "*", you have 3 times left!Please input your password: ***IloveYou   
 Don't input "\*", you have 3 times left!Please input your password: okokok   
Incorrerct password!! You have 2 times left!Please input your password: okfine   
Incorrerct password!! You have 1 times left!Please input your password: github   
Correct. The program is starting...   
## Answer 15
    temp=input('Please input your password:')
    password="github"
    i=3
    while "*" in temp:
        print('Don\'t input "*", you have %d times left!'%i,end="")
        temp=input('Please input your password:')
    while (temp!=password) and (i>0):
        i-=1
        print("Incorrerct password!! You have %i times left!"%i, end="")
        temp=input('Please input your password:')
    print("Correct. The program is starting...")
## Question 16
An n-digit number that is the sum of the nth powers of its digits is called an n-narcissistic number. It is also sometimes known as an Armstrong number, perfect digital invariant (Madachy 1979), or plus perfect number. Hardy (1993) wrote, "There are just four numbers, after unity, which are the sums of the cubes of their digits: 153=1^3+5^3+3^3,  370=3^3+7^3+0^3, 371=3^3+7^3+1^3, and 407=4^3+0^3+7^3. These are odd facts, very suitable for puzzle columns and likely to amuse amateurs, but there is nothing in them which appeals to the mathematician." Narcissistic numbers therefore generalize these "unappealing" numbers to other powers (Madachy 1979, p. 164).
The smallest example of a narcissistic number other than the trivial 1-digit numbers is    
 153=1^3+5^3+3^3.     
 Design a program to find out all 3-narcissistic number from 100-999.
 ## Answer 16
 Method 1   
     
     for a in range(1,10,1):
        A=100*a
        for b in range(0,10,1):
            B=10*b
            for c in range(0,10,1):
                C=c
                i=A+B+C
                while i==a**3+b**3+c**3:
                    print(i)
                    break    
Method 2   

    for i in range(100, 1000):
        sum = 0
        temp = i
        while temp:
            sum = sum + (temp%10) ** 3
            temp //= 10        
        if sum == i:
            print(i)
    
Method 3   A general way to find out narcissistic numbers:
   
        def narcissistic_number_1(num):

        length = len(str(num))

        count = length    

        num_sum = 0    

        while count:        

            num_sum += ((num // 10 ** (count - 1)) % 10) ** length     

            count -= 1    

        else:       

            if num_sum == num:            

                print("%d is %d bit narcissistic_number" % (num, length))
            else:                        
                pass


    max_num = int(input('Please input your range:'))


    for num in range(0, max_num):

        narcissistic_number_1(num)        
# 21/01/2019 & 22/02/2019
Reading a novel: The Three-boday Problem
# 23/01/2019
## Question 17
There are 3 red balls, 3 yellow balls, 6 green balls in one box. Randomly pick 3 balls from the box, how many cases could be ?
## Answer 17
    print("No.\tRed\tYellow\tGreen")
    i=0
    for Red in range(0,4):
        for Yellow in range(0,4):
            for Green in range(0,7):
                if Red+Yellow+Green==3:
                    i=i+1
                    print(i,'\t',Red, '\t', Yellow, '\t', Green)
## Question 18
if: Member=\['Jim',100,'Wendy',98,'Selina',97,'Helen',89], design a program to print the following:    
Jim    
100    
Wendy    
98    
Selina    
97    
Helen    
89   
## Answer 18
    Member=['Jim',100,'Wendy',98,'Selina',97,'Helen',89]
    for each in Member:
        print(each)
## Question 19
Change the above result to the following:    
Jim: 100   
Wendy: 98   
Selina: 97   
Helen: 89   
## Answer 19
Method 1
    
    Member=['Jim',100,'Wendy',98,'Selina',97,'Helen',89]
    for each in Member:
        if type(each)==type('a'):
            print(each+':', end=' ')
        else:
            print(each)
Method 2  

    Member=['Jim',100,'Wendy',98,'Selina',97,'Helen',89]
    count = 0
    length = len(Member)
    while count < length:
        print(Member[count]+': ',Member[count+1])
        count += 2
Method 3   

    Member=['Jim',100,'Wendy',98,'Selina',97,'Helen',89]
    for each in range(len(Member)):
        if each%2 == 0:
            print(Member[each]+": ", Member[each+1])
#25/01/2019   
## Question 20
What does list1 = \[(x, y) for x in range(10) for y in range(10) if x%2==0 if y%2!=0] mean?    
## Answer 20
It means:   

    list1=[]
    for x in range(10):
        if x%2==0:
            for y in range(10):
                if y%2!=0: 
                    list1.append((x,y))
    print(list1)
And it will print:    
[(0, 1), (0, 3), (0, 5), (0, 7), (0, 9), (2, 1), (2, 3), (2, 5), (2, 7), (2, 9), (4, 1), (4, 3), (4, 5), (4, 7), (4, 9), (6, 1), (6, 3), (6, 5), (6, 7), (6, 9), (8, 1), (8, 3), (8, 5), (8, 7), (8, 9)]    
## Question 21
list1=\['1.Just Do It','2.Everything Is Possible','3.Coding Changes the World','4.Impossible Is Nothing']    
list2=\['4.Adidas','2.Lining','3.Github','1.Nike']
Design a program that print:    
1:Nike: Just Do It  
2.Lining: Everything Is Possible   
3.Github: Coding Changes the World  
4.Adidas: Impossible Is Nothing  
## Answer 21

    list1=['1.Just Do It','2.Everything Is Possible','3.Coding Changes the World','4.Impossible Is Nothing']    
    list2=['4.Adidas','2.Lining','3.Github','1.Nike']
    list3=[name+": "+slogan[2:] for slogan in list1 for name in list2 if name[0]==slogan[0]]
    for each in list3:
        print(each)

# 26/01/2019 Web Deveopment
## Case 1 Hello world
    from flask import Flask

    app = Flask(__name__)

    @app.route('/')
    def index():
        return 'Hello, World!'

    if __name__ =='__main__':
        app.run(debug=True, host='0.0.0.0', port=5000)
## Template
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        {%if title%}
        <title>{{title}}</title>
        {% else %}
        <title>Singer</title>
        {% endif %}
    </head>
    <body>
        {% include 'navbar.html'%}
        {% block content %}
        {% endblock %}
    </body>
    </html>
# 28/01/2019
## URL and parameters
    @app.route('/article/<id>')
    def article(id):
        return 'The parameter you request is: s%' %id
## reverse URL and redirect
    from flask impoort Flask, redirec, url_for
    app = Flask(__name__)
    
    @app.route('/')
    def index():
        login_url = url_for('login')
        return redirect(login_url)
        return 'This is homepage.'
        
    @app.route('/login/')
    def login():
        return 'This is login page.'
## test for redirect
    @app.route('/question/<is_login>/')
    def question(is_login):
        if is_login == '1'
            return 'This is publishing page.'
        else:
            return redirect(url_for('login'))
# 29/01/2019
## IF statement in Web
    from flask import Flask, render_template
    app = Flask('__name__')
    @app.route('/<is_login>')
    def index(is_login):
        if login == '1':
            user = {'username': Jim, 'age': 28, }
            return render_template('index.html', user = user )
        else:
            return render_template('index.html')
    if __name__= '__main__':
        app.run(debug=True)
## The  'index.html' involved
    <!DOCTYPE html>
    <html lang='en'>
    <head>
         <meta charset="UTF-8">
         <title>Exercise</title>
    </head>
    <body>
        {% if user%}
            {% <a href="#"> {{user.username}} </a> %}
            {% <a href="#"> Logout </a> %}
        {% else %}
            {% <a href="#"> Login </a> %}
            {% <a href="#"> Sign up </a> %}
        {% ednif %}
    </body>
    
    </html>
# 30/01/2019    
## filter
    from flask import Flask, render_template

    app = Flask('__name__')


    @app.route('/')
    def index():
        comments=[{'username': 'Jin', 'content': 'Very good.'}, {'username': 'Jim', 'content': 'Not bad.'}]
        myimage='https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png'
        return render_template('index.html', comments=comments, myimage=myimage)


    if __name__ == '__main__':
        app.run(debug=True)
        
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>过滤器</title>
    </head>
    <body>
        <img src="{{myimage|default('https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=1456128855,663055519&fm=58') }}", alt="">
        <hr>
        <p>评论数：（{{ comments|length}}）</p>
        <ul>
            {% for comment in comments %}
                <li>
                    <a href="#">{{comment.username}}</a>
                    <p>{{comment.content}}</p>
                </li>
            {% endfor %}
    </body>
    </html>
# 31/01/2019
## MYSQL: add data
    from flask import Flask
    from flask_sqlalchemy import SQLAlchemy
    import config

    app = Flask('__name__')
    db = SQLAlchemy(app)
    app.config.from_object(config)

    # create table article(
    #     id int primary key autoincrement,
    #     title varchar(100) not null,
    #     content text not null,
    # )

    class Article(db.Model):
        __tablename__='article'
        id = db.Column(db.Integer, primary_key=True, autoincrement=True)
        title = db.Column(db.String(100), nullable=False)
        content = db.Column(db.Text, nullable=False)
    db.create_all()

    @app.route('/')
    def index():
        article1=Article(title='ITSinger', content='I am Singer0001')
        db.session.add(article1)
        db.session.commit()
        return 'index'
## Query
    from flask import Flask
    from flask_sqlalchemy import SQLAlchemy
    import config

    app = Flask('__name__')
    db = SQLAlchemy(app)
    app.config.from_object(config)

    class Article(db.Model):
        __tablename__='article'
        id = db.Column(db.Integer, primary_key=True, autoincrement=True)
        title = db.Column(db.String(100), nullable=False)
        content = db.Column(db.Text, nullable=False)
    db.create_all()

    @app.route('/')
    def index():

        article11 = Article.query.filter(Article.title=='ITSinger').first()
        print('title: %s' % article11.title)
        print('content: %s' % article11.content)
        return 'index'


    if __name__ == '__main__':
        app.run(debug=True)
## Confige.py
    # dialect+driver://username:password@host:port/database
    DIALECT = 'mysql'
    DRIVER = 'mysqldb'
    USERNAME = 'root'
    PASSWORD = '645018@hzzj'
    HOST = '127.0.0.1'
    PORT = '3306'
    DATABASE ='db_demo1'
    SQLALCHEMY_DATABASE_URI ='{}+{}://{}:{}@{}:{}/{}?charset=utf8'.format(DIALECT, DRIVER, USERNAME, PASSWORD, HOST, PORT, DATABASE)

    SQLALCHEMY_TRACK_MODIFICATIONS = False
## Foreign Key
    from flask import Flask
    from flask_sqlalchemy import SQLAlchemy
    import config

    app = Flask('__name__')
    app.config.from_object(config)
    db = SQLAlchemy(app)
    # #user
    # create table users(
    #     id int primary key autoincrement,
    #     username varchar(100) not null)
    # # article
    # create table article(
    #     id int primary key autoincrement,
    #     title varchar(100) not null
    #     content text not null,
    #     author_id int,
    #     foreign key `author_id` references `users.id`
    # )
    # create table article(
    #     id int primary key autoincrement,
    #     title varchar(100) not null,
    #     content text not null)
    class User(db.Model):
        __tablename__= 'user'
        id = db.Column(db.Integer, primary_key=True, autoincrement=True)
        username = db.Column(db.String(100), nullable=False)
    class Article(db.Model):
        __tablename__='article'
        id = db.Column(db.Integer, primary_key=True, autoincrement=True)
        title = db.Column(db.String(100), nullable=False)
        content = db.Column(db.Text, nullable=False)
        author_id = db.Column(db.Integer, db.ForeignKey('user.id'))
        author = db.relationship('User',backref=db.backref('articles'))
    db.create_all()


    @app.route('/')
    def index():
        # article1=Article(title='ITSinger', content='I am Singer0001')
        # db.session.add(article1)
        # db.session.commit()
        # article11 = Article.query.filter(Article.title=='ITSinger').first()
        # print('title: %s' % article11.title)
        # print('content: %s' % article11.content)
        # article1=Article.query.filter(Article.title=='ITSinger').first()
        # article1.title='Dancer'
        # db.session.commit()
        # article1=Article.query.filter(Article.title=='Dancer').first()
        # db.session.delete(article1)
        # db.session.commit()
        # SQL
        #添加一篇文章，先添加用户
        # user1 = User(username='Jim')
        # db.session.add(user1)
        # db.session.commit()
        #
        # article1 = Article(title='AAA', content='BBB', author_id=1)
        # db.session.add(article1)
        # db.session.commit()
        # article2 = Article(title='aaa', content='bbb')
        # article2.author = User.query.filter(User.id==1).first()
        # db.session.add(article2)
        # db.session.commit()
        # article = Article.query.filter(Article.title=='AAA').first()
        # print('username: %s'%article.author.username)
        user=User.query.filter(User.username=='Jim').first()
        result=user.articles
        for article in result:
            print('-'*10)
            print(article.title)
        return 'index'


    if __name__ == '__main__':
        app.run(debug=True)

# 2/2/2019
## Database init and tables migrate
## db_scripts.py
    from flask_script import Manager

    DBManager = Manager()

    @DBManager.command
    def init():
        print('Successfully init database！')

    @DBManager.command
    def migrate():
        print('Successfully migrate tables！')

## manage.py
    from flask_script import Manager
    from itsinger import app
    from db_scripts import DBManager
    manager = Manager(app)


    @manager.command
    def runserver():
        print('The server is on!!!')


    manager.add_command('db',DBManager)

    if __name__=='__main__':
        manager.run()
## session and cookie
    from flask import Flask,session
    import os
    app = Flask(__name__)
    app.config['SECRET_KEY'] = os.urandom(24)
    @app.route('/')
    def index():
        session['username']='Jim'
        return 'index'
    @app.route('/get/')
    def get():
        return session.get('username')
    @app.route('/delete/')
    def delete():
        print(session.get('username'))
        session.pop('username')
        print(session.get('username'))
        return 'delete success'

    @app.route('/clear/')
    def clear():
        print(session.get('username'))
        session.clear()
        print(session.get('username'))
        return 'OKld'
    if __name__ == '__main__':
        app.run(debug=True)
