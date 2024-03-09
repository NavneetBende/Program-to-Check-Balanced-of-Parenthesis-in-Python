Check the balance of parenthesis in Python
To check balanced parenthesis is a basic interview question where we are asked to find whether the given string(of brackets) is balanced or not. To do this , the traditional way of doing is using stacks but we can also find by using normal programming techniques. Different brackets are  ( ) , [ ] , { }. Question can be asked on any type of bracket or of all types of brackets.

Program to check the balance of parenthesis in Python
Balanced Parenthesis Problem Python
Missing Braces Program in Python Working:
Step 1: Take the input string
Step 2: Call the isbalanced function
Step 3: This function returns True if the string is balanced, else False
Step 4: This function returns true or false for the string that contains ( )
Python code:- Check the balance of parenthesis in Python
Run
def isbalanced(s):
  c= 0
  ans=False
  for i in s:
    if i == "(": 
     c += 1
    elif i == ")":
     c-= 1
    if c < 0:
     return ans
    if c==0:
     return not ans
  return ans
s="{[]}"
print("Given string is balanced :",isbalanced(s))
Given string is balanced : True
Working:
This approach is to check whether the string is balanced or not in case the string contains several types of brackets like { ( [ ] ) }

Step 1: Take the input string
Step 2: Call the isbalanced function
Step 3: This function returns True if string is balanced , else False
Step 4: This function replaces the set of brackets until the string len becomes zero
Solution 2:
Run
def isbalanced(s):
    while(len(s)!=0):
        s=s.replace('()','')
        s=s.replace('[]','')
        s=s.replace('{}','')
    if(len(s)==0):
        return True
    else:
        return False
s=input("Enter a string of brackets:")
print("Given string is balanced:",isbalanced(s))
Enter a string of brackets: ({{}}){}[]
Given string is balanced : True
