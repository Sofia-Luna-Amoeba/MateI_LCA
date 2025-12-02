Sofia.qmd
---
title: "Tarea5SofiaLuna"
format: html
---

## holamundo

## Ejercicio 1

Calcular
$$\frac{8!}{5!3!}$$

```{python}
import math

result = math.comb(8, 3)
result
```

## Ejercicio 2

Calculate each of the following. Your answer must be a number. No arithmetic operations are allowed in your answer. Please give 7 places after your decimal point if you use scientific notation.


a) $\frac{720!}{40!680!}$


```{python}
import math

result_a = math.comb(720, 680)
result_a
```

b) $\frac{220!}{190!50!}$


```{python}
import math

result_a = math.comb(220, 190)
result_b

```


c) $\frac{609! - 605!}{604!}$


```{python}
import math

result_c = (math.factorial(609) - math.factorial(605)) / math.factorial(604)
result_c
```
 
## Ejercicio 3

a) $\frac{7!}{5!}$
```{python}
import math

result_a = math.factorial(7)  / math.factorial(5)
result_a
```

## Ejercicio 4

Standard automobile license plates in a country display 2 numbers, followed by 2 letters, followed by 3 numbers. How many different standard plates are possible in this system? (Assume repetition of letters and numbers is allowed.)

```{python}
import numpy as np

numbers = 10  # 0-9
letters = 26  # A-Z

# Calculate the total combinations
total_plates = (numbers ** 2) * (letters ** 2) * (numbers ** 3)
total_plates
```


## Ejercicio 5

A true-false test contains 11 questions. In how many different ways can the 11-question test be answered?


```{python}
questions = 11
options_per_question = 2  # True or False

total_ways = options_per_question ** questions
total_ways
```


## Ejercicio 6

This problem is taken from the delightful book "Problems for Mathematicians, Young and Old" by Paul R. Halmos.
Suppose that 947 tennis players want to play an elimination tournament. That means: they pair up, at random, for each round; if the number of players before the round begins is odd, one of them, chosen at random, sits out that round. The winners of each round, and the odd one who sat it out (if there was an odd one), play in the next round, till, finally, there is only one winner, the champion. What is the total number of matches to be played altogether, in all the rounds of the tournament?


```{python}
#| code-fold: true

players = 947
matches = 0
rounds = 0

while players > 1:
    matches += players // 2
    players = (players + 1) // 2

    rounds += 1
    print(f"After round {rounds}, remaining players: {players}")
print(f"Total matches played: {matches}")
```

## Ejercicio 10

James owns 6 different mathematics books and 6 different computer science books and wish to fill 5 positions on a shelf. If the first 2 positions are to be occupied by math books and the last 3 by computer science books, in how many ways can this be done?

```{python}
import math

math_books = 6
cs_books = 6

# Calculate the arrangements
math_arrangements = math.perm(math_books, 2)
cs_arrangements = math.perm(cs_books, 3)

total_arrangements = math_arrangements * cs_arrangements
total_arrangements
```

## Ejercicio 11
A company has 2785 employees. Each employee is to be given an ID number that consists of one letter followed by 3 digits.
How many different ID numbers are possible?


```{python}
import numpy as np

numbers = 10  # 0-9
letters = 26  # A-Z

# Calculate the total combinations
total_plates = letters  * (numbers ** 3) 
print(total_plates)
```

## Ejercicio 12
A fair 6
-sided die is rolled 10
 times and the resulting sequence of 10
 numbers is recorded.

How many different sequences are possible?
```{python}
6**10
```

How many different sequences consist entirely of even numbers?
```{python}
3**10
```

How many different sequences are possible if the first, third, and fourth numbers must be the same?
```{python}
6**8
```

## Ejercicio 13

How many ways can a team of 21 hockey players choose a captain and two alternate captains?


```{python}
import math
captain_choices = 21

alternate_choices = math.comb(29, 2)

total_choices = captain_choices * alternate_choices
total_choices
```

## Ejercicio 14

Find how many positive integers with exactly four decimal digits, that is, positive integers between 1000 and 9999 inclusive, have the following properties:
(a) are divisible by 7.
(b) are divisible by 5 but not by 7.
(c) are even.
(d) are not divisible by either 5 or 7.
```{python}
a =0
b =0
c =0
d = 0
for n in range(1000, 10000):
    if n % 7 == 0:
        a += 1
    if n % 5 == 0 and n % 7 != 0:
        b += 1
    if n % 2 == 0:
        c += 1
    if n % 5 != 0 and n % 7 != 0:
        d += 1

a
b
c
d
```

## Ejercicio 15

How many different 9-letter permutations can be formed from 7
 identical H's and two identical T's?

b) $\frac{9!}{7!2!}$


```{python}
import math

result_a = math.comb(9, 7)
result_b

```

## Ejercicio 16

A boy has 2 red , 4 yellow and 3 green marbles. In how many ways can the boy arrange the marbles in a line if:

a) Marbles of the same color are indistinguishable?

```{python}
from math import factorial

total_marbles = 2 + 4 + 4
ways = factorial(total_marbles) / (factorial(2) * factorial(4) * factorial(4))
ways

```


b) All marbles are distinguishable?

```{python}
ways_distinguishable = factorial(total_marbles)

ways_distinguishable
```

## Ejercicio 17
 How many different ways can a race with 8 runners be completed?

```{python}
import math
math.factorial(8)
```

