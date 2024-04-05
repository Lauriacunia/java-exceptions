## Exceptions in Java

### Example of how to use exceptions in Java

<img src="https://github.com/Lauriacunia/java-exceptions/assets/63796774/0b5ecc91-f3ec-49a5-a899-04e90e72ca26" />

### Throw & Throws

- **Throw**: Used to throw an exception explicitly.
- **Throws**: Used to declare an exception.

### Example

```java
public class Main {
    public static void main(String[] args) {
        try {
            metodo1();
        } catch (Exception e) {
            System.out.println("Excepcion capturada en main");
        }
    }

    public static void metodo1() throws Exception {
        metodo2();
    }

    public static void metodo2() throws Exception {
        metodo3();
    }

    public static void metodo3() throws Exception {
        throw new Exception();
    }
}
```

<img src="https://github.com/Lauriacunia/java-exceptions/assets/63796774/8bea6e80-7029-4041-8743-297a017b8e5b" />
