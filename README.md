import random
def is_game():
    print('Welcome to guessing game')

    print('Enter the right limit of the number to guess:')
    t = int(input())
    num = random.randint(1, t)
    c = 1


    def is_valid(num):
        if n.isdigit() and 1 <= int(n) <100:
            return True
        else:
            return False
        pass

    while True:
        print('Input the number from 1 to', t, ': ')
        n = input()
        if is_valid(n) == False:
            print('Maybe you should input the integer number from 1 to 100?')
            continue
        else:
            n = int(n)

            if n < num:
                print('Your number is smaller than that one, try again')
                c += 1
                continue
            elif n > num:
                print('Your number is bigger than that one, try again ')
                c += 1
                continue
            elif n == num:
                print('You guessed, congratulation!')
                print('You used tries:', c)
                break
    print('Thank you for playing the number guessing game, see you... ')
    pass
is_game()
w = input('Would you like to play this game one more time? Enter "yes" if you want: ')
if w.lower()=='yes':
    is_game()
else:
    print('f')
