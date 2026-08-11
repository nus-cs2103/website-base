{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Checkstyle", "Use Checkstyle", "primary") }}

Use Checkstyle to detect coding style violations.

Refer to the tutorial [_Using Checkstyle_ @SE-EDU/guides](https://se-education.org/guides/tutorials/checkstyle.html) to learn how to use Checkstyle.
<p/>


{% call show_ai_guidance("A-Checkstyle") %}
Some sample prompts:

{% call mdblock() %}
**Briefly explain Checkstyle**: what it is and how it can be useful in this project.

**Do we even need it?** In this project we already use the /seedu-java-coding-standard to comply with the required coding standard. Is there any value in also using Checkstyle? Should we choose one only, and if yes, which one?
{% endcall %}

{% call mdblock() %}
**Set up Checkstyle for this project**, as explained in https://se-education.org/guides/tutorials/checkstyle.html

**Checkstyle configuration** matching [our Java coding standard](https://se-education.org/guides/conventions/java/intermediate.html) can be found in the [AddressBook Level 3 project](https://github.com/se-edu/addressbook-level3/tree/master/config/checkstyle).
{% endcall %}

{% call mdblock() %}
How do I manually run Checkstyle?
{% endcall %}

{% call mdblock() %}
Run Checkstyle and fix any violations found. Also explain the fixes you did, for my own knowledge.
{% endcall %}

{% endcall %}