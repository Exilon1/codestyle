3.1.
```java
class Button {
    
    public static final String DESKTOP_WINDOWS_BUTTON = "dwb";
    public static final String DESKTOP_MACOS_BUTTON = "dmb";
    public static final String WEB_HTML_BUTTON = "whb";
    
    private Component parentComponent;
    private String type;
    
    private Button(Component parent) {
        this(parent, WEB_HTML_BUTTON);
    }

    private Button(Component parentComponent, String buttonType) {
        this.parentComponent = parentComponent;
        type = buttonType;
    }
    
    public static Button htmlButtonByParentComponent(Component parentComponent) {
        return new Button(parentComponent);
    }

    public static Button windowsButtonByParentComponent(Component parentComponent) {
        return new Button(parentComponent, DESKTOP_WINDOWS_BUTTON);
    }

    public static Button macOSButtonByParentComponent(Component parentComponent) {
        return new Button(parentComponent, DESKTOP_MACOS_BUTTON);
    }
}
```

3.2.  
interface Operation
abstract class AbstractWindow

Именование интерфейса идентично именованию классов.  
К имени абстрактного класса добавляется префикс Abstract.