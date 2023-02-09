```java
// FakeNode используется только в чачестве головы и хвоста
public class FakeNodeLinkedList2 {}
```
Переносим комментарий на класс FakeNode согласно пункту 1.

---
```java
// Находит целые числа в строке
private static void initializeExpressionStack(String expression) {
    List<Object> list = new LinkedList<>();

    Pattern integerPattern = Pattern.compile("\\d+");
```
Переносим комментарий на строку `Pattern integerPattern` согласно пункту 1.

---
```java
// Находит целые числа в строке
Pattern integerPattern = Pattern.compile("\\d+");
Matcher matcher = integerPattern.matcher(expression);
```
Переделываем на `Регулярное выражение ищет целые числа в строке символов` согласно пункту 2.

---
```java
public class PostfixCalculator {
    
    // Вычисляет любое математическое выражение
    public  Integer calculate(String expression) {}
}
```
Информация не точная. Переделываем на `Вычисляет выражение в постфиксной записи, содержащее +,-,*,/` согласно пункту 3.

---
```java
public class PostfixCalculator {
    
    // Проверяет, равны ли 2 объекта
    public  boolean equals(Object firstObg, Object secondObg) {}
}
```
Убираем комментарий согласно пункту 4.

---
```java
/**
 * Данный класс предназначен исключительно для тестирования.
 */
```
Заголовок добавлен согласно пункту 5.

---
```java
/**
 * Стек, значения которого кладутся и забираются не с конца, а с начала.
 */
public class InvertedStack<T> {}
```
Убираем комментарий согласно пункту 7.

---
Убираем комментарий с сыылкой на confluence, где перечисляется историЯ изменений фичи согласно пункту 8.

---
`// Этот класс содержит единственное обращение к базе данных в этом пакете`  
Убираем комментарий согласно пункту 9.

---
Класс DocumentUtil. Убираем комментарий с каждого метода и даём общий комментарий классу согласно пункту 10.

---
```java
public class PostfixCalculator {
    
//    private static Integer doOperation(Integer firstOperand, Integer secondOperand, Character operation) {
//      ...
```
Удаляем комментарий с неиспользуемым кодом согласно пункту 11. Метод заменён на лямбду.

---
```java
    private static final Map<Character, Operation> operations = Map.of(
        PLUS, Integer::sum,
        MINUS, (k, l) -> k - l,
        MULTIPLY, (k, l) -> k * l,
        DIVIDE, (k, l) -> k / l
        );
```
Убраны комментарии с лямбд согласно пункту 12. Код достаточно нагляден.
