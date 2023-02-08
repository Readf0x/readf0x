```java
int day = 1;
boolean caffeine = false;
switch(day) {
    case 1:
        System.out.println("Sunday");
        break;
    case 7:
        System.out.println("Saturday");
        break;
    default:
        if(caffeine) {
            System.out.println("Looking forward to the weekend!");
        } else {
            System.out.println("I'm going to kill myself");
        }
}

```
