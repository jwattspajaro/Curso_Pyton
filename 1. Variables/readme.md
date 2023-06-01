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

