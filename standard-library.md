# Standard Library

## Syntax
Connery is based on [Lispy](http://www.buildyourownlisp.com/) and like Lispy has two primary statement types, S-Expressions and Q-Expressions.

### S-Expressions
An S-Expression or _Symbolic Expression_ is evaluated as soon as it is encountered. You can think of it just like a expression that you would encounter in any other programming language. S-Expressions are wrapped in parentheses.
```
(print "This string will be printed.")
```
```
This string will be printed.
```
```
(+ 1 1)
```
```
2
```

### Q-Expressions
A Q-Expression or _Quoted Expression_ is just like an S-Expression except it is not evaluated immediately, instead Q-Expressions can be saved for later evaluation, this is useful for defining functions. Q-Expressions are wrapped in curly brackets.

```
; A function can be defined with a Q-Expression
(fun {FUNCTION_NAME FUNCTION_ARG} {print FUNCTION_ARG})
; And then later used
(FUNCTION_NAME "Hello, World!")
```
```
Hello, World!
```

## Essentials

**def** _(or =)_ - Variable assignment, define a variable in the current scope.
```
; Strings
def {VARIABLE_NAME} "example string"
; Numbers
def {VARIABLE_NAME} 32
; Using =
= {VARIABLE_NAME} "another string"
```

**fun** - Allows function definition in the current scope.
```
fun {FUNCTION_NAME} {FUNCTION_BODY}
```

**if** - Conditional statement, if the first expression evaluates to True _(1)_ than the first statement will be evaluated otherwise the second statement is.
```
(if (True) {print "This always happens} {print "This never happens"})
```