### Arduino
**Arduino** is a circuit board programmable from a computer. It is an **open source** project, meaning anyone with a computer, an Internet connection, and coding knowledge can help out with its development. To program for the board, you’ll need to know how to code **Wiring**, a programming language based on the widely used C. This documentation is here to get you started on that.

### Functions
**Functions** are the building blocks of a program. Most will look like this:

```Arduino
output function(parameter) {
    procedure
}
```

`output`: One word to tell Arduino what kind of information it can expect this function to evaluate to. Evaluation is similar to reducing a fraction to simplest terms: Arduino runs all the code between the brackets and may or may not end up with a leftover piece of info. For some functions, you won’t need to include this at all; for others, you’ll need to make the output `void`, meaning “nothing”, so Arduino knows it won’t get any info out of this function.

`function`: The name of the function. It lets Arduino know what it’s going to do with the parameters.

`parameter`: A fancy word for “what has to be true for this function to run”. Parameters are usually in the form of logical statements—things that can be either true or false. More on how these work later in the documentation.

`procedure`: What Arduino does if the parameters are true. You’ll learn what to write here in the next section.

Always make sure to put `{`brackets`}` around the code in the function or your code will break! In addition, although your code will work just fine if you don’t tab in the code between the brackets or put the brackets on a new line like I did, these practices will help you read through your code and prevent many common errors like forgetting brackets and parentheses.

### Basic Functions
There are a few functions every Wiring program must have in order to run in the first place.

The first function you’ll need to know is `setup()`. This function takes no parameters; whatever is between the brackets will run every time you press the “RESET” button on your Arduino board, so that’s why there’s nothing between the parentheses. You’ll need to include `void` as the output for this function to work: `void setup()`.

The second function all Wiring programs must have is `loop()`. This is the main body of your program, and it will run over and over again as long as Arduino is connected to a power source. Like `setup()`, `loop()` requires `void` as its output to work: `void loop()`.

Here is a basic outline of a Wiring program:

```Arduino
void setup() {

}

void loop() {

}
```

Of course, you’ll need to add code to run between the brackets before your program runs. That’s where statements come in.

### Statements
When giving someone instructions on how to do something, you give them steps to proceed through in order in the form of sentences. Likewise, you’ll use statements to tell Arduino how to accomplish a task. Statements make up the procedures that functions run based on the truth value of their parameters. They come in two forms:

```Arduino
statement(parameter);
```

and

```Arduino
statement;
```

Just as in functions, the parameters go between the parentheses. However, parameters to statements usually tell Arduino _how_ to run the statement, not _whether_ to run the statement. Of course, there are exceptions to every rule, but get used to parameters that tell statements how to run in Arduino.

Don’t forget to put a semicolon`;` after each statement!

### Common Functions
The first function you’ll probably use a lot is `if()`. The truth value of what you put between the parentheses of an if statement tells Arduino whether to run what’s between the following brackets.

If you want to run code over and over again, if statements won’t quite cut it. You’ll have to use `while()`. It’s basically an if statement that runs over and over again as long as its parameters are true. You might use a while loop to perform an action over and over again or keep Arduino from moving on to the next statement until

Be careful with while statements! If your procedure and/or parameters are too intensive to run and your parameters stay true for a while (no pun intended), Arduino could break.

This is one of the many uses for the statement `delay()`. The parameter of a delay statement should evaluate to a whole number in milliseconds, thousandths of a second. Add `delay(10);` at the end of every loop you use, including while loops, to give Arduino a break after a hard day’s work—or, rather, a hard second’s work.