# Evaluating conditions and conditional statement
A conditional statement evaluates an expression and executes instructions depending on the outcome of the evaluation. Conditionals depend on operators to evaluate if an expression is true or false. A condition and selection are not the same thing. A condition asks a question. A selection processes the answer.
Look at the following image to understand how the conditional statement work 
![image](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/If-Then-Else-diagram.svg/1920px-If-Then-Else-diagram.svg.png)
Lets take a simple example of how exactly it is work
**this file helps us to understand conditionals in Python.**
**what do you think the output will be when you execute these instructions?**

a = 5
b = "bar"

if a == 5:
    print("Yes, the variable a has been assigned to the value 5.")
else:
    print("No, the variable a has not been assigned to the value 5.")

 **what do you think the output will be when you execute these instructions?**

a = 5
b = "bar"

if b == "foo":
     print("yes, the variable b has been assigned the value foo")
else:
     print("no, the variable b has been assigned to some other value than foo.")



# For loops
A for loop enables a particular set of conditions to be executed repeatedly until a condition is satisfied. Imagine a situation where you would have to print numbers from 1 to 100. What would you do? Will you type in the printf command a hundred times or try to copy/paste it? This simple task would take an eternity. Using a for loop you can perform this action in three statements. This is the most basic example of the for loop. It can also be used in many advanced scenarios depending on the problem statement.
Check out the flowchart of a for loop to get a better idea of how it looks:
  ![flowchart](https://study.com/cimages/multimages/16/a4bea689-4e19-4e9d-bf71-433c13a2aa68_for_0.png)


# Syntax of a For Loop

1- for (initialization statement; test expression; update)

2-{statement 
 
3-// statements

4-}

let's see a quick example of how *for loop* actually work
for (var counter = 1; counter < 5; counter++) {
    console.log('Inside the loop:' + counter);
}
console.log('Outside the loop:' + counter);

#### the outputs for this example will be:
**Inside the loop:1**

**Inside the loop:2**

**Inside the loop:3**

**Inside the loop:4**

**Outside the loop:5**

