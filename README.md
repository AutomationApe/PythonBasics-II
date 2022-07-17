# PythonBasics-II
Continuation of PythonBasics 

Conditional logic
    
    Conditional logic allows us to have more control over the flow/execution of our program.
    Conditional logic allows for us to set code to execute if certain conditions are met.
    ex:
    
      is_old = True
      is_licensed = True
      
      if is_old:
        print("you are old enough to drive!")
       
      ^This is an if statement, they allow for us to run code only if a condition is met. In this case, is_old is true, which means the code executes.

      there is also an else statement, to be used in conjunction with the if statement. The else statement provides another path for the code
      to follow if the conditions in the if statement are not met.
      ex:
      
      is_old = True
      is_licensed = True
      
      if is_old:
        print("you are old enough to drive!")
      else:
        print("you are not old enough to drive.")
        
      there is also an elif statement (else if), that provides another specific condition and code to be executed if it is met.
      ex:
      
      is_old = True
      is_licensed = True
      
      if is_old:
        print("you are old enough to drive!")
      elif is_licensed:
        print("You can drive now!")
      else:
        print("You are not old enough to drive.")
        
      You can also have if statements with multiple expressions, meaning multiple conditions to be met.
      ex:
      
      if is_old and is_licensed:
       * do stuff*
       
      In this case, both is_old and is_licensed must evaluate to true for the code to execute.
      
      There is also the 'or' operator that can be used to state that code can execute if atleast one condition stated has been met.
      ex:
      
      if is_old or is_licensed:
        * do stuff *
        
For more information on if...else:
https://www.w3schools.com/python/python_conditions.asp

Ternary Operators

    Ternary operators are a shorthand for if-else statements that allow for cleaner code.
    
    They allow for if-else statements, in certain conditions, to be created in one line.
    ex: 
    
        is_friend = true
        can_message = "Messaging is allowed" if is_friend else "Messaging is not allowed"
        
    As you can see, the message to the left will execute if 'is_friend' is true, while the message on the right will execute if the conditon
    is false.
    
Short Circuiting

    Short circuiting is the ability of the interpreter to be more performant by evaluating the first parts of certain conditions
    and deciding if it needs to evaluate the second part of the condition.
    
    For example, let's say you have an if statement like this one:
    if is_user or is_admin:
        print("Welcome")
        
    The interpreter can evaluate the first condition 'is_user', and if it evaluates to true, the interpreter knows it can skip evaluating the 
    other condition as the 'or' operator indicates it only needs to satisfy one of the conditions.
    
Logical & Conditional Operators

    Logical operators are incredibly useful as they allow for the combination of conditional statemtents.
    
    Conditional operators are used to compare two values.
    
    Logical Operatrors include:
        and - returns true if the conditions provided are true; ex: if x == red and y == blue:
        or - returns true if atleast one of the conditions are true; ex: if x == red or y == blue:
        not - reverses the result, returning the opposite of the evaluation; ex: not(x == red)
        
    Conditional Operators include:
        '==' - equal; ex: if x == y
        '!=' - not equal; ex: if x != y
        '>' - greater than; ex: if x > y
        '<' - less than; ex: if x < y
        '>=' - greater than or equal to; if x >= y
        '<=' - less than or equal to; if x <= y
        
For more information on operators:
https://www.w3schools.com/python/python_operators.asp

== vs is

    '==' is a comparison operator, meaning it targets the value of a variable rather than the type.
    ex: 1 == 1 -> evaluates to true
    
    'is' is an identity operator, meaning it targets the memory location of a variable to determine if it is the same object.
    ex: a is b -> evaluates to false
    
    '==' is indicative of an evaluation of the value itself.
    
    'is' is indicative of an evaluation of the location in memory where a value is stored.

For Loops

    Loops are very powerful tools in programming as they allow us to execute lines of code for a certain amount of iterations or until a certain
    condition is met.
    
    For loops
    ex:  for item in items:
      
    The idea of for loops is that you are providing a variable to iterate over an iterable (something with a group of items)
    of some sort. For example, let's say you have a list of 10 fruits. 
    You could use a for loop to iterate over all 10 items and print them out. ex: for fruit in fruits:
                                                                                    print(fruit)
    You can also nest loops. Meaning, you can have a loop inside of a loop.
    The way that this works is the outer loop will execute first, then enter the inner loop and execute through its entirety,
    before exiting the inner loop, and moving onto the next iteration of the outer loop.
    ex:
    
        numbers = [1,2,3]
        letters = [a,b,c]
    
        for number in numbers:
            for letter in letters:
                print(number,letter)     ->   This results in the following:
                                                   1a
                                                   1b
                                                   1c
                                                   2a
                                                   2b
                                                   2c
                                                   etc.

