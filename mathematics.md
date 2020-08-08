# Mathematics

## Mathematical Operations
Builtin 
{: .label .label-purple }
Connery is a [functional programming](https://en.wikipedia.org/wiki/Functional_programming) language as such mathematical operations are no different from regular functions and are used in a style similar to [polish notation](https://en.wikipedia.org/wiki/Polish_notation). 
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
Builtin 
{: .label .label-purple }
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
Builtin 
{: .label .label-purple }
pow returns the power of a number for a given exponent.
```
(pow 2 10)
```
```
1024
```

### is_even
StdLib
{: .label .label-green }
is_even returns True _(1)_ if the number is even, and False _(0)_ if the number is odd.
```
(is_even 2)
```
```
1
```

### is_odd
StdLib
{: .label .label-green }
is_odd returns False _(0)_ if the number is even, and True _(1)_ if the number is odd.
```
(is_odd 2)
```
```
0
```
### rand
Builtin 
{: .label .label-purple }
rand returns a random number between the two numbers provided inclusive.
```
(rand 1 10)
(rand 1 10)
(rand 1 10)
(rand 1 10)
```
```
4
3
10
1
```

## Equality checking
Builtin 
{: .label .label-purple }
Equality checking can be completed in the same manner as other mathematical operations, as well as greater than or less than. If the statement is true it returns True _(1)_ otherwise it returns False _(0)_.
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
; Not equal
(!= 1 2)
```