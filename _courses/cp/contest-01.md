---
layout: slide
title: Contest 01
---

# P0

Given two numbers a and b, returns the sum

```python
def p0(a, b):
	### ADD_YOUR_CODE_HERE ###
  
p0(10, 20)
>>> 30
```

### Answer

<div class="fragment">
{% highlight python %}
def p0(a, b):
	return a + b
{% endhighlight %}
</div>

@@@

# P1

Given a rectangle $a \times b$, returns the area

```python
def p1(a, b):
	### ADD_YOUR_CODE_HERE ###
  
p1(10, 20)
>>> 200
```

### Answer

<div class="fragment">
{% highlight python %}
def p1(a, b):
	return a * b
{% endhighlight %}
</div>

@@@

# P2

Given a number n, returns the sum of the numbers 1 to n

```python
def p2(n):
	### ADD_YOUR_CODE_HERE ###
  
p2(5)
>>> 15
```

### Answer

<div class="fragment">
{% highlight python %}
def p2(n):
	return n * (n + 1) / 2
{% endhighlight %}
</div>

@@@

# P3

Given a number n, returns the sum of the even numbers 2 to n

```python
def p3(n):
	### ADD_YOUR_CODE_HERE ###
  
p3(5)
>>> 6
```

### Answer

<div class="fragment">
{% highlight python %}
def p3(n):
	a = n // 2
	return a * (a + 1)
{% endhighlight %}
</div>

@@@

# P4

Given a number n, returns the factorial of n.

```python
def p4(n):
	### ADD_YOUR_CODE_HERE ###
  
p4(5)
>>> 120 
```

### Answer

<div class="fragment half-column">
{% highlight python %}
def p4(n):
	if n < 2:
        return 1
    else:
        return n * p4(n-1)
{% endhighlight %}
</div>

<div class="fragment half-column">
{% highlight python %}
def p4(n):
	result = 1
	for i in range(2, n+1):
        result *= i
	
	return result
{% endhighlight %}
</div>

@@@

# P5

Given a number n, print a square $n \times n$ of 'X'

```python
def p5(n):
	### ADD_YOUR_CODE_HERE ###
	
p5(4)
>>> XXXX
    X  X
    X  X
    XXXX
```

@@

<h3> Answer </h3>

{% highlight python %}
def p5(n):
	for i in range(n):
		line = 'X'
		if i == 0 or i == n-1:
			for j in range(n-1):
				line += 'X'
		else:
			for j in range(n-2):
				line += ' '
			line += 'X'
		print(line)
{% endhighlight %}

@@@

# P6

Given a number n, print a chess board of size $n \times n$.

```python
def p6(n):
	### ADD_YOUR_CODE_HERE ###
	
p6(6)
>>> XOXOXO
    OXOXOX
    XOXOXO
	OXOXOX
    XOXOXO
	OXOXOX
```

@@

<h3> Answer </h3>

```python
def p6(n):
	for i in range(n):
		line = ''
		for j in range(n):
			line += 'X' if (i+j) % 2 == 0 else 'O'
		print(line)
```

@@@

# P7

Given a list of numbers, returns the greatest number

```python
def p7(l):
	### ADD_YOUR_CODE_HERE ###
	
p7([6, 4, 7, 3, 5, 8, 2, 9, 1])
>>> 9
```

@@

### Answer

```python
def p7(l):
	return max(l)
```

@@@

# P8

Given a list of numbers, returns the second greatest number

```python
def p8(l):
	### ADD_YOUR_CODE_HERE ###
	
p8([6, 4, 7, 3, 5, 8, 2, 9, 1])
>>> 8
```

@@

### Answer

```python
def p8(l):
	greatest  = -float('inf')
	greatest2 = -float('inf')
	for x in l:
		if x > greatest:
			greatest2 = greatest
			greatest = x
		elif x > greatest2:
			greatest2 = x
	return greatest2
```

@@@

# P9

Given a list of numbers, returns the sum of the numbers on odd positions

```python
def p9(l):
	### ADD_YOUR_CODE_HERE ###
	
p9([0, 1, 2, 1, 3, 1, 4])
>>> 3
```

@@

### Answer

```python
def p9(l):
	result = 0
	for i in range(1, len(l), 2):
		result += l[i]
	return result
```

@@@

# P10

Given a list of numbers, returns the last element

```python
def p10(l):
	### ADD_YOUR_CODE_HERE ###
	
p10([0, 1, 2, 3, 4])
>>> 4
```

@@

### Answer

```python
def p10(l):
	return l[-1]
```


@@@

# P11

Given a list of numbers, returns the reversed list

```python
def p11(l):
	### ADD_YOUR_CODE_HERE ###
	
p11[0, 1, 2, 3, 4])
>>> [4, 3, 2, 1, 0]
```

@@

### Answer

```python
def p11(l):
	return l[::-1]
```

@@@

# P12

Given a list of numbers, returns the elements on even positions in a list

```python
def p12(l):
	### ADD_YOUR_CODE_HERE ###
	
p12([0, 1, 2, 3, 4])
>>> [0, 2, 4]
```

@@

### Answer

```python
def p12(l):
	return l[::2]
```
@@@

# P13

Given a number n, returns the squares from 1 to n

```python
def p13(n):
	### ADD_YOUR_CODE_HERE ###
	
p13(5)
>>> [1, 4, 9, 16, 25]
```

@@

### Answer

```python
def p13(l):
	return [i*i for i in range(1, n)]
```

