{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance with context %}

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

{% call show_ai_guidance("Level 9. Find") %}

As this increment is fairly straightforward, breaking it into smaller steps might not have much learning value. You can try to 'one shot' it: give the AI all the information up front and ask it to complete the increment entirely, including committing, tagging, and pushing. If the AI misses some parts of the expected work, you can learn from that and try to be more comprehensive the next time you attempt it.
{% endcall %}
