Try and catch both are Java keywords and used for exception handling. The try block is used to enclose the suspected code. Suspected code is a code that may raise an exception during program execution.

```java
try {
    int a = 12;
    int b = 5;
    int c = a/b;
} catch(ArithmeticException e){
    System.out.println(e);
}
```

Multiple try-catch:

```java
try {
    Integer in = new Integer("abc");
    in.intValue();
} catch (ArithmeticException e) {
    System.out.println("Arithmetic " + e);
} catch (NumberFormatException e) {
    System.out.println("Number Format Exception " + e); 
}
```

Example:

```java
public class Main {
    public static void main(String[] args) {
        try {
            int a[]=new int[10];    
            System.out.println(a[20]);  
        } catch(ArithmeticException e) {
            System.out.println("Arithmetic Exception "+e);  
        } catch(ArrayIndexOutOfBoundsException e) {
            System.out.println("ArrayIndexOutOfBounds Exception "+e);  
        } catch(Exception e) {
            System.out.println(e);  
        }
    }
}
```

### Important points to Remember

1. If you do not explicitly use the try catch blocks in your program,  Java will provide a default exception handler, which will print the  exception details on the terminal, whenever exception occurs.
2. Super class `Throwable` overrides `toString()` function, to display error message in form of string.
3. While using multiple catch block, always make sure that sub-classes  of Exception class comes before any of their super classes. Else you  will get compile time error.
4. In nested try catch, the inner try block uses its own catch block as well as catch block of the outer try, if required.
5. Only the object of `Throwable` class or its subclasses can be thrown.