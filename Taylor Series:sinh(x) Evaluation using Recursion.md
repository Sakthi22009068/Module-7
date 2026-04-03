# 📐 Taylor Series:sinh(x) Evaluation using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## 🧠 ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## 💻 PROGRAM:

def fact(n):

    if n <= 1:
    
        return 1
        
    else:
    
        return n * fact(n - 1)


def sinh(x, n):

    if n == 0:  # Base case
    
        return x
        
    else:
    
        return (x**(2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)  # Recursive case


x = float(input("Enter the value of x: "))

n = int(input("Enter the number of terms n: "))


result = sinh(x, n)


print(f"sinh({x}) using {n} terms is {result}")


## OUTPUT
Enter the value of x: 2

Enter the number of terms n: 5

sinh(2.0) using 5 terms is 4.055198593287875

Enter the value of x: 1

Enter the number of terms n: 4

sinh(1.0) using 4 terms is 1.1752011936438014

## RESULT
The program successfully evaluates sinh(x) using recursion, summing up the Taylor series terms:

