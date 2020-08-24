# Basic Functions

### def _(or =)_
Builtin 
{: .label .label-purple }
Variable assignment, define a variable in the current scope.
```
; Strings
def {VARIABLE_NAME} "example string"
; Numbers
def {VARIABLE_NAME} 32
; Using =
= {VARIABLE_NAME} "another string"
```

### fun
StdLib
{: .label .label-green }
Allows function definition in the current scope.
```
fun {FUNCTION_NAME} {FUNCTION_BODY}
```
### if
Builtin 
{: .label .label-purple }
Conditional statement, if the first expression evaluates to True _(1)_ than the first statement will be evaluated otherwise the second statement is.
```
(if (True) 
    {print "This always happens"} 
    {print "This never happens"})
```
```
This always happens
```

### tail
Builtin 
{: .label .label-purple }
Remove first item/digit/character from a list/number/string and return the result. _(Note: When used on numbers if the result would begin with zero, the leading zeros will be omitted.)_
```
(tail "Walther PPK")
(tail 1234)
(tail (list "Aston" "Martin"))
(tail 1010)
```
```
"alther PPK"
234
{"Martin"}
10
```

### head
Builtin 
{: .label .label-purple }
Similar to tail, operates on a list/number/string and instead returns the first item/digit/character
```
(head "Walther PPK")
(head 1234)
(head (list "Aston" "Martin"))
```
```
"W"
1
{"Aston"}
```

### join
Builtin 
{: .label .label-purple }
join combines two or more lists or strings into a single list or string.
```
(join (list "item1" "item2") (list "item3" "item4"))
(join "Hello" "," " " "World" "!")
```
```
{"item1" "item2" "item3" "item4"}
"Hello, World!"
```

### list
Builtin 
{: .label .label-purple }
list creates a list from all the consequent items provided to it.
```
(list "item 1" "item 2" 3)
```
```
{"item 1" "item 2" 3}
```

### type
Builtin 
{: .label .label-purple }
type returns a number that corresponds with the type of the item passed to it. See [type_num](http://connerylang.org/constants.html#type_num) for translations or use _type_string_ to get a string instead.
```
(type "example")
(type_string "example")
```
```
1
"String"
```

### \ _(lambda)_
Builtin 
{: .label .label-purple }
Lambda allows the creation of [anonymous functions](https://en.wikipedia.org/wiki/Anonymous_function), useful when paired with functions like filter.
```
(\ {STRING} {print STRING})
```

### length
Builtin 
{: .label .label-purple }
length returns the number of characters in a string, the number of digits in a number, or the number of elements in a list depending on what is passed into it.
```
(length "Bond")
(length 1234)
(length (list 1 2 3 4))
```
```
4
4
4
```