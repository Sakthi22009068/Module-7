# # 🔁 Recursion:Sum of Digits using Recursion in Python

## 🎯 AIM:
To write a Python program to calculate the **sum of all digits** in a number using **recursion**.

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `sum_digit(n)` that:
   - Returns 0 if `n <= 0` (Base Case)
   - Else, returns `n % 10 + sum_digit(n // 10)` (Recursive Case)
3. Take integer input from the user.
4. Call the recursive function and store the result.
5. Print the result.
6. **Stop**

## 💻 PROGRAM:

def sum_digit(n):

    if n <= 0:    # Base case
        return 0
    else:
    
        return (n % 10) + sum_digit(n // 10)  # Recursive case


num = int(input("Enter a number: "))


result = sum_digit(num)

print(f"Sum of digits of {num} is {result}")


## OUTPUT
Enter a number: 1234

Sum of digits of 1234 is 10

Enter a number: 56789

Sum of digits of 56789 is 35

## RESULT
The program successfully computes the sum of digits of a number using recursion, breaking down the number digit by digit until all digits are added.
