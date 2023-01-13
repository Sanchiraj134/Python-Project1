# Python-Project1
#game of stone paper and scissors

import random
print("Welcome to this game of Rock, Paper and Scissor")
print("")
a= input("Your Name:")
print("")
print("Hello!",a,"Here are some rules for this game.")
print("")
print("Rule No. 1 --> Rock smashes Scissor, Scissor cuts Paper and Paper rocks over Rock.")
print("Rule No. 2 --> You will get 3 or 5 chances to play.")
print("Rule No. 3 --> You will get 1 point everytime you win.")
print("At the end you can see your score")
print("")
n= int(input("How many chances you wanna play 3 or 5: "))
print("")
print("Let's Play")
print("")
print("Press 'r' for Rock, 'p' for Paper and 's' for Scissor")
print("")
i= 0
j= 0
k= 0
while n>0 :
    c= random.choice(["r","p","s"])
    d= input("Your choice is: ")
    print ("Computer's choice is:",c)

    if c == d:
        print("You both have same choice")
    elif c == "s" and d =="p":
        print("You lose")
        k = k + 1
    elif c == "p" and d =="s":
        print("You won")
        j = j + 1
    elif c == "s" and d =="r":
        print("You won")
        j = j + 1
    elif c == "r" and d =="s":
        print("You lose")
        k = k + 1
    elif c == "p" and d =="r":
        print("You lose")
        k = k + 1
    elif c == "r" and d =="p":
        print("You won")
        j = j + 1
    else:
        print("Invalid input")
        print("Now,you have to start again!!! ")
    print("")
    n = n - 1

if j > k:
    print("HURRAY! YOU WON.")
    print("Your Score is:",j)
    print("Computer Score is:",k)
elif j == k:
    print("It's a TIE!!!")
    print("You both scored:",j)
else:
    print("Sorry! You Lost.")
    print("Your Score is:",j)
    print("Computer Score is:",k)
    print("BETTER LUCK Next Time.")
