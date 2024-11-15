# Debugging Made Simpler

Recently in Full Stack Development we were taught how to debug and learned about a tool within python that allows you to debug more efficiently. This tool is known as the debugging file in python and it displays the issue with the code as well as the lines that are causing the conflict to occur. This helps speed up the process of going through all your code to find the issue as well as speeding up the whole process of coding as you are able to get more done correctly knowing that your code works as intended.
<br>
One of the examples of problems we encountered were:

```py
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)

```
The problem with this is the count variable does not increase when a space is input. In order to fix this code we would have to in line 5 add a space between the quotes in order for the code to detect the space.
<br>
Another example was:
<img src="/_post/debugger.png" alt= "2nd Example of debugging">
The problem presented here is the n is being interpreted as a string and not an integer the code also does not interpret the even numbers as being even and it stops working before the n which leaves out the final number. I solved this issue on line 2 the int() would have to be used in order to make n an integer then changed the < sign to == on line 5. Lastly on line 13 +1 was added so that the final number isn't left out.
<br>
After debugging the correct code would be:

```py
print("give me a number")


n = int(input())+1


for num in range(1, n):
   if num % 2 == 0:
       print(num, "is even.")
   else:
       print(num, "is odd.")

```
<br>
For the 3rd example the code was meant to calculate the factorial of a given number.
<br>
Incorrect Code Below:

```py
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result)

```

The code didn't detect when -1 was input and also doesn't print the 4th line. Additionally the code only calculates the factorial of 1 despite user input.
<br>
In order to fix it you would have to change the -1 on the third line to a 0. This is done in order to include -1 and any negative integers as user input and allow for the code to carry out as intended. Then on line 6 the initial result would have to be set as equal to the input in order for the for loop to calculate the user's input instead of 1.
<br>

The last example was meant to prompt the user to input the correct password but limit them to 3 attempts.
<br>
The code below is incorrect code:

```py
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break

```
The issue with this code is that it does not print the words "Correct Password" when the password is correct as well as allowing the user more than 3 attempts and not stopping once the conditions are met which is the inputting of the correct password.
<br>
The debugging tool helped with determining that line 8 should be changed from "incorrect_password" to "correct_password" as this will allow the code to compare the user's input with the actualy correct password and will print correct password if it is in fact correct. Then to fix the amount of attempts the greater than sign would have to be replaced with the == on line 13 as this will grant exactly 3 attempts. 
<br>

Overall the debugging tool helps save more time when coding by allowing us to actually create functional code and check over it opposed to us doing it on our own and perhaps missing something in our code.