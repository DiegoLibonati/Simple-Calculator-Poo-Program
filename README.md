# Simple-Calculator-Poo-Program

## Getting Started

1. Clone the repository
2. Join to the correct path of the clone
3. Install requirements.txt
4. Use `python simple_calculator.py` to execute program

## Description

I made a simple calculator with python using tkinter as user interface. It is also developed with object oriented programming. This calculator can subtract, multiply, divide and add. You can also use parenthesis, get percentage and perform the c function. Last but not least you can use the comma.

## Feel free to edit my code

If you want to add a new button you need to do this:

```
Button(width=11, height=4, text="TEXT TO SHOW IN SCREEN", relief="flat", bg="#5C6672", command=lambda:self.YOURFUNCTIONNAME()).place(x=X POSITION, y=Y POSITION)
```

## Technologies used

1. Python

## Libraries used

1. Tkinter

## Galery

![Simple-calculator-program](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/simplecalculatorPoo-0.jpg)

![Simple-calculator-program](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/simplecalculatorPoo-1.jpg)

![Simple-calculator-program](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/simplecalculatorPoo-2.jpg)

![Simple-calculator-program](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/simplecalculatorPoo-3.jpg)

## Portfolio Link

`https://diegolibonati.github.io/DiegoLibonatiWeb/#/projects?q=Simple%20calculator%20with%20poo%20program`

## Video

https://user-images.githubusercontent.com/99032604/198900792-216c32f7-b5e8-415e-b7ec-5808dbd6d55f.mp4

## Documentation

The `show()` method will display the value of that button every time a button is touched:

```
def show(self, value):

    if self.entry_value == "ERROR" or self.entry_value == "0":
        self.entry_value = ""
        self.equation.set(self.entry_value)
        self.entry_value += str(value)
        self.equation.set(self.entry_value)
    else:
        self.entry_value += str(value)
        self.equation.set(self.entry_value)
```

The `clear()` method will clear the main screen:

```
def clear(self):
    self.entry_value = ""
    self.equation.set(self.entry_value)
```

The `solve()` method will perform all the mathematical operations on the numbers entered:

```
def solve(self):
    try:
        result=eval(self.entry_value)
        self.equation.set(result)
        self.entry_value = f"{result}"
    except:
        self.entry_value = "ERROR"
        self.equation.set(self.entry_value)
```
