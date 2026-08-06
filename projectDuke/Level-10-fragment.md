{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance with context %}




<include boilerplate src="level_thumb.md" var-text=":fas-window-maximize:" inline />

### Level 10. GUI

Add a GUI to the chatbot. Use the JavaFX technology to implement the GUI.

<br>
<br>

Refer to the [_JavaFX Tutorial_ @SE-EDU/guides](https://se-education.org/guides/tutorials/javaFx.html) to learn how to get started with JavaFX.<br>
Go through ==at least up to part 4 of the tutorial==. Part 5 covers cosmetic UI tweaks and is optional to learn.

{% call show_ai_guidance("JavaFX Tutorial") %}

You can use AI to go through the JavaFX tutorial the same way you've been doing so far in the project.

For example, after setting up the starter project given in the JavaFX tutorial in a local folder, you can start a Codex project in that folder. Next, you can use a prompt like this:

{% call mdblock() %}
See the JavaFX tutorial given at https://se-education.org/guides/tutorials/javaFxPart1.html

Implement the HelloWorld application as described in that page.
{% endcall %}

To what extent you use AI depends on to what level you want to internalize JavaFX concepts. If you don't think it will not be useful for you to know JavaFX in the future, you can go for maximum use of AI.

{{ icon_tip }} If you wish to use the `present-changes-visually` in this project as well, you can issue a prompt like this:

{% call mdblock() %}
Promote the skill present-changes-visually I created in the project `[give the project folder here]` into a system-wide skill so that I can use it from other projects.
{% endcall %}

You might have to restart Codex to make the promoted skill is available for use.

{% endcall %}

<box type="warning" seamless>

**There are two non-trivial steps** to take here:

1. learning JavaFX basics
1. creating a GUI for your chatbot

You are <span class="text-danger">cautioned against trying to do both in one go</span>. Instead, complete the JavaFX tutorial as a separate project before adding a GUI to the chatbot.

</box>

<box type="important" seamless>

#r#**Common mistake**:## Forgetting to add a separate `Launcher` class (as explained in the [JavaFX tutorial Part 1](https://se-education.org/guides/tutorials/javaFxPart1.html))  when adding the GUI to your project.
</box>

**Minimal requirement:** The GUI should be fit-for-purpose, i.e., users should be able to use the chatbot via the GUI.

{% call show_ai_guidance("Level-10") %}


{% endcall %}
