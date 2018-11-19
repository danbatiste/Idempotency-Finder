# Iterative-Idempotent-Solver

Back in 2016 I was messing around with my calculator and I realized that if you take the cosine of some number, and you take the cosine of the result, and you keep taking the cosine over and over again, you end up with this number where the cosine of that number equaled that same number. And I started to wonder why that was exactly.

Eventually, I figured out that what I was doing was essentially solving a function in the form of f(x) = x. I just took the x on the right side (which is equal to f(x)) and replaced the x inside of the f(x) with its value (substitution axiom), ending up with x = f(x) = f(f(x)). Then I repeated that process to get x = f(f(f(x))).

I found that doing this infinitely many times to get x = f(f(... ((x))... )) while plugging in some value for x (like 2 or any other number) would to one of two things. It would either diverge and become infinitely large, or it would approach some value. 

If it approached a value, then I could plug that value into the equation f(x) = x, and it would be a solution. 

If it diverged, then I could take the inverse of f(x) and do the same process to it. Then I could take the solution from that process and apply it to the original, not-inverse function, and it would be a solution to that too. After all, f(x) = x and f_inverse(x) = x have the same solution.

ln(x) and e^x are a great example of this. e^x diverges, so applying it to itself over and over again will make its value shoot off to infinity. ln(x), however, approaches a numerical value. When I run the program for 100 iterations, solving for x = ln(x), I get: Answer = (0.4026967693059262+1.2313359538054744j). Running it for 10000 iterations gives me (0.3181315052047642+1.3372357014306895j) as an answer.

That value solves for both ln(x) = x and e^x = x.

This math can solve for things like x = 1 + 1/(x^(2 + x)) (which has a solution of x = 1.3579336975676037).
