# Automatic Promotion (Implicit Type Casting)

## Between Numerical Data Types

- When an arithmetic operation is performed between a shorter and a larger data
type, the result is always stored as the larger one

- Precedence goes: `byte` -> `short` -> `int` -> `long` -> `float` -> `double`

- This is known as *implicit type casting*

- Moreover, Java does not do arithmetic operations on data types smaller than
`int`

- Instead it promotes them to `int` before performing any calculation

## With String and Characters

- Adding two strings or a `String` and a `char` concatenates them

- When a `String` and a number are added, the number is converted into a
`String`

- When two `char`s are added together, they're converted to an `int` beforehand

- Similarly, when a `char` is added with an `int` it is converted to an `int`
beforehand
