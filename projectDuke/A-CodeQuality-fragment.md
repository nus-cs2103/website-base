{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-CodeQuality", "Improve code quality", "primary") }}


Critically examine the code and refactor to improve the code quality where necessary.

{{ icon_important_big_red }} When adding this increment, follow closely the 'Code Quality' topics you have learned so far, rather than merely follow your own intuition about code quality.

{% call show_ai_guidance("A-CodeQuality") %}

<tabs>
  <tab header="Sample prompt (less autonomy to AI)">
{% call mdblock() %}
Let's improve the code quality iteratively, one stand-alone refactoring at a time.

First, refer to code quality guidelines in {{ url_course_website }}/se-book-adapted/chapters/codeQuality.html

Review the code against the above guidelines, identify the single highest-priority issue, and fix it. Commit the changes with a commit message that includes a detailed body explaining the rationale behind the update.
{% endcall %}

{{ icon_tip }} If you don't agree with the refactoring, ask AI to amend it or discard it.

{% call mdblock() %}
Move to the next iteration.
{% endcall %}
  </tab>
  <tab header="Sample prompt (more autonomy to the AI)">
{% call mdblock() %}
Refer to code quality guidelines in {{ url_course_website }}/se-book-adapted/chapters/codeQuality.html

If any of the current code needs to be improved based on the guidelines in there, go ahead and do it. One commit per change. The commit message body should explain the rationale for the change.
{% endcall %}

{{ icon_tip }} If you don't agree with any of the refactorings, ask AI to amend/discard them.
</tab>
</tabs>

{% endcall %}
