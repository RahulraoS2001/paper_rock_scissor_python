import random
print("*****************")
print("*       * PAPER * ROCK * SCISSOR *            *")
print("*****************")
print(" Lets start the game!!.... ")
point=0
ai=0
hs=0
cs=0
ma=0
while(True):
    if(ma>5):
        print("#################################")
        print("Total Match: ",ma)
        print("Human Score: ",hs)
        print("AI Score: ",cs)
        if(hs>cs):
            print("Congrats You Won")
        elif(cs>hs):
            print("AI Won.... Better luck next time")
        else:
            print("MATCH DRAW")
        print("##################################")
        break
    c=input(" Choose Paper->p  Rock->r  Scissor->s Stop->stop: ")
    if(c=="p"):
        point=10+random.randint(1,3)
        match point:
            case 11:
                ma=ma+1
                hs=hs+1
                print("Human: Paper", "AI: Rock")
                print("Match: ",ma,"Human Score: ",hs,"AI Score: ",cs)
                print("Human: win","AI: lost")
                print("____________")                
            case 12:
                ma=ma+1
                cs=cs+1
                print("Human: Paper", "AI: Scissor")
                print("Human: Lost","AI: Won")
                print("____________")                
            case 13:
                ma=ma+1
                hs=hs+1
                cs=cs+1
                print("Human: Paper", "AI: Paper")
                print("Match Draw")
                print("____________")                
    elif(c=="r"):
        print("Rock")
    elif(c=="s"):
        print("Scissor")
    elif(c=="stop"):
         break
print("Program End")