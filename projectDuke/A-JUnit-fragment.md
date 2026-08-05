{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-JUnit", "Add JUnit tests", "primary") }}

Add JUnit tests to test the behavior of the code.

* **Minimal**: Use JUnit to test ==at least two non-trivial methods==, from two different classes (if you have multiple classes),<br>
  and ensure they are ==tested reasonably well== (i.e., the test code should try to catch most potential bugs in the target methods).
* **Stretch goal**: Use JUnit to test all non-trivial public methods of all classes.

Refer to the [_JUnit tutorial_ @se-edu/guides](https://se-education.org/guides/tutorials/junit.html) to find how to use JUnit (in the context of this project).

{% call show_ai_guidance("A-JUnit") %}

{{ icon_tip }} If you haven't written JUnit tests before, you may want to write the first 1-2 JUnit tests by hand.

Here a series of prompts for ramping up the JUnit tests in the code base.

{% call mdblock() %}
Add a JUnit test to test one of the methods in the codebase. Choose a method that lends itself well to testing through JUnit.
Include all reasonable test cases.
Follow Gradle and JUnit conventions as to the file path and naming.

If names of the test methods are long, you may resort to the following naming convention:
`featureUnderTest_testScenario_expectedBehavior()`

e.g. `sortList_emptyList_exceptionThrown()` `getMember_memberNotFound_nullReturned()`
{% endcall %}
{% call mdblock() %}
Add tests for all candidate methods that deserve tests in that class.
{% endcall %}
{% call mdblock() %}
Test coverage target: Focus JUnit tests on the top ~50% highest-value methods (prioritizing complex, core, or critical business logic).

Go ahead and add more tests based on the above target.
{% endcall %}
{% call mdblock() %}
Update the relevant AI documentation to reflect the test coverage target of 50%. Mention that JUnit tests need to be updated after each code change to comply with that target.
{% endcall %}

{% endcall %}