```java
// Находит целые числа в строке
Pattern integerPattern = Pattern.compile("\\d+");
Matcher matcher = integerPattern.matcher(expression);
```
Добаавлен комментарий согласно пункту 1.

---
```java
// Возвращает singleton объект UserService
UserService createOnlyServiceImlementation() {}
```
Добаавлен комментарий согласно пункту 1.

---
```java
@Test
void removeTest() {
    // Мы пытаемся выявить ошибки, возникающие только на больших наборах значений
    for (int i = 0; i < 10000; i++) {
        powerSet.put(String.valueOf(i));
    }
```
Добаавлен комментарий согласно пункту 2.

---
```java
@Test
void removeTest() {
    // Пытаемся вызвать N+1 проблему
    List<PostComment> comments = entityManager
        .createQuery("""
            select pc
            from PostComment pc
            """, PostComment.class)
        .getResultList();
```
Добаавлен комментарий согласно пункту 2.

---
```java
public class ExceptionEventLogHandler {
    /**
     * @param thrownException эксепшн, перехваченный в процессе работы
     * @param uiComponent компонент, который будет связан с эксепшном в логе
     */
    @Override
    public boolean handle(Throwable thrownException, UIComponent uiComponent) { }
}
```
Добаавлен комментарий согласно пункту 3.

---
```java
public class FileManager<V> {
    /**
     * @return потомок типа File, которым проинициализирован файл менеджер
     */
    public V createFile() { }
}
```
Добаавлен комментарий согласно пункту 3.

---
```java
// Только для случая неудачного подключения к основному порту
public static final int ADDITIONAL_PORT = 8086;
```
Добаавлен комментарий согласно пункту 4.

---
```java
// Можем получить StackOverflow, если FetchPlan содержит циклическую цепочку ссылок
public List<Task> selectTasks(UUID satrTaskId, FetchPlan fetchPlan) { }
```
Добаавлен комментарий согласно пункту 4.

---
```java
// Находим всех от 18 лет и старше и делаем пометку. Конечный список важен для дальнейшего использования
List<User> users = userList.stream().filter(this::isEghteenAgeOrMore).forEach(this::markAsAdult).collect(Collectors.toList());
```
Добаавлен комментарий согласно пункту 5.

---
```java
// Помещаем в Set, т.к. необходим список без дубликатов
Set<User> users = userList.stream().filter(this::isEghteenAgeOrMore).collect(Collectors.toSet());
```
Добаавлен комментарий согласно пункту 5.

---
```java
// TODO - Ждём обновления библиотеки по работе с ssh
```
Добаавлен комментарий согласно пункту 6.

---
```java
// TODO - Имплементация обращения к фаловому хранилищу произойдёт после настройли соответствующего контейнера
```
Добаавлен комментарий согласно пункту 6.