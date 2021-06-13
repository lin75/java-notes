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
### Primitive types(total of 8)
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
### Reference types (non-primitive)
- for storing complex objects
- Date (import java.util.Date;)
  - ``Date now = new Date();``
- Point (import java.awt.*;)
  - **point1 and point2 are referencing the exact same point object in memory**
  ```java
    Point point1 = new Point(x:1, y:1);
    Point point2 = point1;
    point1.x = 2; // update value
  ```
- **String is also Reference type**
  - **String is IMMUTABLE, it will always create a new String object and return it**
  ```java
    String message = "Hello World"; 
    message.endsWith("!!"); // check if message ends with "!!"
    message.startsWith("!!");
    message.length();
    message.indexOf("H"); // first index of first 'H', if not existed return -1
  
    // methods return new string object
    message.replace("!", "*"); // message.replace(targe, replacement); 
    message.toLowerCase();
    message.trim(); // remove extra white space in the beginning or the end of the string
  ```
- **int []** && **Arrays**
  ```java
    int [] numbers = new int[5];
    numbers[0]=1;
    System.out.println(Arrays.toString(numbers)); // printing int []
    Arrays.sort(numbers); // sort the array
    int [] numbers2 = {2, 3, 4};
  ```
- multi-dimensional array
  ```java
    int[][] numbers = new int[2][3];
    System.out.println(Arrays.deepToString(numbers)); // printing int [][]
  ```
  
# Code
```java
public class Main{ // main class, class (PascalNamingConvention)
  
  public static void main(String[] args){ // main function, function (camelNamingConvention)
  
  }
}
```
```java
final float PI = 3.14F;
short x = 1;
int y = x+2; // int + short: 
int x = (int)1.1;
String x = "1";
Integer.parseInt(x); // takes a string and returns a int
String x = "1.1";
Double.ParseDouble(x);
```
### Math class
```java
Math.round(1.1F); // return a long 1, unless you add (int)in front of it
Math.ceil(1.1F); // return double of 2.0
(int)Math.ceil(1.1F); // 2 
Math.max(1, 2);
Math.min(1,2);
Math.random(); // return a double between 0 and 1
Math.round(Math.random() * 100) ; // between 0 to 100
(int)(Math.random()*100); //between 0 to 100  
```



 
```
