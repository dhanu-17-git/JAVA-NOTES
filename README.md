☕ JAVA MODULE 1 – INTRODUCTION & BASICS

Welcome to your first Java Module!
Here we'll cover everything from OOP concepts to control statements — in the clearest and most beginner-friendly way possible 👇

---

🧠 1️⃣ Object-Oriented Programming (OOP)

Definition / Concept
Object-Oriented Programming (OOP) organizes a program around objects — each representing a real-world entity with data (fields) and behavior (methods).

OOP makes programs more reusable, flexible, and easier to maintain.

---

⚔️ Procedural vs Object-Oriented Programming

Feature Procedural (e.g., C) Object-Oriented (e.g., Java)
Focus Functions / Procedures Objects & Classes
Data Access Global / Free Controlled via Encapsulation
Reusability Difficult High
Example printf(), scanf() System.out.println()

---

💡 Core OOP Principles

🧩 1. Encapsulation

Definition: Wrapping data (variables) and code (methods) together.

Syntax:

```java
class Student {
    private int age;
    public void setAge(int a) { age = a; }
    public int getAge() { return age; }
}
```

Output:

```
No direct output (data hidden and accessed via methods)
```

Explanation:
Think of a capsule — medicine inside, label outside. You can use it but not see what's inside! That's how encapsulation protects your data.

---

🧬 2. Inheritance

Definition: One class acquiring properties and methods of another.

Syntax:

```java
class Parent {
    void display() { System.out.println("Parent class"); }
}
class Child extends Parent {
    void show() { System.out.println("Child class"); }
}
```

Output:

```
Parent class
Child class
```

Explanation:
Just like a child inherits traits from parents, a subclass inherits features of a superclass.

---

🦸‍♂️ 3. Polymorphism

Definition: The ability of one action to behave differently in different contexts.

Syntax:

```java
class Animal {
    void sound() { System.out.println("Animal sound"); }
}
class Dog extends Animal {
    void sound() { System.out.println("Bark"); }
}
```

Output:

```
Bark
```

Explanation:
Same method name → different behaviors. "sound()" means one thing for an Animal, and another for a Dog 🐶.

---

🧱 2️⃣ Code Blocks

Definition / Concept
A block groups multiple statements together using {} braces.

Example:

```java
{
    int a = 10;
    System.out.println(a);
}
```

Output:

```
10
```

Explanation:
Anything inside {} runs together — like a small self-contained program section.

---

✍️ 3️⃣ Lexical Elements

Element Description Example
Whitespace Ignored spaces/tabs/newlines int x = 5;
Identifiers Names for variables, classes, etc. class Car {}
Literals Constant fixed values 10, 'A', "Hello"
Comments Explain code // comment or /* comment */
Separators Special syntax marks () { } , ; .
Keywords Reserved words if, class, for, return

---

🔢 4️⃣ Data Types

Type Size Example
byte 1 byte byte b = 10;
short 2 bytes short s = 200;
int 4 bytes int a = 1000;
long 8 bytes long l = 10000L;
float 4 bytes float f = 2.5f;
double 8 bytes double d = 3.14;
char 2 bytes char c = 'A';
boolean 1 bit boolean flag = true;

Example:

```java
int age = 20;
float marks = 95.5f;
char grade = 'A';
System.out.println("Age: " + age + ", Marks: " + marks + ", Grade: " + grade);
```

Output:

```
Age: 20, Marks: 95.5, Grade: A
```

Explanation:
Data types define what kind of value can be stored. It's like different boxes: one for numbers, one for letters, etc.

---

💼 5️⃣ Variables

Syntax:

```
datatype variableName = value;
```

Example:

```java
String name = "Dhanush";
int age = 20;
System.out.println(name + " is " + age + " years old.");
```

Output:

```
Dhanush is 20 years old.
```

Explanation:
Variables store data you can use later — like keeping a note instead of repeating info.

---

🔄 6️⃣ Type Conversion & Casting

🔹 Widening (Automatic)

```java
int a = 10;
double b = a;
System.out.println(b);
```

Output:

```
10.0
```

🔹 Narrowing (Manual)

```java
double x = 9.8;
int y = (int)x;
System.out.println(y);
```

Output:

```
9
```

Explanation:
Widening = safe (small → big box).
Narrowing = risky (big → small box).

---

⚡ 7️⃣ Automatic Type Promotion

Example:

```java
byte a = 10;
byte b = 20;
int c = a * b;  // promoted to int
System.out.println(c);
```

Output:

```
200
```

Explanation:
When performing math, Java automatically promotes small types like byte to int.

---

🧮 8️⃣ Arrays

Syntax:

```
datatype[] arrayName = new datatype[size];
```

Example:

```java
int[] marks = {85, 90, 95};
for(int i : marks) {
    System.out.println(i);
}
```

Output:

```
85
90
95
```

Explanation:
Arrays store multiple values of the same type — like a row of lockers 🔒.

---

➕ 9️⃣ Operators

Type Symbol Example Meaning
Arithmetic + - * / % a + b Math operations
Relational < == != a > b Compare values
Logical && \|\| ! a>0 && b>0 Combine conditions
Assignment = += -= *= /= a += 5 Update variable
Ternary ?: (a>b)?a:b Short if-else

Example:

```java
int a = 10, b = 5;
System.out.println(a + b);
System.out.println(a > b);
System.out.println((a > b) ? "A is big" : "B is big");
```

Output:

```
15
true
A is big
```

Explanation:
Operators are tools that help Java calculate, compare, and decide.

---

🔁 🔟 Control Statements

🧩 If-Else

```java
int marks = 75;
if (marks >= 50)
    System.out.println("Pass");
else
    System.out.println("Fail");
```

Output:

```
Pass
```

🔄 For Loop

```java
for(int i=1; i<=3; i++)
    System.out.println("Count: " + i);
```

Output:

```
Count: 1
Count: 2
Count: 3
```

🔂 Do-While Loop

```java
int i = 1;
do {
    System.out.println("i = " + i);
    i++;
} while(i <= 3);
```

Output:

```
i = 1
i = 2
i = 3
```

⚡ For-Each Loop

```java
int[] nums = {10, 20, 30};
for(int n : nums)
    System.out.println(n);
```

Output:

```
10
20
30
```

🏁 Jump Statements

```java
for(int i=1;i<=5;i++){
    if(i==3) continue;
    if(i==5) break;
    System.out.println(i);
}
```

Output:

```
1
2
4
```

Explanation:
continue → skip this turn
break → stop loop
return → exit method

---

🧾 MODULE 1 SUMMARY

Topic Description
OOP Concepts Encapsulation, Inheritance, Polymorphism
Lexical Elements Keywords, Identifiers, Literals
Data Types Primitive and Non-Primitive
Variables Store values
Type Conversion Widening and Narrowing
Arrays Store multiple values
Operators Arithmetic, Logical, etc.
Control Statements Decision & Looping Structures

---

💡 Tip:

If you ever feel confused — just remember:

Java = "Objects that talk to each other" 🤝

---

🧠 End of Module 1 – You're now Java Ready! 🚀

---

