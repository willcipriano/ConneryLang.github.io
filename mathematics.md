# Mathematics

## Mathematical Operations

Connery is a functional programming language as such mathematical operations are no different from regular functions and are used in a style similar to [polish notation](https://en.wikipedia.org/wiki/Polish_notation). 
```
; Addition
(+ 1 1)
; Subtraction
(- 1 1)
; Multiplication
(* 1 1)
; Division
(/ 1 1)
```

### mod
mod returns the result of integer division between two numbers. Useful for [job interview tests](https://en.wikipedia.org/wiki/Fizz_buzz).
```
(fun {fizzbuzz number} {
     case
     {(== 0 (mod number 15)) "FizzBuzz"}
     {(== 0 (mod number 5)) "Buzz"}
     {(== 0 (mod number 3)) "Fizz"}
     {Otherwise number}
})
```

### pow
pow returns the power of a number for a given exponent.
```
(pow 2 10)
```
```
1024
```

## Equality checking

Equality checking can be completed in the same manner as other mathematical operations, as well as greater than or less than. If the statement is true it returns True otherwise it returns False.
```
; Equal to
(= 1 1)
; Greater than
(> 2 1)
; Equal to or greater than
(>= 1 2)
; Less than
(< 2 1)
; Equal to or less than
(<= 1 2)
```