# 📐 Taylor Series Using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## 💻 PROGRAM:

def taylor_series(x, n):

    if n == 0:    
 
        return 1
        
    else:
    
        return (x**n / factorial(n)) + taylor_series(x, n-1)  # Recursive case

def factorial(num):

    if num == 0 or num == 1:
    
        return 1
        
    else:
    
        return num * factorial(num - 1)


x = float(input("Enter the value of x: "))

n = int(input("Enter the number of terms n: "))


result = taylor_series(x, n)


print(f"Taylor series sum for x={x} and n={n} terms is {result}")


## OUTPUT
Enter the value of x: 2

Enter the number of terms n: 5

Taylor series sum for x=2.0 and n=5 terms is 7.266666666666667

Enter the value of x: 1

Enter the number of terms n: 4

Taylor series sum for x=1.0 and n=4 terms is 2.708333333333333


## RESULT
The program successfully evaluates the Taylor Series for a given x and n using recursion, with factorial computed recursively as well.
