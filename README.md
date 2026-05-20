import tkinter as tk
import tkinter.font as tkFont



okno=tk.Tk()

okno.title("bradar")

okno.geometry("1000x1000")






lbl_a=tk.StringVar(value="")
lbl_b=tk.StringVar(value="")
vysl_obvod=tk.StringVar(value="")
vysl_obsah=tk.StringVar(value="")

def poStisku():
    a=int(lbl_a.get())
    b=int(lbl_b.get())
    s=a*b
    o=2*a+2*b
    vysl_obvod.set(o)
    vysl_obsah.set(s)




velkyfont= tkFont.Font(family="Comic Sans MS", size=30)

lbl1 = tk.Label(okno, text="strana A:", font=velkyfont)
lbl1.grid(row=1, column=1)

lbl2 = tk.Label(okno, text="strana B:", font=velkyfont)
lbl2.grid(row=2, column=1)


box1 = tk.Entry(okno, font=velkyfont, textvariable=lbl_a)
box1.grid(row=1, column=2)

box2 = tk.Entry(okno, font=velkyfont, textvariable=lbl_b)
box2.grid(row=2, column=2)


btn = tk.Button(okno, text="VÝPOČET", font=velkyfont, command=poStisku)
btn.grid(row=3, column=2)

lbl3 = tk.Label(okno, text="Obvod:", font=velkyfont)
lbl3.grid(row=4, column=1)

lbl4 = tk.Label(okno, text="Obsah:", font=velkyfont)
lbl4.grid(row=5, column=1)

lbl5 = tk.Label(okno, text="číslo1", font=velkyfont, textvariable=vysl_obvod)
lbl5.grid(row=4, column=2)

lbl6 = tk.Label(okno, text="číslo2", font=velkyfont, textvariable=vysl_obsah)
lbl6.grid(row=5, column=2)



okno.mainloop()










import tkinter as tk
import tkinter.font as tkFont
import random



okno=tk.Tk()

okno.title("bradar")

okno.geometry("1000x1000")

velkyfont= tkFont.Font(family="Comic Sans MS", size=30)

def poStisku():
    cs = random.randint(1, 6)
    lbl_hodn.set(cs)
    global soucet

    soucet=soucet+cs
    souc_hodn.set(soucet)


soucet=0





lbl_hodn=tk.StringVar(value="číslo")
souc_hodn=tk.StringVar(value="číslo 2")

lbl1 = tk.Label(okno, text="number 1", font=velkyfont, textvariable=lbl_hodn)
lbl1.grid(row=2, column=2)

lbl2 = tk.Label(okno, text="number 2", font=velkyfont, textvariable=souc_hodn)
lbl2.grid(row=2, column=4)


btn = tk.Button(okno, text="roll dice", font=velkyfont, command=poStisku)
btn.grid(row=1, column=2)




okno.mainloop()















import tkinter as tk
import tkinter.font as tkFont
import random
from pickle import GLOBAL

# def poStisku2():
#     global ent, ent1, vysl
#     cs1=int(ent.get())
#     cs2=int(ent1.get())
#     vysl=0
#     i=cs1
#     while i<cs2:
#         vysl+=i
#         i+=1
#
#     lbl4.set(vysl)

okno=tk.Tk()


okno.geometry("800x600")
velky_font = tkFont.Font(family="Arail", size=30)
ent_hodn=tk.StringVar()
ent_hodn1=tk.StringVar()
lbl_hodn=tk.StringVar(value="Číslo")
lbl_hodn1=tk.StringVar(value="Výsledek:")
lbl_hodn2=tk.StringVar(value="XXXX")

lbl1=tk.Label(okno,font=velky_font,textvariable=lbl_hodn)
lbl1.grid(row=0,column=1)
lbl2=tk.Label(okno,font=velky_font,textvariable=lbl_hodn)
lbl2.grid(row=1,column=1)

# btn=tk.Button(okno,text="Výpočet",command=poStisku2,font=velky_font)
# btn.grid(row=2,column=1)

ent=tk.Entry(okno,font=velky_font,textvariable=ent_hodn)
ent.grid(row=0,column=2)
ent1=tk.Entry(okno,font=velky_font,textvariable=ent_hodn1)
ent1.grid(row=1,column=2)

