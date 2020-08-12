# Strings

### upper
StdLib
{: .label .label-green }
upper converts any lower case characters to upper case.
```
upper "this is lower case"
```
```
"THIS IS LOWER CASE"
```

### lower
StdLib
{: .label .label-green }
lower converts any upper case characters to lower case.
```
lower "THIS IS UPPER CASE"
```
```
"this is lower case"
```

### replace
Builtin 
{: .label .label-purple }
replace replaces all instances of a given string that occur within a string with another string.
```
replace "Sean Connery is the worst Bond." "worst" "best"
```
```
"Sean Connery is the best Bond."
```

### find
Builtin 
{: .label .label-purple }
find returns an index for a particular string if it exists within a given string and False _(0)_ if it does not.
```
(find "Operation Market Garden" "Market")
(find "I've got lunatics laughing at me from the woods." "Jeeps")
```
```
10
0
```

### caseless_find
StdLib
{: .label .label-green }
caseless_find works just like find, but it ignores case.
```
caseless_find "ABCD" "bcd"
```
```
1
```

### split
Builtin 
{: .label .label-purple }
split takes a string and splits it at a particular index returning two strings in a list.
```
split "Late 14th century, Ming Dynasty. How it breaks the heart." 14
```
```
{"Late 14th century, Ming Dynasty. How it " "breaks the heart."}
```

### chop 
Builtin 
{: .label .label-purple }
chop is similar to split, but it only returns the first part of the string and discards the rest.
```
chop "Got lost in his own museum huh?" 8
```
```
"Got lost"
```
