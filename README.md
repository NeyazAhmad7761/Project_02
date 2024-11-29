# Project_02

### **Documentation for the Simple Calculator Project**

---

#### **Overview**
This project is a simple calculator application developed using Python and the Tkinter library. It is able to carry out basic arithmetic operations, which include addition, subtraction, multiplication, and division. The calculator has a graphical user interface (GUI) with buttons for numbers, operators, and functionality such as clearing the input or calculating the result.

---

#### **Key Features**
1. **Graphical Interface**: The application has a pretty graphical interface built with Tkinter.
2. **Arithmetic Operations**: The program supports basic operations such as:
   - Addition (`+`)
   - Subtraction (`-`)
   - Multiplication (`*`)
   - Division (`/`)
3. **Clear Functionality**: There is an option to clear the input field.
4. **Error Handling**: If there is an invalid expression, the program displays an error message.
5. **Real-time Input Display**: Pressing buttons updates the input field.

---

#### **Code Description**

#### 1. **Imports**
 The program imports the `tkinter` module to create the GUI:
```python
from tkinter import *
```

#### 2. **Global Variables**
- `expression`: A string that stores the current mathematical expression.
- `equation`: A `StringVar` that binds the input field to dynamically update based on the expression.

#### 3. **Functions**
- **`press(num)`**:
  - Appends the pressed button's value (`num`) to the global `expression`.
  - Updates the input field using `equation.set(expression)`.

- **`equalpress()`**:
- It calculates the mathematical expression in `expression` by applying the `eval()` method available in Python.
  - The outcome is reflected back into the input box.
  - Catches any errors due to wrong input and renders `"error"`.
 - ***`clear()`***
  - Sets `expression` back to an empty string
  - Clears out the input box

=====4. **GUI MAIN SCREEN**
- **Master Root Window**: Generated via `Tk()` and established a title, size and color.
- **Input Field**: One-line `Entry` widget that's tied to `equation` to display the expression entered.
- **Buttons**:
  - The number buttons (`0` through `9`) send a number to `press(num)`.
  - The operator buttons (`+`, `-`, `*`, `/`) send the chosen operator to `press(operator)`.
  - The special buttons:
    + **Equal (`=`)**: Presses `equalpress()` to calculate the answer.
    + **Clear**: Calls `clear()` to clear the input.
- **Decimal (`.`)**: Adds a decimal point to the expression.

##### 5. **Button Layout**
The buttons are arranged in a grid layout using `grid(row, column)`.

Example:
```python
button1 = Button(gui, text=' 1 ', fg='white', bg='black',
                 command=lambda: press(1), height=1, width=7)
button1.grid(row=2, column=0)
```
---

#### **How to Use**
1. **Run the Program**:
- Run the script in a Python environment with Tkinter installed.
2. **Input Numbers and Operations**:
   Click on the number buttons to input digits.
   Use the operator buttons (+, -, *, /) for arithmetic operations.
3. **Get the Result**:
   Press the = button to calculate and display the result.
4. **Clear the Input**:
- Clear button to clear the calculator.

---

#### **Possible Enhancements**
1. **More Functions**:
   Implement more mathematical functions (e.g., square root, percentage, etc.).
2. **Improved Error Messages**:
   Show error messages with descriptions (e.g., "Division by zero").
3. **Mobile-Friendly**:
   Make the layout more responsive and user-friendly on various screen sizes.
4. **Input from Keyboard**:
- Allow users to input numbers and operators using the keyboard.


---

#### **Conclusion**
This project demonstrates the creation of a basic calculator using Python and Tkinter. It provides a hands-on example of working with GUIs and user input in Python. The project is modular and can be extended with additional features as needed.