## Ejercicio 18
 In how many ways can 5 different novels, 2 different mathematics books, and 1 biology book be arranged on a bookshelf if

(a) the books can be arranged in any order?
```{python}
import math
math.factorial(8)
```

(b) the mathematics books must be together and the novels must be together?
```{python}
import math
from math import factorial

waysdos= factorial(3) * (factorial(5)) * (factorial(2)) 
waysdos

```

the mathematics books must be together but the other books can be arranged in any order?
```{python}
import math
from math import factorial
waystres= factorial(7) * (factorial(2)) 
waystres
```

## Ejercicio 21
Five people applied for jobs at a store. Only two of these people will be hired.

The number of different pairs of people who could be hire is
 ```{python}
import math
numir=math.comb(5,3)
numir
```

## Ejercicio 22

How many ways can 4 CD's be chosen from a case of 10 CDs? 

```{python}
import math

total_ways = math.comb(10,4)

total_ways
```

## Ejercicio 24

 The annual National No Spying Day is celebrated at KAOS headquarters this year. There are 12 Control agents and 17 KAOS agents attending. How many ways can we choose a team of 7 agents if 2 team members need to be from Control and 5 from KAOS?

```{python}
import math

total_ways = math.comb(12, 2) * math.comb(17, 5)
total_ways
```

How many ways can we choose a team of 7 agents if at least 1 team member needs to be from Control?
```{python}
import math
total = math.comb(29, 7)
contr= math.comb(17, 7)
contr
```

## Ejercicio 26

A standard deck of cards consists of four suits (clubs, diamonds, hearts, and spades), with each suit containing 13 cards (ace, two through ten, jack, queen, and king) for a total of 52 cards in all.

How many 7-card hands will consist of exactly 2 hearts and 3 clubs?
```{python}
import math

baraja = math.comb(13,2) * math.comb(13,3) * math.comb(26,2)
baraja
```

## Ejercicio 27
In how many ways can a person invite 4 out of their 13 closest friends to a dinner party?

```{python}
import math

total_ways = math.comb(13, 4) 
total_ways
```

## Ejercicio 29
A standard deck of cards consists of four suits (clubs, diamonds, hearts, and spades), with each suit containing 13 cards (ace, two through ten, jack, queen, and king) for a total of 52 cards in all.

How many 5-card hands will consist of exactly 3 kings and 2 queens?

```{python}
import math
a = math.comb(4,3) * math.comb(4,2)
a
```


## Ejercicio 30
A pizza parlor offers a choice of 16 different toppings. How many 5-topping pizzas are possible?
```{python}
import math
a = math.comb(16,5) 
a
```

## Ejercicio 31
A computer is printing out subsets of a 5 element set (possibly including the empty set).

(a) At least how many sets must be printed to be sure of having at least 4 identical subsets on the list?
```{python}
import math
a1 = 2**5
num = 4
a = (num-1) * a1 + 1
a
```

At least how many identical subsets are printed if there are 161 subsets on the list?
```{python}
import math
auno = 2**5
valordos= 161
b = math.ceil(valordos / auno)
b
```

## Ejercicio 32
(a)Among 33 people at least how many were born in the same month?
```{python}
a = (33 // 12) + 1
a
```

(b) Assuming that no one is born on Feb. 29 (leap day), how many people should be selected to guarantee that at least 9 were born on the same day, not considering the year?
```{python}
b = (9-1)*365 + 1
b
```

# Problema 40

There are 356
 students in a college who have taken a course in calculus, 230 who have take a course in discrete mathematics, and 180 who have taken a course in both calculus and discrete mathematics. How many students at this college have taken a course in either calculus or discrete mathematics?


$$\# (A \cup B) = \# A + \# B - \# (A \cap B)  = 356+ 230-180= 406$$

## Ejercicio 49
A secret code for a bank vault consists of 3 letters, then 4 digits and then 4 more letters.

How many different codes are possible?
```{python}
import numpy as np

numbers = 10  # 0-9
letters = 26  # A-Z

# Calculate the total combinations
total_plates =  (letters ** 3) * (numbers** 4)  *(letters ** 4)
total_plates
```

How many codes are possible if repeating letters and digits is not allowed?

 ```{python}
import math
b = math.perm(26, 7) * math.perm(10, 4)
b
```

How many codes are possible if repeats are not allowed and the second letter must be 'P' and the third digit must be '1'?
 ```{python}
import math
c1=math.perm(25,6 )
c2=math.perm(9,3 )
c=c1*c2
c
```

If the wrong code is entered the vault automatically locks and the alarm sounds. Suppose repeating letters and digits are allowed in the code. What is ther probability of a thief breaking into the vault if the thief has no prior knowledge of the secret code?
 ```{python}
from fractions import Fraction
total = 80318101760000
d = Fraction(1, total)
print(d)      
print(float(d))
```

## Ejercicio 50
 A DNA sequence can be represented as a string of the letters ACTG (short for adenine, cytosine, guanine, and thymine).

  (a) How many DNA sequences are exactly 21 letters long? 

```{python}
DNA=4**21
DNA
```

 Given a DNA sequence of length 21, how many single letter mutations are possible?
 ```{python}
DNAmutacion=3*21
DNAmutacion
```

Given a DNA sequence of length 21, how many double letter mutations are possible? 
 ```{python}
import math
c=(math.comb(21,5) * (3**2))
c
```

