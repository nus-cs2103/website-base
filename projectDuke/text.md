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
* **Levels**: A series of features, meant to be added to Duke in the given order, although some can be skipped. These have been named `Level 0` to `Level 10` to indicate how each makes the product progressively "level up".
* **Extensions:**
  * ++<span class="badge rounded-pill bg-primary">Category A</span>++ These are internal/feature enhancements meant to help you practice a specific Java or an SE technique.
  * ++<span class="badge rounded-pill bg-info">Category B</span>++ These are enhancements related to task tracking.
  * ++<span class="badge rounded-pill bg-success">Category C</span>++ These are enhancements, not specifically related to task tracking.
  * ++<span class="badge rounded-pill bg-danger">Category D</span>++ Each of these adds the ability to track another type of entity.
</div>
</div>

## <span class="text-white bg-dark p-1">Levels</span>

{% for level in [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10] %}
<div id="Level-{{ level }}">
<include src="Level-{{ level }}-fragment.md" />
</div><hr>
{% endfor %}

<p/>

<include src="extensions-fragment.md" />

</div>
