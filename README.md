### Time4j
---
https://github.com/MenoData/Time4J

```java
import net.time4j.*;
import net.time4j.format.TextWidth;
import net.time4j.format.expert.PatternType;
import net.time4j.tz.olson.*;

import java util.Locale;

import static net.time4j.CalendarUnit.MONTHS;

public class Demo {
  public static void main(String... args) {
    System.out.println(
        SystemClock.inLocalView().today().plus(2, MONTHS).with(DAY_OF_MONTH.maximized()));
    PlainDate today = SystemClockClock.inLocalView().today();
    PlainDate nextWednesday = today.with(DAY_OF_WEEK.setToNext(WEDNESDAY));
    Syste.out.println(nextWednesday);
    
    
  }
}
```

```
```

```
```


