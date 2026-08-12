{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Assertions", "Use assertions", "primary") }}

Use the `assert` feature (not JUnit assertions) to document important assumptions that should hold at various points in the code.

{% call show_ai_guidance("Use Assertions") %}
Sample prompt:

{% call mdblock() %}
Use the Java assert feature to document important assumptions that should hold at various points in the code.

Justify each case.
{% endcall %}

{% endcall %}