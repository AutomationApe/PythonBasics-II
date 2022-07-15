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

      
