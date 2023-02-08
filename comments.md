3.1.  
```java
// Проверяет, можно ли использовать расширение для данного типа файла
boolean allowFileExtension(FileDescriptor file) {}
```
---
```java
class StringUtils {
    // true, если null и пустая строка после удаления пробелов 
    boolean isBlank(String str) { }
}
```
---
```java
// Устраняет проблему нахождения абсолютного значения числа, если оно равно Integer.MIN_VALUE
if (iter == Integer.MIN_VALUE) {
    return Integer.MAX_VALUE % filter_len;
}

return Math.abs(iter) % filter_len;
```
---
```java
public int find(String value) {
    int index = hashFun(value);

    try {
        // Т.к. операция удаления отсутствует, реагируем сразу на незянятый слот
        if (slots[index] == null) {
        return -1;
        }
        ...
```
---
```java
// Проверка необходима для ноды, а не не для хранимого значения
private boolean checkTheNodeIsContainedInList(Node node) {
    Node current =  head;
    while (current != null) {
        ...
    }
```
---
```java
// Используется только в качестве неизменных головы и хвоста LinkedList
abstract class FakeNode extends Node2 {}
```
---
```java
// Итерируем, пока не пробежим по всем ячейкам, или пока не наткнёмся на пустую ячейку
for (int i = 0; i < slots.length && slots[index] != null; i++) {}
```

3.2.  
Не было