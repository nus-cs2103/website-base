{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-save:" inline />

### Level 7. Save

{% set requirements_level_7 %}
Save the tasks on the hard disk automatically whenever the task list changes. Load the data from the hard disk when the chatbot starts up. You may hard-code the file name and relative path from the project root, %%e.g., `./data/duke.txt`%%

The format of the file is up to you. Example:
```{.no-line-numbers}
T | 1 | read book
D | 0 | return book | June 6th
E | 0 | project meeting | Aug 6th 2-4pm
T | 1 | join sports club
```
{% endset %}

{{ requirements_level_7 }}

<box type="tip" seamless>

**If you use file paths in your code,**
* remember to use relative paths rather than absolute paths such as `C:\data`. If not, your app can cause unpredictable results when used on another computer.
* remember to [specify file paths in an OS-independent way](https://www.sghill.net/how-do-i-make-cross-platform-file-paths-in-java.html). If not, your app might not work when used on a different OS.
</box>

<box type="important" seamless>

**Your code must <tooltip content="i.e., if the file is missing, your code must create it">handle</tooltip> the case where the data file doesn't exist at the start.** Reason: when someone else takes your chatbot and runs it for the first time, the required file will not exist on their computer. Similarly, if you expect the data file to be in a specific folder (e.g., `./data/`), you must also handle the folder-does-not-exist-yet case.
</box>

**Stretch goal**: Handle the situation of the data file being corrupted (i.e., content not in the expected format).

{% call show_ai_guidance("Level 7. Save") %}

One possible way to break this increment into small steps is:

1. Implement writing to the file. Ask for a minimal implementation for the <tooltip content="the execution path that doesn't encounter any error conditions">'happy path'</tooltip> only.
1. Implement reading from the file. Happy path only.
1. Add error handling.
1. Ask to check if the two notes given (the one about the file path and the one about the file not existing) are covered.

If you are confident that you know how to implement this increment yourself, you can ask for a more complete implementation in one go.

Here are the sample prompts for the first incremental approach.

{% call mdblock() %}
Here is the requirement:

{{ req_start }}{{ requirements_level_7 }}{{ req_end }}

For now, do a minimal implementation of the "happy path" for writing to the file. Reading from the file can be implemented later.
Update tests and run /test-ui. At the end, run /present-changes-visually
{% endcall %}

{% call mdblock() %}
Proceed to implementing the reading from the file, similar to the previous round.
{% endcall %}

{% call mdblock() %}
In this round, enhance the code to handle all edge cases and possible errors.
{% endcall %}

{% call mdblock() %}
Here are two additional requirements. Ensure the code meets them too.

...

{% endcall %}

{% endcall %}

{% call show_ai_guidance("General: Compact to prevent context rot") %}

AI tools can show how much of the context window the current chat thread has used. In Codex, simply typing `/` in the chat box when it is empty will pop up details about the ongoing chat, including a line named `Compact` stating the status of the context window.

It is said that the AI will start getting 'dumber' once you go past 30-40% of the context window. If that happens to you, you can use the /compact command to compact the context.

{{ ask_chatgpt("More about compacting context", "Tell me more about the context window and compacting it (what, how). When should I manually compact?") }}

{% endcall %}
