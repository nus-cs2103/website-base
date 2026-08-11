{% from "common/macros.njk" import ask_chatgpt, show_prompt_part1, show_prompt_part2, show_ai_guidance with context %}


<include boilerplate src="level_thumb.md" var-text=":fas-comments:" inline />

### Level 1. Echo

{% set requirements_level_1 %}
Update the code to echo commands entered by the user, and exit when the user types the command `bye`.
{% endset %}
{% set sample_output_level_1 %}
```
     ...

     What can I do for you?
    ____________________________________________________________

list
    ____________________________________________________________
     list
    ____________________________________________________________

blah
    ____________________________________________________________
     blah
    ____________________________________________________________

bye
    ____________________________________________________________
     Bye. Hope to see you again soon!
    ____________________________________________________________

```
{% endset %}

{{ requirements_level_1 }}
<br>
Example:
{{ sample_output_level_1 }}

* The indentations are optional.

<box type="tip" seamless>

**You are strongly encouraged to customize the chatbot**: In addition to the command/display formats, you can even customize its personality to make your chatbot unique.
</box>

{% call show_ai_guidance("Level1: Echo") %}
Start a new chat thread in the Codex project you created in Level-0.

<box type="tip" seamless>

Use one chat thread per iP increment, and rename the thread to match the increment. It makes past chat threads easier to find and, more importantly, reduces the risk of {{ ask_chatgpt("context rot", "What is 'context rot'?") }}.
</box>

{{ show_prompt_part1(requirements_level_1, sample_output_level_1) }}
{{ show_prompt_part2() }}

{% endcall %}
