---
layout: default
title: Constants
parent: Language Reference 
nav_order: 8
---
# Constants

Connery contains a number of constant values for the sake of convenience and to improve readability.

| Constant Variable Name     | Actual Value          | Purpose                                  |
|:---------------------------|:----------------------|:-----------------------------------------|
| True                       | 1                     | Conditional statements                   |
| False                      | 0                     | Conditional statements                   |
| None                       | Empty Q-Expression    | Comparison / returning nothing           |
| Empty                      | Empty String          | Comparison / returning nothing           |
| Otherwise                  | True                  | Case statements                          |
| std_lib_main_location      | "stdlib/main.connery" | Reloading the standard library           |

# Enums

## type_num

| Value   | Assigned to           |
|:--------|:----------------------|
| 0       | "Number"              |
| 1       | "String"              |
| 2       | "S Expression"        |
| 3       | "Q Expression"        |
| 4       | "Function"            |
| 5       | "Symbol"              |

## weekday_num

| Value   | Assigned to           |
|:--------|:----------------------|
| 0       | "Monday"              |
| 1       | "Tuesday"             |
| 2       | "Wednesday"           |
| 3       | "Thursday"            |
| 4       | "Friday"              |
| 5       | "Saturday"            |
| 6       | "Sunday"              |

## month_num

| Value   | Assigned to           |
|:--------|:----------------------|
| 0       | "January"             |
| 1       | "February"            |
| 2       | "March"               |
| 3       | "April"               |
| 4       | "May"                 |
| 5       | "June"                |
| 6       | "July"                |
| 7       | "August"              |
| 8       | "September"           |
| 9       | "October"             |
| 10      | "November"            |
| 11      | "December"            |