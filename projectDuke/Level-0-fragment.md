{% from "common/admin.njk" import show_ai_guidance with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-grin-hearts:" inline />

### Level 0. Rename, Greet, Exit

**++(a) Give your chatbot a new name++**, to differentiate it from the placeholder name `Duke`.<br>
* **Avoid these common choices** as well: `Chatty`, `Jarvis`, `ChatBot`, `Chad`
* Rename `Duke.java` to match the chatbot name you selected, and remove all traces of `Duke` from the code.

{% call show_ai_guidance("Renaming the chatbot") %}

1. Tweak the `AGENTS.md` file in the project root, and commit it.
   <box type="info" seamless>

   Information in the `AGENTS.md` is read by AI agents and are included as part of the context.<br>
   In this specific case, things you can tweak:

   * Fill in the parts marked as `[to be filled]`
   * If using a Mac, ensure the instructions about switching to the correct Java version matches your Java set up.
   </box>
1. Start a new chat/project in Codex (i.e., ChatGPT app in Codex mode). Set your iP folder as the folder of that chat.<br>
   Refer to the tutorial [_Using the Codex Desktop App_ at SE-EDU Guides](https://se-education.org/guides/tutorials/codexDesktop.html) for more info.
1. Try the following prompt.
   ```
   I wish to change the chatbot name from duke to [NEW NAME].
   **Which files** need to be changed in what way?
   ```
 1. If you are happy with reply, you can follow up with a `Go ahead and make those changes`.<br>
    <box type="tip" seamless>

    Recommended: Start with a cheaper model (e.g., `Luna` at `High` or `Extra High` setting). Use more expensive models only when cheaper ones fail to meet expectations or you think the task is worth a higher cost of tokens.
    </box>
 1. If Codex doesn't update the banner, you can ask it to do so.
    ```{ heading="sample prompt"}
    Generate an ASCII-art banner for the word [NEW NAME] (case-sensitive).
    Give me a few variations.
    ```
 1. Examine and test the updated code. If you are happy with it, commit the changes. %%Yes, you can ask Codex to create the commit but if you are new to Git, it is better to do the commits yourself before you start delegating it to AI. Besides, hand-committing can even be faster, and saves tokens.%%

{% endcall %}

**++(b) Update the initial code simply greet the user and exit.++**
<br>

{% set sample_output_greet_and_exit %}
```
____________________________________________________________
[CHATBOT BANNER]
Hello! I'm [CHATBOT NAME].
What can I do for you?
____________________________________________________________
Bye. Hope to see you again soon!
____________________________________________________________
```
{% endset %}
Example:
{{ sample_output_greet_and_exit }}
* Horizontal lines are optional. So is the banner.
* Change the wording to match the personality you wish to give your chatbot. The above is an example only.

{% call show_ai_guidance("Updating the initial code") %}

This change is simple enough that you can easily do it by hand. Doing it using AI can help you get used to working with the AI without losing much value on the hand-coding front (i.e., a way of taking 'baby steps'). Here are two sample prompts:

````{ heading="sample prompt"}
The requirement given to me:

Update the code to simply greet the user and exit. Here is an example output:

{{ sample_output_greet_and_exit | trim }}

I have updated the code accordingly. Review my changes and suggest possible issues and areas to improve.
````

````{ heading="sample prompt"}
Update the code to simply greet the user and exit. Here is an example output:

{{ sample_output_greet_and_exit | trim }}
````

{% endcall %}

