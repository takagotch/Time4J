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
    System.out.println(nextWednesday);
    
    PlainTimestamp currentLocalTimestamp = SystemClock.inZonalView(EUROPE.BERLIN).now();
    PlainTime roundedTime =
        curentLocalTimestamp.getWallTime()
        .with(MINUTE_OF_HOUR.atFloor())
        .with(MINUTE_OF_HOUR.roundedDown(5));
    System.out.println("Rounded wall time: " + roundedTime);
    
    PlainTime eveningTime = PlainTime.of(20, 45);
    ChronoFormatter<PlainTime> formatter = 
        ChronoFormatter.ofTimePattern("h:mm B", PatternType.CLDR, Locale.ENGLISH);
    System.out.println(
        ChronoFormatter.ofTimePattern("h:mm B", PatternType.CLDR, Locale.ENGLISH);
    System.out.println(
        "12-hour-format with dayperiod: "
        + formatter.format(eveningTime));
        
    Moment leapsecondUTC =
        PlainDate.of(2012, Month.JUNE, 30)
        .at(PlainTime.midnightAtEndOfDay())
        .atUTC(.minus(1, SI.SECONDS);
    System.out.println(leapsecondUTC);
    
    System.out.println(
        "Japan-Time: "
        + ChronoFormatter.ofMomentPattern(
          "uuuu-MM-dd'T'HH:mm:ssXX",
          PatternType.CLDR,
          Locale.ROOT,
          ASIA.TOKYO
        ).format(leapsecondUTC)
    );
    
    Duration<ClockUnit> dur = Duration.of(337540, ClockUnit.SECONDS).with(Duration.STD_CLOCK_PERIOD);
    
    String s1 = Duration.Formatter.ofPattern(ClockUnit.class, "hh:mm:ss").format(dur);
    System.out.println(s1);
    
    String s2 = PrettyTime.of(Locale.FRANCE).print(dur, TextWidth.WIDE);
    System.out.println(s2);
    
    CHronoFormatter<LocalDate> formatter2 = 
      ChronoFormatter.setUp(PlainDate.threeten(), new Locale("en", "SE"))
        .addPattern("GGGG yyyy, MMMM ", PatternType.CLDR)
        .addEnglishOrdinal(ChronoHistory.ofSweden().dayOfMonth())
        .build();
    System.out.println(formatter2.format(LocalDate.of(1712, 3, 11)));
  }
}

TZDATA.init();
```

```
```

```
```


