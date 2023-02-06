```java
int minimalAge = Integer.MAX_VALUE;

for (User user: userList) {
    if (minimalAge > user.getAge()) {
        minimalAge = user.getAge();
    }
}
```
`minimalAge` связывается при написании кода. Это необходимо, потому что переменная является аккумулятором ислужит для нахождения минимального возраста.

---
```java
private static final int PORT = 8080;
private static final int ADDITIONAL_PORT = 8081;

Connection createConnection() {
    int validPort = PORT;
    
    if (isValid(validPort)) {
        log.add("Connected by port $S", validPort);
        return connect(validPort);
    }

    validPort = ADDITIONAL_PORT;
    log.add("Connected by additional port $S", validPort);
        
    return connect(validPort);
}
```
Инициализируем validPort на этапе компиляции, т.к. переменная должна быть инициализирована перед её непосредственным использованием.  
Переменная используется во многих местах метода и не может быть заменена на константу.

---
```java
class MainWindow {
    private final UUID userId = UUID.fromString("5fc03087-d265-11e7-b8c6-83e29cd24f4c");
    private User user;
    public EntityManager entityManager;
    
    void onAuthorizeListener() {
        user = entityManager.getUserById(userId);
        ...
    }
}
```
Метод-лиснер подписан на событие авторизации пользователя в текущем окне.
`entityManager.getUserById(userId);` делает запрос в базу данных. Это пример ленивой инициализации, когда дефолтный юзер необходим в коде программы не в момент инициализации окна, а на этапе авторизации некого иного пользователя.