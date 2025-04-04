# Print
`System.out.print` в Java — это метод, который используется для вывода данных в консоль (или терминал) 
без добавления символа новой строки в конце. То есть, после использования `print`, курсор остается на той же строке, 
а следующий вывод будет происходить в той же строке, если только не будет вызван другой метод (например, `println`).
<h2> Различие между `System.out.print` и `System.out.println`:</h2>

+ `System.out.print` — выводит данные без добавления новой строки в конце.
+ `System.out.println` — выводит данные и добавляет символ новой строки после вывода, то есть курсор переходит на следующую строку.

`System.out` в Java — это объект, который представляет собой стандартный поток вывода (обычно, это консоль или терминал). Он используется для вывода данных, таких как текст или числа, на экран.
Расшифровка:
+ `System` — это класс из стандартной библиотеки Java в пакете `java.lang`, который предоставляет доступ к системным ресурсам и информации.
+ `out` — это публичное статическое поле в классе `System`, представляющее поток вывода (тип `PrintStream`), связанный с консолью.

### Пример использования `System.out.println`:
```java
public class Main {
    public static void main(String[] args) {
        // Выводим строки с использованием println
        System.out.println("Привет, мир!");
        System.out.println("Как дела?");
        System.out.println("Java — это здорово!");
    }
}
```
**Результат выполнения:**
```
Привет, мир!
Как дела?
Java — это здорово!
```
**Объяснение:**
1. Каждое использование `System.out.println` выводит текст или данные на экран, добавляя новую строку после каждого вызова. Это позволяет результатам быть более структурированными, так как каждый вывод начинается с новой строки.

2. В примере:
   + Первая строка выводит `"Привет, мир!"`, и курсор перемещается на новую строку.
   + Вторая строка выводит `"Как дела?"` на новой строке.
   + Третья строка выводит `"Java — это здорово!"` также на новой строке.

**Когда использовать `System.out.println`:**
+ Когда нужно, чтобы вывод был на новой строке после каждого сообщения.
+ Для упрощения восприятия вывода данных пользователем, добавляя четкие разделения между результатами.

### Пример использования `System.out.print`:
```java
public class Main {
    public static void main(String[] args) {
        System.out.print("Привет");
        System.out.print(", ");
        System.out.print("мир!");
    }
}
```
**Результат:**
```
Привет, мир!
```
Как видите, все выводится на одной строке, так как `print` не добавляет символ новой строки.
### Почему использовать `System.out.print`?
+ **Вывод на той же строке**: Когда нужно вывести несколько частей текста или чисел на одной строке, не начиная с новой строки после каждого вывода.

**Пример:**
```java
public class Main {
    public static void main(String[] args) {
        int count = 5;
        System.out.print("Количество: ");
        System.out.print(count);
    }
}
```
**Результат:**
```
Количество: 5
```
**Итог:**
`System.out.print` полезен, когда вы хотите вывести несколько элементов на одной строке, без перехода на новую строку.

<h2>System.out.printf()</h2>

Этот метод используется для форматированного вывода. Он позволяет выводить строки с подстановкой значений и заданиям специфического формата (например, для чисел, дат и так далее). Форматирование задаётся с помощью специального синтаксиса, похожего на форматирование в языке C.

**Пример:**
```java
int age = 25;
System.out.printf("I am %d years old\n", age);
```
**Вывод:**
```CSS
I am 25 years old
```

<h2>System.out.format()</h2>

Этот метод является синонимом метода printf() и работает точно так же, то есть тоже позволяет форматировать строки. Он просто использует другой стиль имени метода.

**Пример:**
```java
double pi = 3.14159;
System.out.format("Value of pi: %.2f\n", pi);
```
**Вывод:**
```lua
Value of pi: 3.14
```
**Разница между методами:**
+ `print()` выводит текст без новой строки.
+ `println()` выводит текст и добавляет новую строку.
+ `printf()` и `format()` позволяют выводить строки с форматированием (например, ограничение числа знаков после запятой, выравнивание и так далее).

**Заключение**
Выбирайте метод в зависимости от того, требуется ли вам добавление новой строки в конце, или вам нужно форматировать вывод. Если требуется просто вывести текст, `print` и `println` — это простые и удобные методы. Если же нужно вывести данные в определённом формате, используйте `printf` или `format`.

<h2>Форматные спецификаторы:</h2>

Метод `printf` принимает строку формата, в которой могут быть указаны специальные форматированные спецификаторы (например, для вывода чисел, строк, дат и т. д.), а затем аргументы, которые должны быть подставлены в эти места.
+ `%d` — для целых чисел.
+ `%f` — для чисел с плавающей точкой (например, для `double`).
+ `%s` — для строк.
+ `%x` — для шестнадцатеричных чисел.

**Пример:**
```java
public class Main {
    public static void main(String[] args) {
        String name = "Алексей";
        int age = 30;

        System.out.printf("Имя: %s, Возраст: %d лет\n", name, age);
    }
}
```
**Вывод**
```
Имя: Алексей, Возраст: 30 лет
```
Метод `printf` помогает сделать вывод данных более читаемым и структурированным, позволяя задавать точный формат для различных типов данных.
