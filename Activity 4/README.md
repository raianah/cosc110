## Activity #3 - Introduction to SymPy

### Questions:
1. What do you think 'x + x' means?
    - 2x. It represents addition of two variables with hidden coefficients, or in this case, addition of two x's with 1 in their value.
2. What does `x * x` represent?
    - x**2. It represents multiplying two variables which adds the hidden exponent of the variable. In this case, the value of two x's are 1.
3. What result do you get? What do you think it means?
    - 1. The limit indicates that as $$x$$ approaches zero, $$\sin(x)$$ closely approximates $$x$$, highlighting the fundamental relationship between the sine function and small angles as the sine function is continuous and smooth at $$x = 0$$.
4. What is the output? Can you describe what it tells you?
    - 2x. The derivative indicates the rate of change of the function at any point. It tells you how steep the curve is at that point.
5. What do you see? How many terms are shown in the result?
    - $$\displaystyle 1 + x + \frac{x^{2}}{2} + \frac{x^{3}}{6} + O\left(x^{4}\right)$$. There are 4 terms shown in the equation.
6. What are the answers?
    - [-2, 2]
7. What kind of problem do you think this is?
    - The equation $$x^2 - 4 = 04$ is a quadratic equation. The answer $$[-2, 2]$$ indicates the values of $$x$$ where the equation holds true.
8. What was your favorite part of this activity?
    - Solving equations. Having this type of programmatical feature in a programming language makes complex math applications simpler. Combined with data visualization libraries like pandas and introduction of pytorch, machine learnings that can answer complex equations will be much easier to produce.
9. What was something new or surprising you learned?
    - The usage of big O notation in the series expansion. I never thought that the big O was used in this scenario and only used to gather time and space complexity.