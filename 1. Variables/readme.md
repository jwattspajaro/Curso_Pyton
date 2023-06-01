### Creating Code with Python
- VS Code is a special type of text editor that is called a compiler. At the top, you’ll notice a text editor and, at the bottom you will see a terminal where you can execute commands.
- In the terminal, you can execute code hello.py to start coding.
- In the text editor above, you can type print("hello, world"). This is a famous canonical program that nearly all coders write during their learning process.
- In the terminal window, you can execute commands. To run this program, you are going to need to move your cursor to the bottom of the screen, clicking in the terminal window. You can now type a second command in the terminal window. Next to the dollar sign, type python hello.py and press the enter key on your keyboard.
- Recall, computers really only understand zeros and ones. Therefore, when you run python hello.py, python will interpret the text that you created in hello.py and translate it into the zeros and ones that the computer can understand.
- The result of running the python hello.py program is hello, world.
- Congrats! You just created your first program.


#### Functions
- Functions are verbs or actions that the computer or computer language will already know how to perform.
- In your hello.py program, the print function knows how to print to the terminal window.
- The print function takes arguments. In this case, "hello, world" are the arguments that the print function takes.

#### Bugs
-+ Bugs are a natural part of coding. These are mistakes, problems for you to solve! Don’t get discouraged! This is part of the process of becoming a great programmer.
Imagine in our hello.py program that accidentally typed print("hello, world" notice that we missed the final ) required by the compiler. If I purposefully make this mistake, you’ll the compiler will output an error in the terminal window!
- Often, the error messages will inform you of your mistake and provide you clues on how to fix them. However, there will be many times that the compiler is not this kind.
Improving Your First Python Program
- We can personalize your first Python program.
In our text editor in hello.py we can add another function. input is a function that takes a prompt as an argument. We can edit our code to say
``` Python
    input("What's your name? ")
    print("hello, world")
```
Variables
- A variable is just a container for a value within your own program.
In your program, you can introduce your own variable in your program by editing it to read

``` Python
    name = input("What's your name? ")
    print("hello, world")
``` 

- Notice that this equal = sign in the middle of name = input("What's your name? ") has a special role in programming. This equal sign literally assigns what is on the right to what is on the left. Therefore, the value returned by input("What's your name? ") is assigned to name.

If you edit your code as follows, you will notice an error

``` Python
    name = input("What's your name? ")
    print("hello, name")
``` 
-The program will return hello, name in the terminal window regardless of what the user types.
Further editing our code, you could type
``` Python

    name = input("What's your name? ")
    print("hello,")
    print(name)
    
``` 
- The result in the terminal window would be

``` Python
        What's your name? David
        hello
        David
``` 

- We are getting closer to the result we might intend!

