# error Handling & Debugging
JavaScript sometimes count as hard langauge to write and therefore , the programmer might make  many errors while he is writting the code. As you know that JS excute the code line by line so if there is an error in line number one for example the others lines will not excuted so it is so important to know where is the error and fix it. At first you need to know the excution order of a code to understand that some part of a code depend on other to be excuted .


After that you need to know the scope of each variable exist in the code. there are mainly two kindes of scope:

1- Global scope : like a scope of a variable written iside a JS file but not inside any function. this variable can be used in either inside or outside any function

2- Function-level-scope: like a scope of a variable written inside a function. this variable can not be used outside that function.



## Error objects
 Error objects can help you find where your mistakes are
and browsers have tools to help you read them. When an Er ror object is created, it will contain the
following properties:

- the name of the error

- the file number 
- the line that hold the error


When there is an error, you can see all of this
information in the JavaScript console 
of the browser.


# Debugging 
  the process that involves finding errors and removing them from your program. 

  Before solving the error we have to know the root cause of that error. Errors can result from:

  - Including language features or syntax that the scripting engine does not support within the script.

- Failing to correctly implement the intent of the program or some particular algorithm. This occurs when, although code is syntactically correct and does not generate any errors, it produces behavior or results other than those you intend.

- Including components that contain bugs themselves. In this case, the problem lies with a particular component, rather than with your script, which “glues” the components together.


After you find the cause of the error , you can solve it simply by searching online for the best solution based in your code functionality.




