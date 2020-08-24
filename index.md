---
layout: default
title: Introduction
nav_order: 1
has_children: false
---
# Introduction
<p align="center">
  <img width="368" height="414.5" src="http://connerylang.org/img/ConneryLogo.jpg">
</p>
<p align="center">Connery is a experimental lisp-like interpreted programming language that is somewhat themed after veteran actor Sean Connery.</p>

<p align="center"><a href="https://github.com/willcipriano/Connery">Connery on github</a></p>

![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/willcipriano/connery?style=for-the-badge)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/willcipriano/Connery?style=for-the-badge)
![Travis (.org)](https://img.shields.io/travis/willcipriano/Connery?style=for-the-badge)

## Connery has several of the features you have come to expect from a programming language
You can assign variables
```
(def {james_bonds_car} "Aston Martin DB5")
(print james_bonds_car)
```
```
Aston Martin DB5
```
You can create functions and conditional statements
```
(fun {toggle_caterpillar_drive caterpillar_drive_status} {
      if (caterpillar_drive_status)
         {False}
         {True}
})
```
You can complete mathematical operations using Polish notation
```
(- 90 1)
```
```
89
```
Connery supports dynamic typing...
```
(def {this_is_a_string} "Bond. James Bond.")
(def {this_is_a_number} 007)
```
type validation...
```
(print (type_string this_is_a_string))
```
```
String
```
string manipulation...
```
(def {connery_quote} "There is nothing like a challenge to bring out the best in man.")
(split connery_quote (find connery_quote " to"))
```
```
{"There is nothing like a challenge" " to bring out the best in man."}
```
and so much more!
```
(def {highlanders} (list "Connor MacLeod" "Ramírez" "Rachel Ellenstein" "Methos"))
(def {highlanders} (join highlanders (list "General Katana")))
(fun {there_can_only_be_one highlander} {!= -1 (caseless_find highlander "MACLEOD")})
(fun {pick_highlander_to_mentor list} {eval (filter there_can_only_be_one list)})
(pick_highlander_to_mentor highlanders)
```
```
"Connor MacLeod"
```
## How is this Sean Connery themed?
When you make a mistake, Connery lets you know with a signature scottish lisp!
```
shtirred: filter requiresh a function and a lisht ash input!
```