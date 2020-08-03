# Introduction

<p align="center">
  <img width="368" height="414.5" src="/img/ConneryLogo.jpg">
</p>

<p align="center">Connery is a experimental lisp-like interpreted programming language that is somewhat themed after veteran actor Sean Connery.</p>

## Connery has several of the features you have come to expect from a programming language

You can assign variables
```
(def {james_bonds_car} "Aston Martin DB5")
```
You can create functions and conditional statements
```
(fun {toggle_caterpillar_drive caterpillar_drive_status} {
      if (== True caterpillar_drive_status)
         {False}
         {True}
})
```
You can complete mathematical operations using Polish notation
```
(- 90 1)
```
Connery supports dynamic typing...
```
(def {this_is_a_string} "Bond. James Bond.")
(def {this_is_a_number} 007)
```
and type validation
```
(print (type_string this_is_a_string))
```
