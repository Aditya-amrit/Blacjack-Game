# Blacjack-Game

import random

def game():
    c=[1,2,3,4,5,6,7,8,9]
    e=random.choice(c)
    f=random.choice(c)
    h=random.choice(c)
    i=[h]
    l=h
    g=[e,f]
    k=e+f
    print(f"your cards are :{g}")
    print(f"the sum is :{k}")
    print(f"Cards computer have: {i}")

    z=False

    while not z:
        i=input("Choose one hit or stay(h or s): ")
        i=i.lower()

        if i=="h":
            d=random.choice(c)
            c1=random.choice(c)
            c2=random.choice(c)
            card=[c1,c2]
            print(f"Next cards of computer are: {card}")
            sum=c1+c2+h
            l+=sum
            k+=d
            print(f"sum of computers card is : {sum}")
            print(f"Sum of yours cards are : {k}")

            if k<22 and k>sum:
                print("You won the game..")
                z=True

            elif k > 21 and k < sum:
                print("You lost the game..")
                z=True

            else:
                print("tie")

        elif i == "s":
            c1=random.choice(c)
            c2=random.choice(c)
            card=[c1,c2]
            print(f"Next cards of computer are: {card}")
            sum=c1+c2+h
            l+=sum
            print(f"sum of computers card is : {sum}")
            print(f"Sum of yours cards are : {k}")

            if k<22 and k>sum:
                print("You won the game..")
                z=True

            elif k > 21 and k < sum:
                print("You lost the game..")
                z=True

            elif k == sum:
                print("tie")

        else:
            z=True

t=False

while not t:
    a=input("Do you want to play the game(y or n): ")
    a=a.lower()

    if a == "y":
        game()

    else:
        t = True
