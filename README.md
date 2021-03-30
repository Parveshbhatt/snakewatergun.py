# snakewatergun.py
<p>import random<br>
print("We Gonna Play Snake Water and Gun")
swg=["snake","water","gun"]
r=random.choice(swg)
dict_swg={1:"snake",2:"water",3:"gun"}

i=1
while(i<=3):
    print(i,".",dict_swg[i])
    i=i+1
uw=0
cw=0
ti=0
z=1
try:
    while(z<=5):
        print("choose 1,2 or 3:")
        a=int(input("Your choice:"))
        b=dict_swg[a]
        print("Your choice:","'",b,"'")
        if b=="snake" and r=="water":
            print("YOu won!!")
            uw=uw+1
        elif b=="snake" and r=="gun":
            print("you loos!!")
            cw=cw+1
        elif b=="water" and r=="snake":
            print("you loos!!")
            cw=cw+1
        elif b=="water" and r=="gun":
            print("you win!!")
            uw=uw+1
        elif b=="gun" and r=="snake":
            print("you win!!")
            uw=uw+1
        elif b=="gun" and r=="water":
            print("you loos!!")
            cw=cw+1
        else:
            print("tie!!")
            ti=ti+1
        print("computer choice:","'",r,"'")
        z=z+1
    print("YOu win :",uw,"times\n","Computer win:",cw,"times\n")
    print("match tie:",ti,"times")
    print(" so,overall winner is :\n")
    if uw>cw:
        print("You")
    elif cw>uw:
        print("computer")
    else:
        print("match is tie !!")
except Exception as e:
    print("oops!! enter only 1,2 or 3 ::")
    
</p>