- You can learn more in Python’s documentation on [data types](https://docs.python.org/3/library/datatypes.html).

#### Comments
- Comments are a way for programmers to track what they are doing in their programs and even inform others about their intentions for a block of code. In short, they are notes for yourself and others that will see your code!
- You can add comments to your program to be able to see what it is that your program is doing. You might edit your code as follows:

# Ask the user for their name

``` Python
        name = input("What's your name? ")
        print("hello,")
        print(name)

``` 
- Comments can also serve as to-do list for you.

#### Pseudocode
- Pseudocode is an important type of comment that becomes a special type of to-do list, especially when you don’t understand how to accomplish a coding task. For example, in your code, you might edit your code to say:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Print hello
        print("hello,")

        # Print the name inputted
        print(name)

``` 
#### Further Improving Your First Python Program
- We can further edit our code as follows:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Print hello and the inputted name
        print("hello, " + name)
``` 
- It turns out that some functions take many arguments.
- We can use a comma , to pass in multiple arguments by editing our code as follows:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Print hello and the inputted name
        print("hello,", name)
``` 
The output in the terminal, if we typed “David” we would be hello, David. Success.

#### Strings and Paremeters
- A string, known as a str in Python, is a sequence of text.
- Rewinding a bit in our code back to the following, there was a visual side effect of having the result appear on multiple lines:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")
        print("hello,")
        print(name)
```
- Functions take arguments that influence their behavior. If we look at the documentation for print you’ll notice we can learn a lot about the arguments that the print function takes.
- Looking at this documentation, you’ll learn that the print function automatically include a piece of code end='\n'. This \n indicates that the print function will automatically create a line break when run. The print function takes an argument called end` and the default is to create a new line.
- However, we can technically provide an argument for end ourselves such that a new line is not created!
- We can modify our code as follows:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")
        print("hello,", end="")
        print(name)
``` 
By providing end="" we are over-writing the default value of end such that it never creates a new line after this first print statement. Providing the name as “David”, the output in the terminal window will be hello, David.

- Parameters, therefore, are arguments that can be taken by a function.

- You can learn more in Python’s documentation on print.

#### A small problem with quotation marks

- Notice how adding quotation marks as part of your string is challenging.
- print("hello,"friend"") will not work and the compiler will throw an error.
- Generally, there are two approaches to fixing this. First, you could simply change the quotes to single quote marks.
- Another, more commonly used approach would be code as print("hello, \"friend\""). The backslashes tell the compiler that the following character should be considered a quotation mark in the string and avoid a compiler error.

#### Formatting Strings
- Probably the most elegant way to use strings would be as follows:
``` Python
        # Ask the user for their name
        name = input("What's your name? ")
        print(f"hello, {name}")
```
#### Notice the f in print(f"hello, {name}"). This f is a special indicator to Python to treat this string a special way, different than previous approaches we have illustrated in this lecture. Expect that you will be using this style of strings quite frequently in this course.
More on Strings
- You should never expect your user will cooperate as intended. Therefore, you will need to ensure that the input of your user is corrected or checked.
- It turns out that built into strings is the ability to remove whitespace from a string.
- By utilizing the method strip on name as name = name.strip(), it will strip all the whitespaces on the left and right of the users input. You can modify your code to be:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Remove whitespace from the str
        name = name.strip()

        # Print the output
        print(f"hello, {name}")
```
Rerunning this program, regardless of how many spaces you type before or after the name, it will strip off all the whitespace.

- Using the title method, it would title case the user’s name:
- 
``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Remove whitespace from the str
        name = name.strip()

        # Capitalize the first letter of each word
        name = name.title()

        # Print the output
        print(f"hello, {name}")
```        
- By this point, you might be very tired of typing python repeatedly in the terminal window. You cause us the up arrow of your keyboard to recall the most recent terminal commands you have made.
- Notice that you can modify your code to be more efficient:

``` Python
        # Ask the user for their name
        name = input("What's your name? ")

        # Remove whitespace from the str and capitalize the first letter of each word
        name = name.strip().title()

        # Print the output
        print(f"hello, {name}")
``` 
- This creates the same result as your previous code.

#### We could even go further!

``` Python
        # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
        name = input("What's your name? ").strip().title()

        # Print the output
print(f"hello, {name}")
``` 
- You can learn more about strings in Python’s documentation on str

#### Integers or int
- In Python, an integer is referred to as an int.
- In the world of mathematics, we are familiar with +, -, *, /, and % operators. That last operator % or modulo operator may not be very familiar to you.
- You don’t have to use the text editor window in your compiler to run Python code. Down in your terminal, you can run python alone. You will be presented with >>> in the terminal window. You can then run live, interactive code. You could type 1+1 and it will run that calculation. This mode will not commonly be used during this course.
- Opening up VS Code again, we can type code calculator.py in the terminal. This will create a new file in which we will create our own calculator.
- First, we can declare a few variables.

``` Python
        x = 1
        y = 2

        z = x + y

        print(z)

``` 
Naturally, when we run python calculator.py we get the result in the terminal window of 3. We can make this more interactive using the input function.

``` Python
        x = input("What's x? ")
        y = input("What's y? ")

        z = x + y

        print(z)

        print(z)

``` 
- Running this program, we discover that the output is incorrect as 12. Why might this be?
- Prior, we have seen how the + sign concatenates two strings. Because your input from your keyboard on your computer comes into the - compiler as text, it is treated a string. We, therefore, need to convert this input from a string to an integer. We can do so as follows:

``` Python
        x = input("What's x? ")
        y = input("What's y? ")

        z = int(x) + int(y)

        print(z)
``` 

The result is now correct. The use of int(x), is called “casting” where a value is temporarily changed from one type of variable (in this case a string) to another (here, an integer).

- We can further improve our program as follows:

``` Python
        x = int(input("What's x? "))
        y = int(input("What's y? "))

        print(x + y)
        
``` 
- This illustrates that you can run functions on functions. The most inner function is run first, and then the outer one is run. First, the input function is run. Then, the int function.

- You can learn more in Python’s Documenation of [int](https://docs.python.org/3/library/functions.html?highlight=float#int).

#### Readability Wins
- When deciding on your approach to a coding task, remember that one could make a reasonable argument for many approaches to the same problem.
- Regardless of what approach you take to a programming task, remember that your code must be readable. You should use comments to give yourself and others clues about what your code is doing. Further, you should create code in a way that is readable.

#### Float Basics
- A floating point value is a real number that has a decimal point in it, such as 0.52.
- You can change your code to support floats as follows:

``` Python
        x = int(input("What's x? "))
        y = int(input("What's y? "))

        print(x + y)
``` 
- This change allows your user to enter 1.2 and 3.4 to present a total of 4.6.

- Let’s imagine, however, that you want to round the total to the nearest integer. Looking at the Python documentation for round you’ll see that the available arguments are round(number[n, ndigits]). Those square brackets indicate that something optional can be specified by the programmer. Therefore, you could do round(n) to round a digit to its nearest integer. Alternatively, you could code as follows:

``` Python
        # Get the user's input
        x = float(input("What's x? "))
        y = float(input("What's y? "))

        # Create a rounded result
        z = round(x + y)

        # Print the result
        print(z)
``` 

The output will be rounded to the nearest integer.

- What if we wanted to format the output of long numbers? For example, rather than seeing 1000, you may wish to see 1,000. You could modify your code as follows:

``` Python
        # Get the user's input
        x = float(input("What's x? "))
        y = float(input("What's y? "))

        # Create a rounded result
        z = round(x + y)

        # Print the formatted result
        print(f"{z:,}")
``` 

Though quite cryptic, that print(f"{z:,}") creates a scenario where the outputted z will include commas where the result could look like 1,000 or 2,500.

#### More on Floats
- How can we round floating point values? First, modify your code as follows:

``` Python
        # Get the user's input
        x = float(input("What's x? "))
        y = float(input("What's y? "))

        # Calculate the result
        z = x / y

        # Print the result
        print(z)

```
When inputting 2 as x and 3 as y, the result z is 0.6666666666 seemingly going on to infinite as we might expect.

- Let’s imagine that we want to round this down, we could modify our code as follows:

``` Python
        # Get the user's input
        x = float(input("What's x? "))
        y = float(input("What's y? "))

        # Calculate the result and round
        z = round(x / y, 2)

        # Print the result
        print(z)

```

As we might expect, this will round the result to the nearest two decimal points.

- We could also use fstring to format the output as follows:


``` Python
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result
z = x / y

# Print the result
print(f"{z:.2f}")

```

This cryptic fstring code displays the same as our prior rounding strategy.

- You can learn more in Python’s documentation of [float](https://docs.python.org/3/library/functions.html?highlight=float#float).

Def
Wouldn’t it be nice to create our own functions?
Let’s bring back our final code of hello.py by typing code hello.py into the terminal window. Your starting code should look as follows:
