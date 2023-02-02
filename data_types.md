Заменить невалидное приведение  
```java
boolean intChar(char c) {
    switch ((int) c) {
        case (0):
        case (1):
        ...
```
на 
`switch (Character.getNumericValue(c))`

---
Где можно, стараться использовать методы valueOf() классов Integer, Double и др., особенно для преобразования между числовыми и строчными типами.

---
Для предотвращения деления на 0 использовать условие перед вычислением:  
```java
if (divider == 0) {}
```
---
Для проверки целочисленности деления делаем перед эти проверку:
```java
if (value % divider != 0) {}
```
---
Код нахождения хэшфункции
```java
    public int hashFun(String value) {
        int hash = value.hashCode();
        return ((hash < 0) ? -hash : hash) % size;
    }
```
не покрывает кейс, когда value.hashCode() может вернуть значение Integer.MIN_VALUE, которое даёт false при сравнении < 0.  
Перед кодом вставляем проверку:
```java
if (hash == Integer.MIN_VALUE) { }
```
Или используем инструментарий BigInteger.

---
Во всех случаях, где нужно сравнивать или округлять вещественные числа с заданной точностью, используем BigDecimal.

---
`lond cash;` меняем на `double cash;`

---
`Report report = createReportByCode("LOAN_CODE");`  
Выносим строку в константу  
`public static final String LOAN_CODE = "LOAN_CODE";`

---
`User user = findById(UUID.fromString("5fc03087-d265-11e7-b8c6-83e29cd24f4c"));`
Неизменный uuid выносим в константу
`public static final String USER_ID = "5fc03087-d265-11e7-b8c6-83e29cd24f4c";`

---
В приложение на Java Spring сразу настраиваем Resource Bundle для добавления локализации в приложение.

---
В реализации DynamicArray в методе удаления элемнта проверку на зполненность массива выносим в в переменную с говорящим названием или в одноимённый метод
```java
boolean hasConditionToReduce = (capacity % 2 == 0 && count < capacity / 2) || 
                                (capacity % 2 != 0 && count <= capacity / 2);
```
---
Процесс выдачи займа может быть запущен, если кредитная история чиста, и сумма займов за год не превышает 50000.  
Выносим в переменную
```java
boolean allowToStartLoanProcess = isCleanLoanHistory && yearLoanTotal <= LIMIT;
```