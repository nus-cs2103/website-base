{% from "common/macros.njk" import ask_chatgpt, show_ai_guidance, show_prompt_part1, show_prompt_part2 with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-list:" inline />

### Level 2. Add, List

{% set requirements_level_2 %}
Add the ability to store whatever text is entered by the user and
display it back to the user when requested.

* There is no need to save the data to the hard disk.
* Assume there will be no more than 100 tasks. If you wish, you may use a fixed-size array (e.g., `String[100]`) to store the items.
{% endset %}
{% set sample_output_level_2 %}
```
    ...
     What can I do for you?
    ____________________________________________________________

read book
    ____________________________________________________________
     added: read book
    ____________________________________________________________

return book
    ____________________________________________________________
     added: return book
    ____________________________________________________________

list
    ____________________________________________________________
     1. read book
     2. return book
    ____________________________________________________________
bye
    ____________________________________________________________
     Bye. Hope to see you again soon!
    ____________________________________________________________

```
{% endset %}

{{ requirements_level_2 }}
<p/>
Example:
{{ sample_output_level_2 }}

{% call show_ai_guidance("Level 2. Add, List") %}
{{ show_prompt_part1(requirements_level_2, sample_output_level_2) }}
{{ show_prompt_part2() }}
{% endcall %}
