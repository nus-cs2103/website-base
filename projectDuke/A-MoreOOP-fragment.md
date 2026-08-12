{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-MoreOOP", "Make the code more OOP", "primary") }}

{% set requirements_moreoop %}
Gradually (i.e., in small steps) extract closely related code as classes.

* **Minimal**: Extract the following classes:
  * `Ui`: deals with interactions with the user
  * `Storage`: deals with loading tasks from the file and saving tasks in the file
  * `Parser`: deals with making sense of the user command
  * `TaskList`: contains the task list, %%e.g., it has operations to add/delete tasks in the list%%
{% endset %}
{{ requirements_moreoop }}

<div class="indented-level2">
{% set requirements_moreoop_minimal %}
For example, the code of the main class could look like this:
```java
public class Duke {

    private Storage storage;
    private TaskList tasks;
    private Ui ui;

    public Duke(String filePath) {
        ui = new Ui();
        storage = new Storage(filePath);
        try {
            tasks = new TaskList(storage.load());
        } catch (DukeException e) {
            ui.showLoadingError();
            tasks = new TaskList();
        }
    }

    public void run() {
        //...
    }

    public static void main(String[] args) {
        new Duke("data/tasks.txt").run();
    }
}
```
{% endset %}
{{ requirements_moreoop_minimal }}
</div>
{% set requirements_moreoop_stretch %}
* **Stretch goal**: Consider extracting more classes, e.g., `*Command` classes (i.e., `AddCommand`, `DeleteCommand`, `ExitCommand` etc.) that inherit from an abstract `Command` class, so that you can write the main logic of the app as follows:
  ```java
  public void run() {
      ui.showWelcome();
      boolean isExit = false;
      while (!isExit) {
          try {
              String fullCommand = ui.readCommand();
              ui.showLine(); // show the divider line ("_______")
              Command c = Parser.parse(fullCommand);
              c.execute(tasks, ui, storage);
              isExit = c.isExit();
          } catch (DukeException e) {
              ui.showError(e.getMessage());
          } finally {
              ui.showLine();
          }
      }
  }
  ```
{% endset %}
<box type="info" seamless>

Your class names may differ from the ones given above. The design can differ too, as long as you can justify it as good OOP (there is no one _correct_ solution for most design problems, after all).
</box>

{% call show_ai_guidance("A-MoreOOP") %}

This is an increment that lends itself well to an incremental approach. We can ask AI to proceed incrementally, rather than us deciding on the increments. Here is an example:

{% call mdblock() %}
The target: {{ req_start }}
{{ requirements_moreoop }}
{{ requirements_moreoop_minimal }}

Your class names may differ from the ones given above. The design can differ too, as long as you can justify it as good OOP.
{{ req_end }}

Let's do this iteratively. In each iteration, do the following steps:

1. Decide the next natural stand-alone increment that moves the code closer to the target.
2. Implement that increment.
3. Test it to ensure there are no regressions, using the /test-ui skill.
4. Commit the changes with a detailed commit message. You have my permission to commit in this repo.
4. Generate a visual diff using the /present-changes-visually skill. Also explain the rationale for the change and its pros and cons.
5. Briefly outline the next increment to be done in the next iteration. If there are no more increments worth doing, say so and stop.

Go ahead and do the first iteration.
{% endcall %}

After the first iteration is done, examine the change and the rationale. If you don't agree with the change at all, ask Codex to discard the commit. If you want the change to be done in a slightly different way (e.g., you prefer a different class name), ask Codex to update the code accordingly and amend the commit as well.

When there are no more changes to be done, you can check if the stretch goal has been met. Then, you can prompt AI to go for it.

{% call mdblock() %}
Now, let's go for the stretch goal given below. Proceed in the same iterative fashion as before.

{{ req_start }}
{{ requirements_moreoop_stretch }}
{{ req_end }}
{% endcall %}

{% endcall %}
