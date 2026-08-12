{% from "common/macros.njk" import ask_chatgpt, show_ai_guidance with context %}


<include boilerplate src="level_thumb.md" var-text=":fas-trash-alt:" inline />

### Level 6. Delete

Add support for deleting tasks from the list.
<br>
<br>

Example:
```{.no-line-numbers}
list
    ____________________________________________________________
     Here are the tasks in your list:
     1.[T][X] read book
     2.[D][X] return book (by: June 6th)
     3.[E][ ] project meeting (from: Aug 6th 2pm to: 4pm)
     4.[T][X] join sports club
     5.[T][ ] borrow book
    ____________________________________________________________

delete 3
    ____________________________________________________________
     Noted. I've removed this task:
       [E][ ] project meeting (from: Aug 6th 2pm to: 4pm)
     Now you have 4 tasks in the list.
    ____________________________________________________________
```

<include boilerplate src="dukeNestedFragment.md" var-target="A-Collections" var-name="Extension: `A-Collections`" />

{% call show_ai_guidance("General: Get AI to review tests") %}

* You can also ask different Codex models to review the `ui-test-plan.md` and suggest ways to improve it. Something overlooked by one model can be detected by another.
* This is also a good place to use more powerful models. Crafting good test cases has long-term benefits, and is worth the extra token cost.
* You can go one step further and get other AI tools (Claude, Gemini, etc.) to review the test cases file too.

{% endcall %}
