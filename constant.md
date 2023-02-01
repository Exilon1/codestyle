Калькулятор математического выражения в постфиксной записи.  
Программа во множестве мест использует символьные значения '+', '-', '*', '/'.  
Выносим их вконстанты:  
`public static final char PLUS = '+';`  
`public static final char MINUS = '-';`  
`public static final char MULTIPLY = '*';`  
`public static final char DIVIDE = '/';`

---
Реализация PowerSet. Инициализация переменных в конструкторе:
```java
private final int step;
private final String[] slots;

public PowerSet() {
        step = 11;
        slots = new String[20000];
}
```
Переносим магическое число 20000 в константу. Константу step переделывваем в STEP.

---
Реализация LinkedList с фейковыми головой и хвостом.  
Голова и хвост инициализируются единожды в конструкторе, и более не меняются в процессе выполнения.  
Имена могут быть переделаны в верхний регистр  
`private final FakeHead HEAD;`  
`private final FakeTail TAIL;`

---
Реализация хэш функции, где в какой-то момент происходит деление по модулю простого числа.  
Простое число может быть вынесено в константу.

---
Реализация динамического массива. Инициализация внутреннего массива в конструкторее:
```java
public DynArray(Class clz) {
    makeArray(16);
}
```
Избавляемся от магического числа 16.  
То же самое в методе 
```java
public void clear() {
    array = null;
    count = 0;
    makeArray(16);
}
```
---
То же самое в 
```java
private void reduceArray() {
    int newCapacity = (int) (capacity / 1.5);

    if (newCapacity < 16) {makeArray(16);
        return;
    }

    makeArray(newCapacity);
}
```
Выносим делитель capacity в константу LOAD_RATIO  

---
Ининициализация любого генератора случайных чисел.
`var random = new Random(17);`
Выносив в INITIALIZE_NUMBER.

---
Получение случайного числа в диапазоне. Границу выносим в константу BOUND.

---
При создании сокета список портов можно хранить в константах PUBLIC_PORT, ADDITIONAL_PORT...

---
В REST контроллерах неизменяемые эндпоинты можно хранить в строчных константах.

---
Для любого неизменяемого URL подойдёт константа с этим суффиксом:
CONNECTION_URL

---
Любой неизменный UUID можно хранить в константе с тем же именем.