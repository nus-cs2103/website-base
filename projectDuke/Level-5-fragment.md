{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_example with context %}

<include boilerplate src="level_thumb.md" var-text=":fas-exclamation-triangle:" inline />

### Level 5. Handle Errors

Teach the chatbot to deal with errors such as incorrect inputs entered by the user.
<br>
<br>

Example:
```
todo
    ____________________________________________________________
     OOPS!!! The description of a todo cannot be empty.
    ____________________________________________________________

blah
    ____________________________________________________________
     OOPS!!! I'm sorry, but I don't know what that means :-(
    ____________________________________________________________
```

<box type="important" seamless>

You are strongly encouraged to use your own wording for the error messages, rather than use the error message given in the example above.
</box>

<include boilerplate src="dukeNestedFragment.md" var-target="A-Exceptions" var-name="Extension: `A-Exceptions`" />
<p/>

* **Minimal**: Handle at least the two types of errors shown in the example above.
* **Typical**:
  * Handle all possible errors in the current version.
  * As you evolve the chatbot, continue to handle errors related to the new features added.
* **Stretch goals**:
  * Make the error handling more error-specific e.g., give the user a clear/specific explanation of the error and how to correct it.

{% call show_ai_guidance("Level 5. Handle Errors") %}

As before, you can proceed in small steps. Ensure AI runs the `test-ui` skill after each code update.
{% endcall %}

{% call show_ai_guidance("General: Keep updating AI files") %}

As the project progresses, observe where AI falters or overlooks things, and update the AI files accordingly.

For example, you can force AI to improve the quality of testing with a prompt like this:
{% call mdblock() %}
Add more test cases to cover edge cases and incorrect inputs.
Interleave positive and negative test cases to detect incorrect inputs affecting the correctness of the internal states.
{% endcall %}
Then, you can introduce temporary bugs into the code and see if the `test-ui` skill can detect them. If it cannot, you can ask AI to improve the skill to cover such cases.

{% endcall %}


