[Java Tutorial for Beginners [2020]](https://www.youtube.com/watch?v=eIrMbAQSU34)
## Package
- use package to group related classes 
- com.<packageName>
- ``package come.<packageName>`` on top of class file (e.g. Main.java);

## filename
- ends with ``.java``

## Running Java program
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
## Code
```java
public class Main{ // main class, class (PascalNamingConvention)
  
  public static void main(){ // main function, function (camelNamingConvention)
  
  }
}
```
```java
System.out.println(" "); // print

```
