{% from "common/macros.njk" import mdblock, show_ai_guidance with context %}


<include boilerplate src="level_thumb.md" var-text=":fas-grin-hearts:" inline />

### Level 0. Rename, Greet, Exit

**++(a) Give your chatbot a new name++**, to differentiate it from the placeholder name `Duke`.<br>
* **Avoid these common choices** as well: `Chatty`, `Jarvis`, `ChatBot`, `Chad`
* Rename `Duke.java` to match the chatbot name you selected, and remove all traces of `Duke` from the code.

{% call show_ai_guidance("Renaming the chatbot") %}

1. Tweak the `AGENTS.md` file in the project root, and commit it.
   <box type="info" seamless>

   AI agents read the information in `AGENTS.md`, which is included in their context.<br>
   In this specific case, things you can tweak:

   * Fill in the parts marked as `[to be filled]`
   * If using a Mac, ensure the instructions about switching to the correct Java version match your Java setup.
   </box>
1. Start a new chat/project in Codex (i.e., ChatGPT app in Codex mode). Set your iP folder as the folder of that chat.<br>
   Refer to the tutorial [_Using the Codex Desktop App_ at SE-EDU Guides](https://se-education.org/guides/tutorials/codexDesktop.html) for more info.
1. Try the following prompt.
  {% call mdblock() %}
  I wish to change the chatbot name from duke to [NEW NAME].
  Which files need to be changed in what way?
  {% endcall %}
1. If you are happy with the reply, you can follow up with a `Go ahead and make those changes`.<br>
   <box type="tip" seamless>

   **To economize the use of tokens, start with a cheaper model** (e.g., `Luna` at `High` or `Extra High` setting). Use more expensive models only when cheaper ones fail to meet expectations or you think the task is worth a higher cost of tokens.

    **Set the permission level to `Approve for me`**: Codex will still ask your permission when performing 'risky' actions but proceed with less risky actions without bothering you every time.
   </box>
1. If Codex doesn't update the banner, you can ask it to do so.
   {% call mdblock() %}
   Generate an ASCII-art banner for the word [NEW NAME] (case-sensitive). Give me a few variations.
   {% endcall %}
1. Examine and test the updated code. If you are happy with it, commit the changes. %%Yes, you can ask Codex to create the commit, but if you are new to Git, it is better to do the commits yourself. Besides, hand-committing can even be faster, and it saves tokens.%%

{% endcall %}


**++(b) Update the initial code to simply greet the user and exit.++**


{% set requirements_level_0 %}
Update the initial code to simply greet the user and exit.
{% endset %}

{% set sample_output_level_0 %}
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
{{ sample_output_level_0 }}
* Horizontal lines are optional. So is the banner.
* Change the wording to match the personality you wish to give your chatbot. The above is an example only.

{% call show_ai_guidance("Updating the initial code") %}

This change is simple enough to do by hand. Doing it with AI instead is a way of taking 'baby steps': you get used to working with AI without giving up much hand-coding practice. Here are two sample prompts:

<tabs>
  <tab header="Sample prompt (less AI)">

{% call mdblock() %}
The requirement given to me:

{{ req_start }}
{{ requirements_level_0 | trim }}
{{ req_end }}

 Here is an example output:
{{ sample_output_level_0 | trim }}

{{ review_prompt }}
{% endcall %}
  </tab>
  <tab header="Sample prompt (more AI)">

{% call mdblock() %}
{{ update_prompt }}

{{ req_start }}
{{ requirements_level_0 | trim }}
{{ req_end }}

Example output:

{{ sample_output_level_0 | trim }}
{% endcall %}
</tab>
</tabs>

{% endcall %}

