{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_example, show_prompt_part1, show_prompt_part2 with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-business-time:" inline />

### Level 4. ToDos, Events, Deadlines

Add support for tracking three types of tasks:
<br>
<br>

1. **ToDos**: tasks without any date/time attached to them %%e.g., _visit new theme park_%%
2. **Deadlines**: tasks that need to be done before a specific date/time %%e.g., _submit report by 11/10/2019 5pm_%%
3. **Events**: tasks that start at a specific date/time and end at a specific date/time<br>
   %%e.g., (a) _team project meeting 2/10/2019 2-4pm_ (b) _orientation week  4/10/2019 to 11/10/2019_%%

Example:
```{.no-line-numbers}
todo borrow book
    ____________________________________________________________
     Got it. I've added this task:
       [T][ ] borrow book
     Now you have 5 tasks in the list.
    ____________________________________________________________

list
    ____________________________________________________________
     Here are the tasks in your list:
     1.[T][X] read book
     2.[D][ ] return book (by: June 6th)
     3.[E][ ] project meeting (from: Aug 6th 2pm to: 4pm)
     4.[T][X] join sports club
     5.[T][ ] borrow book
    ____________________________________________________________

deadline return book /by Sunday
    ____________________________________________________________
     Got it. I've added this task:
       [D][ ] return book (by: Sunday)
     Now you have 6 tasks in the list.
    ____________________________________________________________

event project meeting /from Mon 2pm /to 4pm
    ____________________________________________________________
     Got it. I've added this task:
       [E][ ] project meeting (from: Mon 2pm to: 4pm)
     Now you have 7 tasks in the list.
    ____________________________________________________________
```

At this point, dates/times can be treated as strings; there is no need to convert them to actual dates/times.

Example:
```{.no-line-numbers}

deadline do homework /by no idea :-p
    ____________________________________________________________
     Got it. I've added this task:
       [D][ ] do homework (by: no idea :-p)
     Now you have 6 tasks in the list.
    ____________________________________________________________
```

<include boilerplate src="dukeNestedFragment.md" var-target="A-Inheritance" var-name="Extension: `A-Inheritance`" />

{% call show_ai_guidance("Level 4. ToDos, Events, Deadlines") %}

As before, you can proceed in small steps, for example, first adding the feature without using inheritance and then adding the extension `A-Inheritance`.
Commit after each step, and tag after completing each increment.
{% endcall %}

{% call show_ai_guidance("General: Get AI to check its work") %}

Recent AI coding harnesses already do some checking of their own work. However, it is in our interest to step in and strengthen these guard rails. In addition, do some manual testing of your own.

**Create a `test-ui` skill** that you (and Codex) can use to test the code. Here's a sample prompt:

{% call mdblock() %}

Create a project-specific skill named `test-ui`, as follows.
* The skill should run the program and test it with a set of commands, and check if the output matches the expected output.
* The skill should take as input a list of commands and a list of expected outputs, and run the program with each command, checking if the output matches the expected output.
* The list of test cases (and other relevant information) should be recorded in `test/ui-test-plan.md` file.
* Each test case should specify the aim of the test case, inputs, and the expected output.
* After testing, show a record of console inputs/outputs, so that we can see what the test session looked like.
* If a test case failed, terminate the test session immediately, and report the actual and expected outputs.
{% endcall %}

After the skill is created, invoke it. If the behavior is not to your satisfaction, you can ask the AI to improve the skill.

To ensure the skill is used after each code update, you can issue a prompt such as the following:

{% call mdblock() %}
Update relevant agent files to ensure that after each code update,
1. the `test/ui-test-plan.md` is updated (if needed), and,
2. the `test-ui` skill is invoked.
{% endcall %}

It is likely this will result in an update to the `AGENTS.md` file.

Commit the changes to the Codex files.
{% endcall %}


