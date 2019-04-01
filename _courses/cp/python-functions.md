---
layout: slide
title: Python Functions
---

### Functions

f(x,y) = ?

```python
def sum(a, b):
	return a + b

def fibonacci(n):
	if n == 0:
		return 0
	elif n == 1:
		return 1
	else:
		return sum(fibonacci(n-1), fibonacci(n-2))

for i in range(10):
	print(fibonacci(i))
```

@@@

### Useful functions

- `print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`
- `range([start], stop[, step])`
- `str(object)`
- `int(x, base=10)`
- `float(x)`
- `pow(x, y[, z])`
- `chr(i)`
- `ord(c)`
- `input([prompt])`

@@@

### Lambda functions

`lambda arguments : expression`

<div class="half-column">
{% highlight python %}
def add(x, y): 
    return x + y

add(10, 20) # 30
{% endhighlight %}
</div>

<div class="half-column">
{% highlight python %}
add = lambda x, y : x + y 
add(10, 20) # 30
{% endhighlight %}
</div>

@@@

### Python Scope resolution - LEGB Rule

- L, Local: Within a function (def or lambda).

- E, Enclosing-function locals: Local scope of all statically enclosing functions (def or lambda).

- G, Global: At the top-level of a module file, or by executing a global statement.

- B, Built-in: Preassigned built-in names module (range, print, ...).

@@

### Example
```python
i = 1
def function1():
    i = 2
    print(i, 'in function1()')

print(i, 'in global')
function1()
print(i, 'in global')
```

<div class="fragment">
{% highlight python %}
1 in global
2 in function1()
1 in global
{% endhighlight %}
</div>

@@

### Example

{% highlight python %}
var1 = 1
def function1(a):
	var2 = var1 + 1
	def function2(b):
		var3 = var2 + 1
		for var4 in range(10):
			var3 += var4
        
		return var3
    
	return function2(a + var2)

print(function1(10))
{% endhighlight %}

<div class="fragment">
{% highlight python %}
48
{% endhighlight %}
</div>
