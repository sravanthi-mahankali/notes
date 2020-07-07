---
layout: blog 
title:  "Vim Shortcuts"
permalink: /:title
categories: SimpleConcepts
---
## Basic Movements

| **Symbol** | **action** | **Symbol** | **action** |
| h   j <br><br> k   l    | Character left, right  <br><br>  line up line down | b w | word / token left, right |
| ge e | end of word / token left, right | { } | begining of previous, next paragraph |
| ( ) | begning of previous, next sentence | 0(Zero) gm | begning of line, middle of line |
| ^ $ | first , last character of the line | gg | first line |
| G | last line | nG, :n | nth line |
| % | match the brace | nH, nL| nth line from start, nth line from bottom of window |
| M | middle of window |

## Insert movements

| **Symbol** | **action** | **Symbol** | **action** |
| O(capital o) | insert in new line above | o | insert in new line below |
| i a | insert before , after cursor | I A | insert at beginning, end of line |
| rc | replace | ~ | swtich case |

| **Symbol** | **action** | **Symbol** | **action** |
| y | copy | p | paste |
| :%s/word/with/gc | replace the with with word and </br> asks for every occurance of with |


