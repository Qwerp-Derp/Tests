# Task 2 (6 marks):

## Synopsis:

Swift, like many other programming languages, is *object-oriented*, which means you need to create things called *objects* to write a working Swift program. In this task, you are to create a class which simulates fractions.

You are to:

- Create a class called `Fraction`.
- Implement operator overloading on that `Fraction` class, for addition (`+`) and subtraction (`-`).
- Extend the fraction class using `extension`, and implement multiplication (`*`) and division (`/`).

**NOTE**: For all operators, you have to fully simplify the fraction.

- Print a string representation of the fraction `numerator/denominator` when `print()` is called on a fraction.

Here are some examples, and what they should respectively output:

```swift
let a = Fraction(num: 2, den: 5) // num = numerator, den = denominator
let b = Fraction(num: 3, den: 4)

/*
    In all examples below, the resulting fraction is fully simplified.
*/
a + b // Fraction(num: 23, den: 20)
a - b // Fraction(num: -7, den: 20)
a * b // Fraction(num: 3, den: 10)
a / b // Fraction(num: 8, den: 15)

print(a) // 2/5
print(a + b) // 23/20
```

## Submission Method:
You are to create a `.playground` file with your name as the file name, which contains all the code relevant to the task.

## Marking Criteria:
- 1 mark for creating a `Fraction` class.
- 1 mark for implementing addition/subtraction algorithms with simplification.
- 1 mark for operator overloading.
- 1 mark for properly using `extension`.
- 1 mark for implementing multiplication/division algorithms with simplification.
- 1 mark for implementing stringification of fraction class, with functions such as `print()`.