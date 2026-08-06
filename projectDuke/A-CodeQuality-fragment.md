{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-CodeQuality", "Improve code quality", "primary") }}


Critically examine the code and refactor to improve the code quality where necessary.

{{ icon_important_big_red }} When adding this increment, follow closely the 'Code Quality' topics you have learned so far, rather than merely follow your own intuition about code quality.

{% call show_ai_guidance("A-CodeQuality") %}

<tabs>
  <tab header="Sample prompt (less AI)">
{% call mdblock() %}
{% endcall %}
  </tab>
  <tab header="Sample prompt (more AI)">
{% call mdblock() %}
{% endcall %}
</tab>
</tabs>

{% endcall %}