For more information on For Loops:
https://www.w3schools.com/python/python_for_loops.asp


Iterable
    
    An iterable can be a list, dictionary, tuple, set, string, etc.
    
    These are iterables because they can be iterated over, we can go one by one over each item in the collection.
    
    Iterable is the noun, it is a thing.
    
    To iterate is the action, we iterate over iterables.
    
Enumerate

    The enumerate function is a useful function as it allows you to iterate over a collection and return the item and the index of said item.
    ex:
        for i, char in enumerate("Hello"):
            print(i, char)
            
    This would return the indices and letters inside hello, [0] h, [1] e, so on so forth
    
While Loops

    While loops are another powerful form of loops, as they allow for code to execute until a certain condition is no longer met.
    ex:
    
        i = 0
        while i < 50:
            print(i)
            i += 1
            
    This will print all numbers between 0 to 49. It is important to note that you must include 'i += 1' or something to this effect, as this
    ensures that after each iteration, i is incremented by one, and the loop will not be an infinite loop.
    
For more information on While Loops:
https://www.w3schools.com/python/python_while_loops.asp

Break, Continue, Pass
    
    The break, continue, and pass keywords are all forms of control flow. 
    
    The break statement, allows for us to stop a loop even if the while condition is true.
    ex:
    
        i = 0
        while i < 6:
            print(i)
            if i == 3:
                break
            i += 1
    This code would print 1 to 6, but the if statement executes a break statement upon reaching the number 3. Therefore, the loop will exit at number 3.
    
    The continue statement allows us to stop a loop at the current iteration, and continue with the next.
    ex:
    
        i = 0
        while i < 6:
            i += 1
            if i == 3:
                continue
            print(i)
    This code would print 1 to 6, but the if statement executes a continue statement upon reaching the number 3. Therefore, the loop will skip printing
    the number 3, and instead will print numbers 1, 2, 4, 5, and 6.
    
    The pass statment is rarely used, but essentially tells the code to move to the next line. It can be useful as a placeholder.
    ex:
    
       for item in my_list:
        pass
        
    This code will do absolutely nothing but can act as a placeholder while you are designing your loop.
    
Functions

    Functions are powerful tools in programming that allow us to write instructions to execute in order to complete a task. Print() is a function.
    
    We can also create our own functions.
    ex:
    
        def say_hello():
            print("Hello!")
            
    We would make use of this function as follows:
        say_hello()
        
    Functions are great thanks to their ability to be reused multiple times. Rather than writing something over and over again, we could define
    a function and call the function instead. 
    
    * Functions should do one thing really well *
    * Functions should typically return something *
   
For more information on functions:
https://www.w3schools.com/python/python_functions.asp

Arguments VS Parameters

    The power of functions beyond their reusability, is their ability to be dynamic. For example, we can give a function parameters inside of the
    brackets, to expand their utility.
    
    For example:
    
        def say_hello(name,emoji):
            print(f"Hello {name}! {emoji})
            
    The arguments are the actual values provided to the functions, saved as the parameters.
    ex:
    
        say_hello('Jaime', '👋')
        
        This would result in the following: Hello Jaime! 👋 
        
    There is such thing as keyword arguments, which allow us to explicitly set our arguments to our parameters, ex: 
    say_hello(emoji="👋", name="Jaime")
    
    Notice that in the parameters, name comes before emoji but in the arguments, we listed the emoji first. Without the keywords,
    the emoji would have been saved to the name parameter and would not have followed the desired format.
    
    We can also set defaults in our parameters in the function definition. This enables us to have default values to fall back on should a function
    be called without argument values. ex:
    
    def say_hello(name = "Darth Vader", emoji = "🚀")
    
    If we call say_hello(), the default values will be output in the message.
    
Return

    The return keyword commands a function to output something when called.
    
    This is useful in many ways, one of which when defining a function that does some form of math.
    ex:
    
        def sum(num1, num2):
            return num1 + num2
          
        print(sum(10,5)) -> outputs: 15
    
    * Return ends the function flow *
        
 Methods vs Functions
 
    example of functions:
    print()
        
    example of methods:
    message = "hello"
    
    message.capitalize()
    
    
    The difference is that methods are owned by objects, therefore, when calling a method, one must call the object first and then the method they want
    using the '.' accessor. 
  
Docstrings

    Docstrings allow for a programmer to comment inside of our function in a way that provides information about our function.
    
    ex:
    
        def test(a):
            '''
            Info: This function tests and prints paramater a
            '''
            print(a)
            
        We can see the information in a variety of ways, such as hovering over the function in our IDE, calling the help function, or using
        a dunder method as follows:
        
        print(test.__doc__) -> outputs the docstring we wrote in our test function
        
For more information on docstrings:
https://www.programiz.com/python-programming/docstrings


    
