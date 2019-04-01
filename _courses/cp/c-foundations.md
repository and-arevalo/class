---
layout: slide
title: C++ Foundations
---

## Hello World!

### Python
```python
print('Hello World!')
```

### C++
```c++
#include <iostream>

int main(){
	std::cout << "Hello World!" << std::endl;
	return 0;
}
```

@@@

## Console output

A simple operation between 3 5 20 : 160

### Python
```python
print('A simple operation between', 3, 5, 20, ':', (3+5) * 20)
```
	
### C++
```c++
#include <iostream>

int main(){
	std::cout << "A simple operation between " << 3 
	<< " " << 5 << " " << 20 << " : " << (3+5)*20 << std::endl;
		
	return 0;
}
```

@@@

## User input

### Python
```python
n = int(input())
```
	
### C++
```c++
#include <iostream>

int main(){
	int n;
	std::cin >> n;
	
	return 0;
}
```

@@@

## Variables

### Python

A dynamically typed programming language 

```python
a = 123456789
```

### C

A static typed programming language 

```c++
int a = 123456789;
```

@@

## [C data types](https://en.wikipedia.org/wiki/C_data_types)


| Type | Bytes |
|:----:|:-----:|
| char, signed char, unsigned char | 1 |
| short, unsigned short | 2 |
| int, unsigned int | 4 |
| long, unsigned long | 8 |
| long long, unsigned long long | 16 |
| float | 4 |
| double | 8 |
| long double | 16 |

@@

## Integer overflow

```c++
#include <iostream>

int main(){
    short n;
    std::cout << n << std::endl; // 0
	
	n += 30000;
	std::cout << n << std::endl; // 30000
	
	n += 30000;
	std::cout << n << std::endl; // -5536

    return 0;
}
```

@@@

## Conditionals

### Python
```python
if n % 2 == 0:
	print(n, 'is even')
else:
	print(n, 'is odd')
```

### C++
```c++
if (n % 2 == 0){
	std::cout << n << " is even" << std::endl;
} else {
	std::cout << n << " is odd" << std::endl;
}
```

```c++
std::cout << n << (n % 2 == 0 ? " is even" : " is odd") << std::endl;
```

@@

## Logical operators

| Python | C++ |
|:------:|:---:|
| not | ! |
| and | && |
| or | &#124;&#124; |

@@@

## While Loop

### Python
```python
n = 5
while n > 0:
  print(n)
  n -= 1
```

### C++
```c++
int n = 5;
while (n > 0){
	std::cout << n << std::endl;
	n--;
}
```

@@

## Do While Loop

### C++

```c++
int n = 0;
while (n > 0){
	std::cout << n << std::endl;
	n--;
	// This block is executed only while the condition is true
}
```

```c++
int n = 0;
do {
	std::cout << n << std::endl;
	n--;
	// This block is executed minimum one time
	// and is repeated while the condition is true
} while (n > 0);
```

@@@

## For

### Python
```python
for i in range(5):
  print(n)
```

### C++
```c++
for (int i=0; i<5; i++){
  std::cout << i << std::endl;
}
```

```c++
for (<Initialization>; <Condition>; <Increment>){
	...
}
```

@@@

## Functions
### Python
```python
def isEven(n):
	return n % 2 == 0
print(isEven(10), isEven(23))
```

### C++
```c++
#include <iostream>

bool isEven(int n){
	return n % 2 == 0;
}
int main(){
    std::cout << isEven(10) << " " << isEven(23) << std::endl;
    return 0;
}
```

@@

### Void type

```c++
#include <iostream>

void greets(std::string str){
	std::cout << "Hello " << str << "!" << std::endl;
}

int main(){
    std::string str;
	std::cin >> str;
    greets(str);
	
    return 0;
}
```

@@

### Namespaces

```c++
#include <iostream>
using namespace std;

void greets(string str){
	cout << "Hello " << str << "!" << endl;
}

int main(){
    string str;
	cin >> str;
    greets(str);
	
    return 0;
}
```

@@@

## Arrays

```c++
#include <iostream>
using namespace std;

int main(){
	int n = 10;
	int arr[n];
	for (int i=0; i<n; i++){
		cout << arr[i] << " ";
	}
	cout << endl;
	
	int arr2[n] = {};
	for (int i=0; i<n; i++){
		cout << arr2[i] << " ";
	}
	cout << endl;
	
    return 0;
}
```

@@

## Matrices

```c++
#include <iostream>
using namespace std;

int main(){
	int n = 10;
	int m = 5;
	
	int arr[n][m] = {};
	for (int i=0; i<n; i++){
		for (int j=0; j<m; j++){
			cout << arr[i][j] << " ";
			arr[i][j] = i * j;
		}
		cout << endl;
	}
	
	cout << endl;
	
	for (int i=0; i<n; i++){
		for (int j=0; j<m; j++){
			cout << arr[i][j] << " ";
		}
		cout << endl;
	}
	
    return 0;
}
```

@@

## Multidimensional arrays

```c++
#include <iostream>
using namespace std;

int main(){
	int n = 10;
	int m = 5;
	int o = 3;
	
	int arr[n][m][o] = {};
	for (int i=0; i<n; i++){
		for (int j=0; j<m; j++){
			for (int k=0; k<o; k++){
				arr[i][j][k] = i * j * k;
			}
		}
	}
	
	for (int i=0; i<n; i++){
		for (int j=0; j<m; j++){
			for (int k=0; k<o; k++){
				cout << arr[i][j][k] << " ";
			}
			cout << endl;
		}
		cout << endl;
	}
	
    return 0;
}
```