{% from "common/macros.njk" import ask_chatgpt, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Enums", "Use enumerations", "primary") }}

Use Java `enum`s, if applicable.

{% call show_ai_guidance("A-Enums") %}

Here's a useful experiment: First, look through the code and see if you can identify any variables that can be represented as an `enum`. Then, ask AI to suggest a list of `enum`s that can be used in the code.
{% endcall %}
