{% from "common/macros.njk" import ask_chatgpt, show_ai_guidance with context %}

<include boilerplate src="dukeExtensionTitle.md" var-extId="A-Enums"
         var-extHeading="Use Enumerations"/>
<markdown>

Use Java `enum`s, if applicable.

{% call show_ai_guidance("A-Enums") %}

Here's useful experiment: First, look through the code and see if you can identify any variables that can be represented as an `enum`. Then, ask AI to suggest a list of `enum`s that can be used in the code.
{% endcall %}
</markdown>
