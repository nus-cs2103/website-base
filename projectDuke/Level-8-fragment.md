{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-clock:" inline />

### Level 8. Dates and Times

Teach the chatbot how to understand dates and times. For example, if the command is `deadline return book /by 2/12/2019 1800`, the chatbot should understand `2/12/2019 1800` as _2nd of December 2019, 6pm_, instead of treating it as just a String.

* **Minimal**: Store deadline dates as a `java.time.LocalDate` (or `java.time.LocalDateTime`) in your task objects. Accept dates in a format such as `yyyy-mm-dd` (e.g., `2019-10-15`)  and print in a different format such as `MMM dd yyyy` (e.g., `Oct 15 2019`).
* **Stretch goal**: Use dates and times in more meaningful ways, e.g., add a command to print deadlines/events occurring on a specific date.

<panel header="Using dates/times in Java" minimized >

A code snippet using the `LocalDate` class to deal with dates/times (you may use other approaches too):
```java
import java.time.LocalDate;
import java.time.format.DateTimeFormatter;
import java.time.temporal.ChronoUnit;

public class Main {
    public static void main(String[] args) {
        //create dates from strings
        LocalDate d1 = LocalDate.parse("2019-12-01");
        LocalDate d2 = LocalDate.parse("2019-12-02");
        LocalDate d3 = LocalDate.parse("2019-12-02");

        //compare dates
        System.out.println(d1.isBefore(d2)); // -> true
        System.out.println(d1.isAfter(d2)); // -> false
        System.out.println(d2.equals(d3)); // -> true

        //work with dates
        System.out.println(d1.getDayOfWeek()); // -> SUNDAY
        System.out.println(d1.getMonth()); // -> DECEMBER
        System.out.println(d1.plus(1, ChronoUnit.YEARS));  // -> 2020-12-01

        // get today's date and print it in a specific format
        LocalDate d4 = LocalDate.now();
        System.out.println(d4); // -> 2019-10-15
        System.out.println(d4.format(DateTimeFormatter.ofPattern("MMM d yyyy"))); // -> Oct 15 2019
    }
}
```

* [A tutorial from https://www.baeldung.com/](https://www.baeldung.com/java-8-date-time-intro)
</panel>

{% call show_ai_guidance("General: Look out for random deviations") %}

AI can do an action (such as running the tests) the first few times without any issue but run into a problem the next time. At times, wanting to be helpful, it will then try to 'fall back' on other alternatives. If you are not monitoring the AI carefully, you might not even realize that AI did something differently and what it did is not what you wanted.

If you see AI going off-track, stop and issue firmer instructions.
{% endcall %}
