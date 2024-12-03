# assignment6.py
# Oluwapelumi Omidiji
# Assignment 6
# 11/04/2024

import math
import random


def problem_1():
    """Return 10 random integers between 25 and 35"""
    return [random.randrange(25, 36) for _ in range(10)]
    

def problem_2():
    """Return an odd integer between 0 and 100."""
    return random.randrange(1, 100, 2)

    
def problem_3():
    """Select a day of the week from a list and return that day."""
    days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
    return random.choice(days)


def pi_approximation():
    """Compute an approximation for pi and print it alongside math.pi."""
    pi_approx = 22 / 7 # Simple approximation
    print(f"Approximation of n: {pi_approx}, math.pi: {math.pi}")
    
    
def conversion(rad):
    """Convert radians to degrees and print both values."""
    degrees = rad * (180 / math.pi)
    print(f"Radians: {rad}, Degree: {degrees}, math.degrees: {math.degrees(rad) }")
    

def factorial_iterative(n):
    """Calculate the factorial of n iteratively."""
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result
    
    
def factorial_recursive(n):
    """Calculate the factorial of a recursively."""
    if n == 0 or n == 1:
        return 1
    else: 
        return n * factorial_recursive(n - 1)


def main():
    print(problem_1())
    print(problem_2())
    print(problem_3())
    pi_approximation()
    conversion(math.pi)
    print(factorial_iterative(5))
    print(factorial_recursive(5))
    

if __name__ == "__main__":
    main()
