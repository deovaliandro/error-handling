Try dan catch adalah keywordyang digunakan untuk menangkap exception. Try digunakan untuk menjalankan kode dan ketika terjadi error, maka akan ditangkap oleh catch.

Contohnya:

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

Contoh lain:

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

### Penting untuk diingat

1.Jika kita tidak memberikan jenis exception yand ditangkap, maka Java kaan menggunakan default exception dimana error akan ditampilkan detail di terminal.
2. Super class `Throwable` akan meng-override `toString()`, untuk menampilkan error dalam bentuk string.
3. Ketika menggunakan multiple catch, pastikan sub-class exeption ditulis sebelum superclassnya untuk mencegah error.
4. Dalam try-catch bercabang, try yang lebih dalam digunakan untuk menangkap error sendiri, namun bisa juga menggunakan exception yang lebih diatasnya jika diperlukan.
5. Hanya jenis objek class `Throwable` atau sub-classnya yang dapat di thrown.