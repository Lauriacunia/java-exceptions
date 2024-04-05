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

### Si la excepción es capturada por un catch, el flujo de ejecución continúa normalmente. Se ejecuta el código que sigue al catch. Pero si la excepción no es capturada, el flujo de ejecución se detiene y se muestra un mensaje de error.

### Try & Catch & Finally

- **Try**: Used to define a block of code in which we want to check for exceptions.
- **Catch**: Used to handle the exception.
- **Finally**: Used to execute important code such as closing a connection, whether an exception is thrown or not.

### Example

```java
public class Main {
    public static void main(String[] args) {
        try {
            metodo1();
        } catch (Exception e) {
            System.out.println("Excepcion capturada en main");
        } finally {
            System.out.println("Finally en main");
        }
    }

    public static void metodo1() throws Exception {
        try {
            metodo2();
        } catch (Exception e) {
            System.out.println("Excepcion capturada en metodo1");
        } finally {
            System.out.println("Finally en metodo1");
        }
    }

    public static void metodo2() throws Exception {
        try {
            metodo3();
        } catch (Exception e) {
            System.out.println("Excepcion capturada en metodo2");
        } finally {
            System.out.println("Finally en metodo2");
        }
    }

    public static void metodo3() throws Exception {
        throw new Exception();
    }
}
```
