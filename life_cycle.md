```java
int count = 0;

    while (slots[index] != null && count < size) {
        count++;
```
Переменной count меняем область видимости на локальную внутри цикла, т.к снаружи она не используется.

---
```java
private int height;
private int weight;
private int proportion;

        {
        Random random = new Random(17);
        height = random.nextInt(190);
        weight = random.nextInt(120);
        }
public NPCUnit() {
      //  Random random = new Random(17);
        proportion = height/weight;
        }
```
Переменную random мы вынисли в блок инициализации вместе с инициализацией 2-х переменных, т.к. внутри конструктора в ней нет необходимости.

---
```java
boolean isValid = validate();

for (int i = 0; i < slots.length && isValid; i++) { }
```
От переменной isValid мы избавляемся, и вносим вызов метода validate() в определение цикла, т.к его дальнейших вызовов не будет.

---
```java
protected JFrame frame;
```
Переделываем в private, т.к. не предполагаем, что пользователь будет расширять текущий класс.

---
```java
public EmailServise emailServise;
```
Переделываем в protected, т.к. в процессе проектирования знаем, что только потомки будут использовать переменную.

---
```java
public Random random;
```
Переносим в классы, где нужен свой Random, переделываем в private и инициализируем его одной и той же константой.

---
```java
public String currentFormat;
```
Переделываем в package, т.к. переменная используется только для обработки документов, работа с которыми локализована в одном пакете documents.

---
В том же пакете, где сосредоточена работа с документами, `String currentFormat;` разбиваем на перменные  
`private String currentCreatinFormat;`
`private String currentConvertationFormat;`
и используем лишь в классах, отвечающих за создание и конвертацию документов.

---
```java
Scanner scanner = null;
    try {
        scanner = new Scanner(new File("test.txt"));
        while (scanner.hasNext()) {
            System.out.println(scanner.nextLine());
        }
    }
```
переделываем в 
```java
    try (Scanner scanner = new Scanner(new File("test.txt"))) {
        while (scanner.hasNext()) {
            System.out.println(scanner.nextLine());
        }
    }
```
Делаем пеерменную видемой лишь на уровне блока try.