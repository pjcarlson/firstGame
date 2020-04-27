# firstGame
#This is my first python code still a work in progress
#Chose your own adventure game March 2020

import random

import sys

sys.exit

def start():

    print('WELCOME TO THIS GAME!')

    print('You must be at least six years old to play.')
    print('How old are you?')

    age = int(input('Enter your age:'))

    while True:
        if age >= 6:
            print("Congratulations, you're old enough to play!")
            break;
        else:
            sys.exit("You need to grow up some before you can play, goodbye.")
            break;

    if age >= 6:
        print('What is your name?')
    name = input("> ")
    print(f'Well, {name} do you want to go on an adventure?')
    go = input("> ")

    if go in ['yes', 'Y' , 'YES' , 'Yes', 'y', 'yep', 'yup', 'sure', 'I guess', 'I suppose', 'yes please']  :
        print ('Hurrah! Let us begin!')
    elif go in ['no', 'NO', 'No', 'N', 'n', 'nah', 'no thank you']:
        print('Are you sure? It will be fun.')
        sure = inpput("> ")

        if sure == ('yes', "I'm sure"):
            sys.exit('Farewell, enjoy staying in your cozy home!')
        else:
            print("Let's get going then, we're waisting time!")

    else:
        print('Hurrah!, Let us begin!')

    print("The journey will be difficult, but the reward will be great!")
    input('Press enter to continue')
    print('Before you embark on your journey, you need to choose a weapon!')
    print('What weapon will you bring? You can bring a sword or a staff.')

    weapon = input("> ")

    if weapon in ['sword' , 'Sword', 'SWORD']:
        print("A sword! Great choice...you do know how to use that right?")
    elif weapon == 'staff':
        print("A staff! Excellent choice.")
    else:
        print(f'A {weapon} interesting choice...')

    print("Well, okay let's get going then.")
    input('Press Enter to continue')
    print('You open your door and head north out of town.')
    input('Press Enter to continue')

    items = 'food', 'towel', 'rope'

    def general_store():
        print('Before you leave town you stop by the general store for some supplies.')
        print()
        print("You're in luck, the shop keeper has all you need in stock.")
        print("Food for your journey costs $5, a towel is $2, and the rope you need is $3.")
        input('Press Enter to continue')
        print("Unfortunatley, you don't have enough money you only have $5.")
        print('What should you do?')

        print()
        print('A) buy the rope')
        print()
        print('B) buy the towel')
        print()
        print('C) buy the food')
        print()
        print('D) leave the store')

    general_store()

    tries = 4
    while tries > 0:
         choice = input("> ")
         if choice in ('leave the store', 'D', 'd'):
             print('You leave the store and meet a friend.')
             break;
         else:
             ('buy the food', 'C', 'buy the towel', 'B', 'buy the rope', 'A' )
             print("That won't be enough for the journey.")

             tries -=1
    def riddler():
        if choice in ('leave the store', 'D'):
            print('Your friend says that he will give you the money you need.')
            print("But first he needs you to solve a riddle that he's been working on for days")
            print("Do you accept to asnwer the riddle for money?")
            riddle = input("> ")

            if riddle == 'yes':
                print("What has hands but doesn't clap?")
                answer = input("> ")

                if answer in ('clock', 'a clock'):
                    print("Your friend is happy with this answer and gives you $5.")
                    print("You return to the store to buy your supplies.")
                else:
                    sys.exit("""Sorry, that's incorrect. Without the money to
                        purchase more supplies you cannot finish your journey."""
                        )

            else:
                sys.exit("You don't have enough money to purchase supplies. You can't continue.")
    riddler()

    def general_store_again():
        print(f"You purchase the {items} and head out of town.")

    general_store_again()

    print("You leave the store and continue on your journey, heading north out of town")
    print()
    print('When you reach the edge of town you meet a peculiar old man loading his cart')
    print()
    print('He asks for your assistance. Do you help?')

    help = input("> ")
    if help in ['yes', 'Y' , 'YES' , 'Yes', 'y', 'yep', 'yup', 'sure', 'I guess', 'I suppose', 'yes please',
    'help', 'okay', 'ok'] :
        print("Because you helped the old man he rewards you with a magical cloak.")
        print()
        print("This cloak will provide protection on your journey.")
        print()
        print("He also promises to come to your aid whenever you need.")
    else:
        print('Because you did not help you must suffer the consequences!')
        print()
        print('The old man shows his true form as a wizard')
        sys.exit('he turns you into a mouse and you are immediatly eaten by a hawk!')


    input('Press enter to continue')
    print('As you continue on your journey you come upon a fork in the road.')
    print('Do you go left or right?')

    #This is where the real "choose your own adventure" will require more detail.

    fork = input("> ")

    if fork == "right":

            print("You walk down the path and meet a dragon!")
            input()
            print("Do you fight or run away?")
            fight_or_flight = input()
            if fight_or_flight =="fight":
                print(f"You strike the dragon with your {weapon}!")

                if weapon == 'sword':
                    print("The dragon cries out in pain and roars at you angrily!")
                    print(f"He grabs your {weapon} and throws it into the woods to your left.")
                elif weapon == 'staff':
                    print("The dragon glares at you in annoyance.")
                else:
                    print("The dragon laughs at your strange choice of weapon.")

            else:
                print("You turn to run but the dragon calls out to not be afraid becuase he is friendly!")
                input()
                print("You stop, a little weary, but you turn around and the dragon asks you your name.")
                input()
                print(f"You tell him your name is {name}, becuase you know dragons can tell when someone is lying.")
                input()
                print('The dragon nods his head and tells you his name is Smorty.')
                print("Smorty says, \'I understand why you ran, I'm a dragon and most dragons are evil.\'")

    else:
        print('You turn left, walk down the road a ways and come to a pedler woman!')
        print()
        print('The old woman seems harmless enough.')
        print()
        print('She calls you over to play a game of chance.')
        print()
        print('You consider yourself to be good at games.')
        print()
        print('Do you agree to play?')

        play = input("> ")

        if play == "yes":
            print("""She removes a die from her pouch hanging from her belt.
            The pedlar woman explains that she will roll the die and
            if the die lands on an even number then she will reveal her true form
            to you."""
            )

            def roll(sides = 6):
                num_rolled = random.randint(1, sides)
                return num_rolled

            def main():
                sides = 6
                rolling = True
                while rolling:
                    roll_again = input ("Ready to roll? ENTER = Roll. Q = Quit.")
                    if roll_again.lower() != "q":
                        num_rolled = roll(sides)
                        print(f"You rolled a, {num_rolled}. ")
                    else:
                        rolling = False


            main()

    if fight_or_flight == "fight":
        print("He introduces himself and says his name is Smorty.")
        print("The dragons tells you that hs does not want to fight.")
        print("You introduce yourself and appoligize to Smorty and explain that you don't get out much.")
        print("Lucky for you Smorty is an understanding dragon who needs your help.")


start()
