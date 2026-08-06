{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-CodingStandard", "Tweak the code to comply with a coding standard", "primary") }}

Tweak the code to comply with a given coding standard. From this point onward, ensure any new code added is compliant with the given coding standard.

<box type="tip" seamless>

SE-EDU guides on configuring the code style in IDEs: [Intellij IDEA](https://se-education.org/guides/tutorials/intellijCodeStyle.html) | [VS Code](https://se-education.org/guides/tutorials/vscCodeStyle.html)
</box>


{% call show_ai_guidance("A-CodingStandard") %}

As you need to follow the Java coding standard for future code, you can turn it into a reusable skill.
{% call mdblock() %}

Create a project-specific skill named seedu-java-coding-standard based on rules given in https://se-education.org/guides/conventions/java/intermediate.html

Update your agent files to mandate following this for all code in this project.

Update the current code to follow it, where necessary.

Show me the changes using the /present-changes-visually skill.
{% endcall %}
Same goes for the Git commit message standard:
{% call mdblock() %}
Create a project-specific skill named seedu-git-standard based on rules given in https://se-education.org/guides/conventions/git.html

Update your agent files to mandate following this for all future commits.
{% endcall %}
Next, you can do the following to check if the Git standard is followed correctly.
{% call mdblock() %}
Propose a commit message for the  uncommitted Java code changes.
{% endcall %}
If everything seems OK, you can proceed with the commits. If not, ask AI to update the skill where you see it is not following the standard.
{% call mdblock() %}
Create one commit for the Java code changes, and one commit for each standalone change to agent files.
{% endcall %}

{% endcall %}
