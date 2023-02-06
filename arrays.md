Во всех случаях, когда нужно итерироваться по всем элементам массива без дополнительных условий, вместо
```java
for (int i = 0; i < slots.length && isValid; i++) { }
// в случаях, когда нет дополнительного условия isValid
```
используем  
```java
for (String val: slots)...
for (User user: userList)...
        ...
```
---
Для структур данных Collection, если не предполагается применение операторов continue и break, используем
```java
userList.forEach(this::markAsAdult);
```
---
То же самое через Stream api. 
```java
userList.stream().forEach(this::markAsAdult);
```
где можно отфильтровать пользователей
```java
userList.stream().filter(this::bySomeCriteria).forEach(this::markAsAdult);
```
или перевести коллекцию в другой тип.
```java
userList.stream().map(User::getId).collect(Collectors.toList());
```
Можно генерировать последовательности  
```java
Stream<Integer> streamIterated = Stream.iterate(40, n -> n + 2).limit(20);
```
---
Также у Collection можно взять iterator и использовать в цикле
```java
while(iterator.hasNext()) {
    iterator.next();
        ...
}
```