lbl3=tk.Label(okno,font=velky_font,textvariable=lbl_hodn1)
lbl3.grid(row=3,column=1)

def poStisku2():
    global ent, ent1, vysl
    cs1=int(ent.get())
    cs2=int(ent1.get())
    vysl=0
    i=cs1
    while i<=cs2:
        vysl+=i
        i+=1

    lbl4.set(vysl)
btn=tk.Button(okno,text="Výpočet",command=poStisku2,font=velky_font)
btn.grid(row=2,column=1)



lbl4=tk.Label(okno,font=velky_font,textvariable=lbl_hodn2)
lbl4.grid(row=3,column=2)


okno.mainloop()











import tkinter as tk
import tkinter.font as tkFont
import random
def poStisku():
    global lbl_hodn, ent

    lbl_hodn.set("ahoj")
def poStisku1():

    lbl_hodn.set(ent_hodn.get())



okno=tk.Tk()


okno.geometry("800x600")
velky_font = tkFont.Font(family="Arail", size=30)
ent_hodn=tk.StringVar()
lbl_hodn=tk.StringVar(value="AA")
# lbl_hodn2=tk.StringVar(value="BB")

lbl1=tk.Label(okno,font=velky_font,textvariable=lbl_hodn)
lbl1.grid(row=0,column=1)

# lbl2=tk.Label(okno,textvariable=lbl_hodn2,font=velky_font)
# lbl2.grid(row=0,column=2)

# txtbox=tk.Entry(okno,font=velky_font)
# txtbox.grid(row=0,column=1)

btn=tk.Button(okno,text="stiskni",command=poStisku,font=velky_font)
btn.grid(row=2,column=1)
btn1=tk.Button(okno,text="stiskni",command=poStisku1,font=velky_font)
btn1.grid(row=2,column=2)

ent=tk.Entry(okno,font=velky_font,textvariable=ent_hodn)
ent.grid(row=0,column=2)





okno.mainloop()
import tkinter as tk
import tkinter.font as tkFont





def poStisku():
    a = int(lbl_a.get())
    b = int(lbl_b.get())
    c = int(lbl_c.get())

    v = a * b * c
    p = 2*a*b + 2*a*c + 2*b*c

    vysl_objem.set(v)
    vysl_povrch.set(p)







def idk():
    velkyfont = tkFont.Font(family="Comic Sans MS", size=30)

    lbl1 = tk.Label(okno, text="Strana A:", font=velkyfont)
    lbl1.grid(row=1, column=1)

    lbl2 = tk.Label(okno, text="Strana B:", font=velkyfont)
    lbl2.grid(row=2, column=1)

    lbl3 = tk.Label(okno, text="Strana C:", font=velkyfont)
    lbl3.grid(row=3, column=1)


    box1 = tk.Entry(okno, font=velkyfont, textvariable=lbl_a)
    box1.grid(row=1, column=2)

    box2 = tk.Entry(okno, font=velkyfont, textvariable=lbl_b)
    box2.grid(row=2, column=2)

    box3 = tk.Entry(okno, font=velkyfont, textvariable=lbl_c)
    box3.grid(row=3, column=2)


    btn = tk.Button(okno, text="VÝPOČET", font=velkyfont, command=poStisku)
    btn.grid(row=4, column=2)

    lbl4 = tk.Label(okno, text="Objem:", font=velkyfont)
    lbl4.grid(row=5, column=1)

    lbl5 = tk.Label(okno, text="Povrch:", font=velkyfont)
    lbl5.grid(row=6, column=1)


    lbl6 = tk.Label(okno, font=velkyfont, textvariable=vysl_objem)
    lbl6.grid(row=5, column=2)

    lbl7 = tk.Label(okno, font=velkyfont, textvariable=vysl_povrch)
    lbl7.grid(row=6, column=2)





okno = tk.Tk()
okno.title("Kvadr")
okno.geometry("1000x1000")



lbl_a = tk.StringVar(value="")
lbl_b = tk.StringVar(value="")
lbl_c = tk.StringVar(value="")

vysl_objem = tk.StringVar(value="")
vysl_povrch = tk.StringVar(value="")



idk()
okno.mainloop()
