<span id="title">Project Duke</span>

<div id="body">
<div id="intro">


<div class="lead">

<pic eager add-class="float-start border me-2 mt-2 p1 bg-white" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5d/Duke_%28Java_mascot%29_waving.svg/250px-Duke_%28Java_mascot%29_waving.svg.png?_=20071215164642" width="60">

<small><small>**Duke**, the Java Mascot<br><small>[[credit: Wikipedia](https://en.wikipedia.org/wiki/File:Duke_(Java_mascot)_waving.svg)]</small></small>
</pic>

**Project Duke is an educational software project designed to take you through the steps of building a small software _incrementally_**, while applying as many Java and SE techniques as possible along the way.
</div>

**The project aims to build a product named _Duke_, a Personal Assistant Chatbot that helps a person to keep track of various things.** %%The name _Duke_ was chosen as a placeholder name, in honor of [Duke, the Java Mascot](https://www.oracle.com/java/duke.html).%%

Here is a sample interaction with Duke:
```{.no-line-numbers}
    ____________________________________________________________
      ____        _
     |  _ \ _   _| | _____
     | | | | | | | |/ / _ \
     | |_| | |_| |   <  __/
     |____/ \__,_|_|\_\___|

     Hello! I'm Duke
     What can I do for you?
    ____________________________________________________________

list
    ____________________________________________________________
     Here are the tasks in your list:
     1.[T][X] read book
     2.[D][ ] return book (by: June 6th)
     3.[E][ ] project meeting (from: Aug 6th 2pm to: 4pm)
     4.[T][X] join sports club
    ____________________________________________________________

todo borrow book
    ____________________________________________________________
     Got it. I've added this task:
       [T][ ] borrow book
     Now you have 5 tasks in the list.
    ____________________________________________________________


deadline return book /by Sunday
    ____________________________________________________________
     Got it. I've added this task:
       [D][ ] return book (by: Sunday)
     Now you have 6 tasks in the list.
    ____________________________________________________________

mark 2
    ____________________________________________________________
     Nice! I've marked this task as done:
       [D][X] return book (by: June 6th)
    ____________________________________________________________

blah
    ____________________________________________________________
     OOPS!!! I'm sorry, but I don't know what that means :-(
    ____________________________________________________________

bye
    ____________________________________________________________
     Bye. Hope to see you again soon!
    ____________________________________________________________

```

{{ icon_tip }} **You are ==encouraged to give your chatbot another name (and a different personality if you wish)==**, to differentiate yours from others'. In the case of the latter, please do not use slang/words that some others in the class might not know, and also avoid offensive language.

<div id="increments_summary">

The project consists of the following _increments_:
* **Levels**: A series of features, meant to be added to Duke in the given order, although some can be skipped. These have been named `Level 1` to `Level 10` to indicate how each makes the product progressively "level up".
* **Extensions:**
  * ++<span class="badge rounded-pill bg-primary">Category A</span>++ These are internal/feature enhancements meant to help you practice a specific Java or an SE technique.
  * ++<span class="badge rounded-pill bg-info">Category B</span>++ These are enhancements related to task tracking.
  * ++<span class="badge rounded-pill bg-success">Category C</span>++ These are enhancements, not specifically related to task tracking.
  * ++<span class="badge rounded-pill bg-danger">Category D</span>++ Each of these adds the ability to track another type of entities.
</div>
</div>

## <div class="text-white bg-dark p-1">Levels</div>
<div id="Level-0">
<include src="Level-0-fragment.md" />
</div><hr>
<div id="Level-1">
<include src="Level-1-fragment.md" />
</div><hr>
<div id="Level-2">
<include src="Level-2-fragment.md" />
</div><hr>
<div id="Level-3">
<include src="Level-3-fragment.md" />
</div><hr>
<div id="Level-4">
<include src="Level-4-fragment.md" />
</div><hr>
<div id="Level-5">
<include src="Level-5-fragment.md" />
</div><hr>
<div id="Level-6">
<include src="Level-6-fragment.md" />
</div><hr>
<!-- ================================================================================================ -->
<div id="Level-7">

<include boilerplate src="level_thumb.md" var-text=":fas-save:" inline />

### Level 7. Save

Save the tasks on the hard disk automatically whenever the task list changes. Load the data from the hard disk when the chatbot starts up. You may hard-code the file name and relative path from the project root %%e.g., `./data/duke.txt`%%

The format of the file is up to you. Example:
```{.no-line-numbers}
T | 1 | read book
D | 0 | return book | June 6th
E | 0 | project meeting | Aug 6th 2-4pm
T | 1 | join sports club
```

<box type="tip" seamless>

**If you use file paths in your code,**
* remember to use relative paths rather than absolute paths such as `C:\data`. If not, your app can cause unpredictable results when used on another computer.
* remember to [specify file paths in an OS-independent way](https://www.sghill.net/how-do-i-make-cross-platform-file-paths-in-java.html). If not, your app might not work when used on a different OS.
</box>

<box type="important" seamless>

**Your code must <tooltip content="i.e., if the file is missing, your code must create it">handle</tooltip> the case where the data file doesn't exist at the start.** Reason: when someone else takes your chatbot and runs it for the first time, the required file will not exist on their computer. Similarly, if you expect the data file to be in a specific folder (e.g., `./data/`), you must also handle the folder-does-not-exist-yet case.
</box>

**Stretch goal**: Handle the situation of the data file being corrupted (i.e., content not in the expected format).

</div><hr><!-- ================================================================================================ -->
<div id="Level-8">

<include boilerplate src="level_thumb.md" var-text=":fas-clock:" inline />

### Level 8. Dates and Times

Teach the chatbot how to understand dates and times. For example, if the command is `deadline return book /by 2/12/2019 1800`, the chatbot should understand `2/12/2019 1800` as _2nd of December 2019, 6pm_, instead of treating it as just a String.

* **Minimal**: Store deadline dates as a `java.time.LocalDate` (or `java.time.LocalDateTime`) in your task objects. Accept dates in a format such as `yyyy-mm-dd` (e.g., `2019-10-15`)  and print in a different format such as `MMM dd yyyy` (e.g., `Oct 15 2019`).
* **Stretch goal**: Use dates and times in more meaningful ways e.g., add a command to print deadlines/events occurring on a specific date.

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

</div><hr><!-- ================================================================================================ -->
<div id="Level-9">

<include boilerplate src="level_thumb.md" var-text=":fas-search:" inline />

### Level 9. Find

Give users a way to find a task by searching for a keyword in the task description.
<br>
<br>

Example:
```{.no-line-numbers}
find book
    ____________________________________________________________
     Here are the matching tasks in your list:
     1.[T][X] read book
     2.[D][X] return book (by: June 6th)
    ____________________________________________________________
```

</div><hr><!-- ================================================================================================ -->
<div id="Level-10">

<include boilerplate src="level_thumb.md" var-text=":fas-window-maximize:" inline />

### Level 10. GUI

Add a GUI to the chatbot. Use the JavaFX technology to implement the GUI.

<br>
<br>

Refer to the [_JavaFX tutorial_ @SE-EDU/guides](https://se-education.org/guides/tutorials/javaFx.html) to learn how to get started with JavaFX.<br>
Go through ==at least up to part 4 of the tutorial==. Part 5 covers cosmetic UI tweaks and is optional to learn.

<box type="warning" seamless>

**There are two non-trivial steps** to take here:

1. learning JavaFX basics
1. creating a GUI for your chatbot

You are <span class="text-danger">cautioned against trying to do both in one go</span>. Instead, complete the JavaFX tutorial as a separate project before adding a GUI to the chatbot.

</box>

<box type="important" seamless>

#r#**Common mistake**:## Forgetting to add a separate `Launcher` class (as explained in the [JavaFX tutorial Part 1](https://se-education.org/guides/tutorials/javaFxPart1.html))  when adding the GUI to your project.
</box>

**Minimal requirement:** The GUI should be fit-for-purpose, i.e., users should be able to use the chatbot via the GUI.

</div>

<p/>

<include src="extensions-fragment.md" />


</div>
