## Activity #3 - Introduction to SymPy

### Tasks:

1. Include all necessary sympy modules.
   - `from sympy import *`

2. Solve for the following
   - $$\frac{5}{3} + \frac{\sqrt{10}}{2}$$
     - ```py
            ra = sympy.Rational(5, 3)
            sqr = sympy.sqrt(10) / 2

            expr = sympy.solve(f"{ra} + {sqr}")
            print(expr)

            "Answer: sqrt(10)/2 + 5/3"
        ```
   - $$\sqrt{50} \times \sqrt{\frac{5}{9}}$$
     - ```py
            sqr1 = sympy.sqrt(50)
            sqr2 = sympy.Rational(5, 9)
            sqra = sympy.sqrt(sqr2)

            expr = sqr1 * sqra
            print(expr)

            "Answer: 5*sqrt(10)/3"
        ```
3. Create the equation for the following using `Symbols`:
    - $$2x+3y=12$$
        - ```py
            x, y = sympy.symbols('x y')

            eq = sympy.Eq(2*x + 3*y, 12)
            print(eq)

            "Answer: Eq(2*x + 3*y, 12)"
          ```
    - $$x−y=4$$
        - ```py
            x, y = sympy.symbols('x y')

            eq = sympy.Eq(x - y, 4)
            print(eq)

            "Answer: Eq(x - y, 4)"
          ```
4. Simplify the following equations using the `simplify` method.
    - $$\frac{x^2 + 2x + 1}{x + 1}$$
        - ```py
            x = sympy.symbols('x')
            expr = (x**2 + 2*x + 1) / (x + 1)

            sim = sympy.simplify(expr)
            print(sim)

            "Answer: x + 1"
            ```
    - $$\frac{1 - \frac{1}{1 + \frac{1}{x}}}{1 + \frac{1}{x}}$$
        - ```py
            x = sympy.symbols('x')
            expr = (1 - 1/(1 + 1/x)) / (1 + 1/x)

            sim = sympy.simplify(expr)
            print(sim)

            "Answer: x/(x + 1)**2"
            ```
5. Expand the following expressions using the `expand` method.
    - $$(2x + 2)^2$$
        - ```py
            x, y = sympy.symbols('x y')
            expr = (2*x + 2)**2

            expn = sympy.expand(expr)
            print(expn)

            "Answer: 4*x**2 + 8*x + 4"
            ```
    - $$(2x + y)(x - 2y)$$
        - ```py
            x, y = sympy.symbols('x y')
            expr = (2*x + y)*(x - 2*y)

            expn = sympy.expand(expr)
            print(expn)

            "Answer: 2*x**2 - 3*x*y - 2*y**2"
            ```