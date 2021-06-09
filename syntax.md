[Java Tutorial for Beginners [2020]](https://www.youtube.com/watch?v=eIrMbAQSU34)
## Package
- use package to group related classes 
- com.<packageName>
- ``package come.<packageName>`` on top of class file (e.g. Main.java);

## filename
- ends with ``.java``

# Running Java program
### Compilation
- Use Java compiler(comes with Java development kit) to compile Source code (.java files) to Byte Code (.class files)
```
$ javac Main.java
(will create Main.class file, can be run on any OS that has Java Runtme Environment (JRE))

```
### Execution
- Java Runtme Environment(JRE) has Java Virtual Machine takes Java Byte Code and translate it into Native Code for the underlying operating system
- Java is portable or platform independent, you can write on Windows and run on Linux
```
$ cd ../../src
$ java com.<packagename>.Main  //look for Main.class
```
  
---
  
# Data Types
### Primitive
- for storing simple values
- byte: 1 byte [-128, 127]
- int: 4 bytes [-2B, 2B] **(use _ to make it readable)**
   - ``int viewsCount = 123_456_789; // use _ to make it readable``
- long: 8 bytes **(need to add 'L' at the end)**
  - ``long viewsCount = 3_123_456_789L; // need to add 'L' at the end``
- float: **(need to add 'F' at the end)**
  - ``float price= 10.99F;``
- double: 8 bytes
- boolean: 1 byte
### Reference (non-primitive)
- for storing complex objects
  
# Code
```java
public class Main{ // main class, class (PascalNamingConvention)
  
  public static void main(){ // main function, function (camelNamingConvention)
  
  }
}
```
```java
System.out.println(" "); // print

```
