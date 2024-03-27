# -Tkinter-A № 1
from tkinter import *
from tkinter import ttk


def show_message():
    label["text"] = "Hello world"


root = Tk()
root.title("Hello world!")
root.geometry("250x200")

btn = ttk.Button(text="Click", command=show_message)
btn.pack(anchor=NW, padx=6, pady=6)

label = ttk.Label()
label.pack(anchor=NW, padx=6, pady=6)

root.mainloop()

# -Tkinter-A № 2

import tkinter as tk

def summ():
    result = int(entry1.get()) + int(entry2.get())
    result_label.config(text=result)

root = tk.Tk()
root.title("Калькулятор")
root.geometry("250x200")

entry1 = tk.Entry(root)
entry1.pack(padx=6, pady=6)

entry2 = tk.Entry(root)
entry2.pack(padx=6, pady=6)

calculate_button = tk.Button(root, text="=", command=summ)
calculate_button.pack(padx=6, pady=6)

result_label = tk.Label(root)
result_label.pack()

root.mainloop()

# -Tkinter-A № 3

import tkinter as tk
import random


def circle():
    x = random.randint(0, 300)
    y = random.randint(0, 300)

    canvas.create_oval(x, y, x + 50, y + 50)


root = tk.Tk()
root.title("Случайный круг")

canvas = tk.Canvas(root, width=300, height=300)
canvas.pack()

button = tk.Button(root, text="Создать круг", command=circle)
button.pack()

root.mainloop()
