# Iterative-Idempotent-Solver

######This program finds solutions to equtions using the process described below.


Let some f(x) = x. Then take x on the right side (which is equal to f(x)) and replace the x inside of the f(x) with its value.
This results in x = f(x) = f(f(x)).

Then, repeat that process to get x = f(f(f(x))).

Doing this infinitely many times gives x = f(f(... ((x))... ))

Plugging in some value for x (like 2 or any other number) does one of two things; either the value of x diverges and becomes infinitely large, or it approaches some value which is a solution to x = f(x).

If it diverges, take the inverse of f(x) (let g(x) = f-1(x)) and run it through the same process, using the same value.

The solution to x = g(x) will also be the solution to x = f(x).


Take e^x, for example. e^x diverges when applying it to itself repeatedly. ln(x), however, approaches a numerical value when iterated. 

With 100 iterations, solving for x = ln(x), the result is (0.4026967693059262+1.2313359538054744j). Running it for 10000 iterations gives (0.3181315052047642+1.3372357014306895j) as an answer.

This value is an approximate solution for both ln(x) = x and e^x = x.


Another example which would be impossible to solve algebraically would be x = 1 + 1/(x^(2 + x)), which has an approximate solution of x ≈ 1.3579336975676037.