@@@

# P14

Given two list of numbers, returns the element-wise multiplication

```python
def p14(l1, l2):
	### ADD_YOUR_CODE_HERE ###
	
p14([0, 1, 2, 3, 4], [5, 6, 7, 8, 9]])
>>> [0, 6, 14, 24, 36]
```

@@

### Answer

```python
def p14(l1, l2):
	n = len(l1)
	return [l1[i] * l2[i] for i in range(n)]
```

@@@

# P15

Given a list of numbers and a number n, returns the number of occurrences of n in the list

```python
def p15(l, n):
	### ADD_YOUR_CODE_HERE ###
	
p15([0, 1, 2, 3, 4, 0], 0)
>>> 2
```

@@

### Answer

```python
def p15(l, n):
	return l.count(n)
```

@@@

# P16

Given a list of numbers, returns the same list without repetitions 

```python
def p16(l):
	### ADD_YOUR_CODE_HERE ###
	
p16([0, 1, 1, 2, 2, 2])
>>> [0, 1, 2]
```

@@

### Answer

```python
def p16(l):
	return list(set(l))
```

@@@

# P17

Given two sets, returns the intersection

```python
def p17(s1, s2):
	### ADD_YOUR_CODE_HERE ###
	
p17({'A', 'B', 'C'}, {'B', 'C', 'D'})
>>> {'B', 'C'}
```

@@

### Answer

```python
def p17(s1, s2):
	return s1 & s2
```

@@@

# P18

Given a list of numbers, returns True if there are duplicate elements

```python
def p18(l):
	### ADD_YOUR_CODE_HERE ###
	
p18([0,1,2,3,1])
>>> True
```

@@

### Answer

```python
def p18(l):
	return len(l) == len(set(l))
```

@@@

# P19

Given a dictionary of costs and a list of amount of items, returns the grand total.

```python
def p19(cost_per_unit, amounts):
	### ADD_YOUR_CODE_HERE ###
	
p19({'Blueberries': 2, 'Banana': 1, 'Orange': 3, 'Cherries': 2, 'Pineapple': 4},
    {'Banana': 10, 'Pineapple': 5})
>>> 30
```

@@

### Answer

```python
def p19(cost_per_unit, amounts):
	total = 0
	for item, amount in amounts.items():
		total += cost_per_unit[item] * amount
	return total
```

@@@

# P20

Given a string and a key k, returns the encrypted message using the Caesar Cipher.

```python
import string 
letters = ' ' + string.uppercase
# ' ABCDEFGHIJKLMNOPQRSTUVWXYZ'

def p20(message, k):
	### ADD_YOUR_CODE_HERE ###
	
p20('ABCD', 3)
>>> 'DEFG'
```

@@

### Answer

```python
def p20(message, k):
	s = ''
	for letter in message:
		i = (letters.index(letter) + k) % len(letters)
		s += letters[i]
	return s
```

@@@

# P21

Given a number n, returns the reversed number

```python
def p21(n):
	### ADD_YOUR_CODE_HERE ###
	
p21(1234567890)
>>> 987654321
```

@@

### Answer

```python
def p21(n):
	number = 0
	while n>0:
		number = number * 10 + (n % 10)
		n = n // 10
	return number
```

@@@

# P22

Given a string, converts all lowercase letters to uppercase letters and vice versa. Hint: s.lower(), s.upper(), s.isupper()

```python
def p22(s):
	### ADD_YOUR_CODE_HERE ###
	
p22('HeLlOw')
>>> 'hElLoW'
```

@@

<h3> Answer </h3>

```python
def p22(s):
	s2 = ''
	for l in s:
		s2 += l.lower() if l.isupper() else l.upper()
	return s2
```

@@@

# P23

Given a string, returns True if it is a palindrome

```python
import re

def p23(s):
	s = re.sub("[^A-Z]", "", s.upper())
	### ADD_YOUR_CODE_HERE ###
	
p23('Eva, can I see bees in a cave?')
>>> True
```

@@

<h3> Answer </h3>

```python
def p23(s):
	s = re.sub("[^A-Z]", "", s.upper())
	n = len(s) // 2
	for i in range(n):
		if s[i] != s[-i-1]:
			return False
	return True
```

@@@

# P24

Given a number n, print a triangle of 'X' in n lines

```python
def p24(n):
	### ADD_YOUR_CODE_HERE ###
	
p24(4)
>>>    X
      X X
     X   X
    XXXXXXX
```

@@

<h3> Answer </h3>

```python
def p24(n):
	for i in range(n-1):
		line = ''
		for j in range(n-i-1):
			line += ' '
		line += 'X'
		for j in range(i+i-1):
			line += ' '
		if i != 0:
			line += 'X'
		print(line)
	line = 'X'
	for i in range(n+n-2):
		line += 'X'
	print(line)
```

@@@

# P25

Given a number n, solve the Hanoi towers puzzle

```python
def p25(n, origin, auxiliary, target):
	### ADD_YOUR_CODE_HERE ###
	
p25(3, '1', '2', '3')
>>> 1=>3
    1=>2
    3=>2
    1=>3
    2=>1
    2=>3
    1=>3
```

@@

<h3> Answer </h3>

```python
def p25(n, origin, auxiliary, target):
    if n == 1:
        print(origin + '=>' + target)
    else:
        p25(n-1, origin, target, auxiliary)
        print(origin + '=>' + target)
        p25(n-1, auxiliary, origin, target)
```
