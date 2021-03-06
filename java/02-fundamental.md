# Table of Contents

1. [Types](#types)
2. [String](#string)
3. [Escape Sequences](#escape-sequences)
4. [Arrays](#arrays)
5. [Constants](#constants)
6. [Arithmetic Expressions](#arithmetic-expressions)
7. [Casting](#casting)
8. [Math Class](#math-class)
9. [Formatting Numbers](#formatting-numbers)
10. [Reading Input](#reading-input)

## Types

- `Primitive Types`, for storing simple values
- `Reference Types`, for storing complex objects

### Primitive Types

| Type    | Bytes |    Range     |
| ------- | ----: | :----------: |
| byte    |     1 |  [-128,127]  |
| short   |     2 |  [-32k,32k]  |
| int     |     4 |  [-2b, 2b]   |
| long    |     8 |              |
| float   |     4 |              |
| double  |     8 |              |
| char    |     2 | A, B, C, ... |
| boolean |     1 |  true/false  |

Example

```java
byte age = 30;
int viewsCount = 123_456_789;
long population = 3_123_456_789L;
float price = 10.99F;
char letter = 'A';
boolean isEligible = false;
```

### Reference Types

Need use `new` to allocate memory

Example

```java
import java.util.Date;

Date now = new Date();
```

## String

String is reference type, but use it often, short way to declare

```java
String message = "Hello World";
```

String is immutable

```java
System.out.println(message.toLowerCase());
// hello world
System.out.println(message);
// Hello World
```

## Escape Sequences

```java
String message = "Hello \"World\"";
// Hello "World"
String path = "c:\\Windows\\..."
// c:\Windows\...
```

## Arrays

```java
import java.util.Arrays;

int[] numbers = new int[5];

numbers[0] = 1;
numbers[1] = 2;

System.out.println(Arrays.toString(numbers));
```

Another way to declare Array

```java
int[] numbers = {2, 3, 5, 1, 4};

Arrays.sort(numbers);
Arrays.toString(numbers);
```

Multi-Dimensional Arrays

```java
int[][] numbers = new int[2][3];
numbers[0][0] = 1;
System.out.println(Arrays.deepToString(numbers));
```

```java
int[][] numbers = { { 1, 2, 3 }, { 4, 5, 6 } };
numbers[0][0] = 7;
System.out.println(Arrays.deepToString(numbers));
```

## Constants

```java
final float PI = 3.14F;
```

## Arithmetic Expressions

```java
int result = 10 / 3;
// 3
```

```java
double result = (double) 10 / (double) 3;
// 3.3333333333333335
```

```java
int x = 1;
int y = x++;
System.out.println(x); // 2
System.out.println(y); // 1
```

```java
int x = 1;
int y = ++x;
System.out.println(x); // 2
System.out.println(y); // 2
```

Compound assignment operators

```java
1.    +=   (compound addition assignment operator)
2.    -=   (compound subtraction assignment operator)
3.    *=   (compound multiplication assignment operator)
4.    /=   (compound division assignment operator)
5.    %=   (compound modulo assignment operator)
6.    &=   (compound Bitwise & assignment operator)
7.    |=   (compound Bitwise | assignment operator)
8.    ^=   (compound Bitwise ^ assignment operator)
9.    >>=  (compound right-shift assignment operator)
10.   >>>= (compound right-shift filled 0 assignment operator)
11.   <<=  (compound left-shift assignment operator)
```

## Casting

Implicit casting

```java
short x = 1;
int y = x + 2;
System.out.println(y); // 3
```

Explicit casting

```java
double x = 1.1;
int y = (int) x + 2;
```

## Math Class

```java
int result = Math.round(1.1F);
int ceiling = (int) Math.ceil(1.1F);
int floor = (int) Math.floor(1.1F);

int ran = (int) (Math.random() * 100);
```

## Formatting Numbers

```java
import java.text.NumberFormat;
NumberFormat currency = NumberFormat.getCurrencyInstance();
String result = currency.format(1234567.891);
System.out.println(result); // $1,234,567.89
```

```java
import java.text.NumberFormat;
String result = NumberFormat.getPercentInstance().format(0.1);
System.out.println(result); // 10%
```

## Reading Input

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
System.out.print("Name: ");

String name = scanner.nextLine().trim();
System.out.println("You are " + name);

scanner.close();
```
