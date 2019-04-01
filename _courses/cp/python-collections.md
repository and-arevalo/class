---
layout: slide
title: Python Collections
---

##  Lists

A sequence of Python objects. 

```python
list1 = ['item 1', 'item 2', 'item 3', 'item 4']
print(list1) # ['item 1', 'item 2', 'item 3', 'item 4']

print('Index 0:',  list1[0])  # Index 0: item 1
print('Index 3:',  list1[3])  # Index 3: item 4
print('Index -1:', list1[-1]) # Index -1: item 4
print('Index -4:', list1[-4]) # Index -4: item 1

print('Slice [1:3]:', list1[1:3]) # Slice [1:3]: ['item 2', 'item 3']
print('Slice [1:]:', list1[1:]) # Slice [1:]: ['item 2', 'item 3', 'item 4']
print('Slice [:3]:', list1[:3]) # Slice [:3]: ['item 1', 'item 2', 'item 3']

list1[1] = 'other item'
print(list1) # ['item 1', 'other item', 'item 3', 'item 4']

del list1[2];
print(list1) # ['item 1', 'other item', 'item 4']
```

@@

## Alternative initializations

```python
list2 = [2*i for i in range(10)]
print(list2) # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]

list3 = [i*i for i in list2]
print(list3) # [0, 4, 16, 36, 64, 100, 144, 196, 256, 324]

list4 = [[i*j for i in range(3)] for j in range(10)]
print(list4) # [[0, 0, 0], [0, 1, 2], [0, 2, 4], [0, 3, 6], [0, 4, 8], [0, 5, 10], [0, 6, 12], [0, 7, 14], [0, 8, 16], [0, 9, 18]]

for row in list4:
	print(row)

# [0, 0, 0]
# [0, 1, 2]
# [0, 2, 4]
# [0, 3, 6]
# [0, 4, 8]
# [0, 5, 10]
# [0, 6, 12]
# [0, 7, 14]
# [0, 8, 16]
# [0, 9, 18]

print(list4[5][2]) # 10
```

@@

### Common Operations

```python
list5 = [1, 2, 3]

# Length
print(len(list5)) # 3

# Concatenation
print(list5 + [4, 5, 6]) # [1, 2, 3, 4, 5, 6]

# Repetition
print(['A'] * 3) # ['A', 'A', 'A']	

# Membership
print(3 in list5) # True
print(4 in list5) # False

# Min/Max
print(max(list5), min(list5)) # 3 1

# Append list.append(obj)
list5.append(2)
print(list5) # [1, 2, 3, 2]

# Insert list.insert(index, obj)
list5.insert(1, 4)
print(list5) # [1, 4, 2, 3, 2]

# Remove list.remove(obj)
list5.remove(2)
print(list5) # [1, 4, 3, 2]

# Count list.count(obj)
print(list5.count(2)) # 2
```

@@@

## Tuples

A sequence of immutable Python objects.

```python
tuple1 = ('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h')

print(tuple1[0])  # 'a'
print(tuple1[-2]) # 'g'
print(tuple1[2:6]) # ('c', 'd', 'e', 'f')

print(len(tuple1)) # 8

x, y, z = (1, 2, 3)
print(x) # 1 
print(y) # 2
print(z) # 3

print((1, 2) + (3, 4, 5)) # (1, 2, 3, 4, 5)

s = ''
for x in tuple1:
  s += x
print(s) # 'abcdefgh'
```


@@@

## Sets

Unordered collections of unique elements

```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
print(basket) # {'orange', 'banana', 'pear', 'apple'}

print('orange' in basket) # True
print('grape' in basket)  # False
```

@@

## Set operations

```python
a = set('abracadabra')
b = set('alacazam')

# unique letters in a
print(a) # {'a', 'r', 'b', 'c', 'd'}

# letters in a but not in b
print(a - b) # {'r', 'd', 'b'}

# letters in a or b or both
print(a | b) # {'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}

# letters in both a and b
print(a & b) # {'a', 'c'}

# letters in a or b but not both
print(a ^ b) # {'r', 'd', 'b', 'm', 'z', 'l'}
```

@@

## Set Methods

| Method              | Description |
|:--------------------|:------------|
| my_set.add(obj)     | Add an object to a set |
| my_set.clear()      | Remove all elements |
| my_set.discard(obj) | Remove an element from set if it is a member |
| my_set.pop()        | Remove and return an arbitrary element |

[https://docs.python.org/3/library/stdtypes.html#set](https://docs.python.org/3/library/stdtypes.html#set)

@@@

## Dictionaries

Mappings `key -> value`.

```python
d = {'a': 11, 'c': 89}

print(d['c']) # 89

d['b'] = 12
print(d) # {'c': 89, 'a': 11, 'b': 12}

del d['a']
print(d) # {'c': 89, 'b': 12}

print(len(d)) # 2

d = {x: x**2 for x in (2, 4, 6)}
print(d) # {2: 4, 4: 16, 6: 36}
```

@@

## Looping Techniques

```python
d = dict(aaa=123, bbb=456, ccc=789)

for key in d:
  print(key, d[key])
# bbb 456
# ccc 789
# aaa 123
  
for value in d.values():
  print(value)
# 456
# 789
# 123

for key, value in d.items():
  print(key, value)
# bbb 456
# ccc 789
# aaa 123
```