---
layout: default
title: Strings
parent: Language Reference 
nav_order: 5
---
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
"this is upper case"
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

### rand_string 
StdLib
{: .label .label-green }
rand_string returns a random string for a given length
```
(rand_string 10)
(rand_string 10)
(rand_string 15)
```
```
"7IPdDBk&vT"
"6V6^Nk#+yC"
"^-B*AYghRNzQ+g9"
```

### delimit
StdLib
{: .label .label-green }
delimit takes a string, splits it at a particular character and returns a list. 
```
delimit "," "a,b,c,d,e,f,g"
```
```
{"a" "b" "c" "d" "e" "f" "g"}
```

### relimit
StdLib
{: .label .label-green }
relimit takes a list of strings and places a delimiter between them, returning a single string.
```
relimit "," (list "a" "b" "c")
```
```
"a,b,c"
```

### string_to_index_list
StdLib
{: .label .label-green }
string_to_index_list takes a string as input and returns a list of numbers that correspond to each character.
```
string_to_index_list "Bond, James Bond"
```
```
{27 14 13 3 77 76 35 0 12 4 18 76 27 14 13 3}
```

### index_list_to_string
StdLib
{: .label .label-green }
index_list_to_string does the opposite of string_to_index_list and converts a list of numbers back into a string.
```
index_list_to_string (list 27 14 13 3 77 76 35 0 12 4 18 76 27 14 13 3)
```
```
"Bond, James Bond"
```

### string_rep
StdLib
{: .label .label-green }
string_rep takes a string as input and returns a list with two numbers that can be used later to see if it matches another string. Useful when you want to minimize memory use or do many comparisons of long strings rapidly. _Note: This method is prone to false positives._
```
string_rep "Sean Connery"
```
```
{12 250}
```

### string_rep_compare
StdLib
{: .label .label-green }
string_rep_compare takes two string reps and compares them. Returns True _(1)_ if they might match and False _(0)_ if they don't match.
```
string_rep_compare (string_rep "Bond, James Bond.") (string_rep "Bond, James Bond.")
```
```
1
```
### string_rep_compare_string
StdLib
{: .label .label-green }
string_hash_compare compares a string rep to a given string to see if they match. Returns True _(1)_ if they might match and False _(0)_ if they don't match.
```
(string_rep_compare_string (string_rep "Sean Connery") "Sean Connery")
(string_rep_compare_string (string_rep "Sean Connery") "Pierce Brosnan")
```
```
1
0
```