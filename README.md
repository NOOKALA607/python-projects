
from tkinter import *
from tkinter import messagebox
window=Tk()
window.title("simple caluculator")
window.geometry("500x500")
window.resizable(0,0)
man=StringVar()

val=""
a=0

operator=""
def press1():
    global val
    val=val+"1"
    man.set(val)

def press2():
    global val
    val=val+"2"
    man.set(val)

def press3():
    global val
    val=val+"3"
    man.set(val)

def press4():
    global val
    val=val+"4"
    man.set(val)

def press5():
    global val
    val=val+"5"
    man.set(val)

def press6():
    global val
    val=val+"6"
    man.set(val)

def press7():
    global val
    val=val+"7"
    man.set(val)

def press8():
    global val
    val=val+"8"
    man.set(val)

def press9():
    global val
    val=val+"9"
    man.set(val)

def press0():
    global val
    val=val+"0"
    man.set(val)

def clr():
    global a
    global operator
    global val
    val=""
    a=0
    operator=""
    
    man.set(val)
def plus():
    global a
    global operator
    global val
    a=int(val)
    operator="+"
    val =val + "+"
    man.set(val)


def minus():
    global a
    global operator
    global val
    a=int(val)
    operator="-"
    val =val + "-"
    man.set(val)

def mul():
    global a
    global operator
    global val
    a=int(val)
    operator="*"
    val =val + "*"
    man.set(val)

def div():
    global a
    global operator
    global val
    a=int(val)
    operator="/"
    val =val + "/"
    man.set(val)

def equal():
    global a
    global operator
    global val
    val2=val
    if operator=="+":
        x=int((val2.split("+")[1]))
        c=a+x
        man.set(c)
        val=str(c)

    elif operator=="-":
        x=int((val2.split("-")[1]))
        c=a-x
        man.set(c)
        val=str(c)

    elif operator=="*":
        x=int((val2.split("*")[1]))
        c=a*x
        man.set(c)
        val=str(c)

    elif operator=="/":
        x=int((val2.split("/")[1]))
        if x==0:
            messagebox.showerror("error","Division by 0 Not Supported")
            a=""
            val=""
            man.set(c)


        else:
            c=int(a/x)
            man.set(c)
            val=str(c)
        
    

l=Label(window, text="CALUCULATOR", font=("elephant",20, "bold"), fg="black")
l.grid(columnspan=2)

e=Entry(window, font=("elephant",20,"bold"),textvariable=man,bd=30
                    ,bg="powder blue",justify="left")
e.grid(columnspan=4)

b1=Button(window, text="1", font=("elephant", 20,"bold"),
                                    fg="black",padx=25,bd=10, command=press1)
b1.grid(row=2, column=0)

b2=Button(window, text="2", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press2)
b2.grid(row=2, column=1)

b3=Button(window, text="3", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press3)
b3.grid(row=2, column=2)

b4=Button(window, text="+", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=plus)
b4.grid(row=2, column=3)

b5=Button(window, text="4", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press4)
b5.grid(row=3, column=0)

b6=Button(window, text="5", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press5)
b6.grid(row=3, column=1)

b6=Button(window, text="6", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press6)
b6.grid(row=3, column=2)

b6=Button(window, text="-",font=("elephant", 20,"bold"),fg="black",padx=25,bd=10, command=minus)
b6.grid(row=3, column=3)

b6=Button(window, text="7", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press7)
b6.grid(row=4, column=0)

b6=Button(window, text="8", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press8)
b6.grid(row=4, column=1)



b6=Button(window, text="9", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press9)
b6.grid(row=4, column=2)

b6=Button(window, text="*", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=mul)
b6.grid(row=4, column=3)

b6=Button(window, text=chr(67), font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=clr)
b6.grid(row=5, column=0)

b6=Button(window, text="0", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=press0)
b6.grid(row=5, column=1)

b6=Button(window, text="=", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=equal)
b6.grid(row=5, column=2)

b6=Button(window, text="/", font=("elephant", 20,"bold"), fg="black",padx=25,bd=10, command=div)
b6.grid(row=5, column=3)


















