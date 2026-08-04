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

{% call show_ai_guidance("Level 5. Handle Errors") %}

As before, you can proceed in small steps. Ensure AI runs the `test-ui` skill after each code update.
{% endcall %}

{% call show_ai_guidance("General: Keep updating AI files") %}

As the project progresses, observe where AI falters or overlooks things, and update the AI files accordingly.

For example, you can force AI to improve the quality of testing with a prompt like this:
```{heading="sample prompt"}
Add more test cases to cover edge cases and incorrect inputs.
Interleave positive and negative test cases to detect incorrect inputs affecting the correctness of the internal states.
```
Then, you can introduce temporary bugs into the code and see if the `test-ui` skill can detect them. If it cannot, you can ask AI to improve the skill to cover such cases.

**{{ icon_tip }} Get AI to review tests:**
* You can also ask different Codex models to review the `ui-test-plan.md` and suggest ways to improve it. Something overlooked by one model can be detected by another.
* This is also a good place to use more powerful models. Crafting good test cases has long-term benefits, and is worth the extra token cost.
* You can go one step further and get other AI tools (Claude, Gemini, etc.) to review the test cases file too.

{% endcall %}


