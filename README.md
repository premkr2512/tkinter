# tkinter Calculator

import tkinter as t      $ import the tkinter module
windows = t.Tk("hello every one")     #create the screen
windows.title("Tkinter")              #title
equation =t.StringVar()
calculation =t.Label(windows,textvariable = equation)
equation.set("23+24")
calculation.grid(columnspan = 4)
equa = ""
def btn_press(num):
    global equa
    equa = equa +str(num)
    equation.set(equa)
def press_equal():
    global equa
    total = str(eval(equa))
    equation.set(total)
    equa= ""
def press_C():
    global equa
    equa = ""
    equation.set("")

button1 = t.Button(windows,text ="1",command = lambda:btn_press(1))
button1.grid(row = 1,column = 0)
button2 = t.Button(windows,text="2",command = lambda:btn_press(2))
button2.grid(row = 1,column = 1)
button3 = t.Button(windows,text ="3",command = lambda:btn_press(3))
button3.grid(row = 1,column = 2)
button4 = t.Button(windows,text="4",command = lambda:btn_press(4))
button4.grid(row = 2,column = 0)
button5 = t.Button(windows,text ="5",command = lambda:btn_press(5))
button5.grid(row = 2,column = 1)
button6 = t.Button(windows,text="6",command = lambda:btn_press(6))
button6.grid(row = 2,column = 2)
button7 = t.Button(windows,text ="7",command = lambda:btn_press(7))
button7.grid(row = 3,column = 0)
button8 = t.Button(windows,text="8",command = lambda:btn_press(8))
button8.grid(row = 3,column = 1)
button9 = t.Button(windows,text ="9",command = lambda:btn_press(9))
button9.grid(row = 3,column = 2)
button0 = t.Button(windows,text="0",command = lambda:btn_press(0))
button0.grid(row = 4,column = 2)
button_equal = t.Button(windows,text="=",command = lambda:press_equal())
button_equal.grid(row =4,column = 1)
button_devide = t.Button(windows,text="/",command = lambda:btn_press("/"))
button_devide.grid(row =4,column = 0)
button_add = t.Button(windows,text="+",command = lambda:btn_press("+"))
button_add.grid(row =4,column = 3)
button_clear = t.Button(windows,text="C",command = lambda:press_C())
button_clear.grid(row =3,column = 3)
button_sub = t.Button(windows,text="-",command = lambda:btn_press("-"))
button_sub.grid(row =2,column = 3)
button_mul = t.Button(windows,text="*",command = lambda:btn_press("*"))
button_mul.grid(row =1,column = 3)
windows.mainloop()
