---
layout: default
title: Syntax
parent: Language Reference 
nav_order: 2
---
# Syntax
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

### Dictionaries
Dictionaries are a data type backed by a hash map that allows you to store any other value and look it up by key. They can be created like so.
```
#"key"&"value",
 "key 2"&2,
 "key 3"&"another value",
 "key 4"&"yet another value"#
```

### Comments
Comments can be prefixed with a semicolon and end at a newline.
```
; This a comment
```