**Questions to discuss during the lecture:**

<panel header="{{ icon_Q }} Review code for quality">
<question has-input="true">

Suggest ways to improve the quality of the code below.

```java
...
private static final String MESSAGE_COMMAND_HELP_PARAMETERS = "Parameters: %1$s";
private static final String MESSAGE_COMMAND_HELP_EXAMPLE = "Example: %1$s";
private static final String MESSAGE_DISPLAY_PERSON_DATA = "%1$s  Phone Number: %2$s  Email: %3$s";
private static final String GOODBYE_MESSAGE = "Exiting Address Book... Good bye!";
private static final String MESSAGE_INVALID_COMMAND_FORMAT = "Invalid command format: %1$s";
...
/** List of all persons in the address book. */
private static final ArrayList<String> person = new ArrayList<>();
...
public static void main(String[] args) {
    showWelcomeMessage();
    processProgramArgs(args);
    loadDataFromStorage();
    while (true) {
        System.out.print("Enter command: ");
        String userCommand = SCANNER.nextLine();
        userCommand = userCommand.trim();
        showToUser(userCommand);
        String feedback = executeCommand(userCommand);
        showResultToUser(feedback);
    }
}
...
/**
 * Show a message to the user
 */
private static void showToUser(String message) {
  System.out.println(LINE_PREFIX + m);
}
```

<div slot="hint">

Some relevant points:

* Similar things should be named similarly (consistency helps readability)
* Use singular names for variables that handle single values
* SLAP: The code of a method should be written as high-level as possible, and at the same level of abstraction
* The first sentence of a method header comment should follow a certain phrasing (refer to coding standard)
* Constant names don't follow camelCase (refer coding standard)
* Indentation should be consistent

</div>

</question>
</panel>

