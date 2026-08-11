{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Jar", "Package the App as a JAR file", "primary") }}

Package the app as an executable JAR file so that it can be distributed easily.

You can assume **the user will run the JAR file in the following way only**:
1. Copy the JAR file into an empty folder.
1. Open a command window in that folder.
1. Run the command `java -jar "{filename}.jar"` e.g., `java -jar "Duke.jar"` (i.e., run the command in the same folder as the JAR file).

<box type="info" seamless>

The double quotes around the filename in the `java -jar "{filename}.jar"` command are not normally needed, but they are needed if the filename contains special characters such as spaces or `[`.
</box>

<box type="info" icon=":fas-question:" seamless>

FAQ: Can we double-click the JAR file to run it?<br>
A: Yes, that usually works too, but being able to do so is not a requirement here. Instead, the `java -jar` command is the recommended way to run the JAR file.
</box>

Refer to the tutorial [_Working with JAR files_ @SE-EDU/guides](https://se-education.org/guides/tutorials/jar.html) to learn how to create JAR files (in the context of this project).

<box type="info" seamless>

**If your project is being revision-controlled using Git/GitHub**,<br>

* <span class="text-danger">do not commit the JAR file created</span>. Reason: We don't normally commit generated binary files into the repository.

* Instead, you can make the JAR file available (via the GitHub release mechanism) in the following manner.

  1. Go to your fork on GitHub and [create a new _release_](https://help.github.com/en/articles/creating-releases).
  1. In the page where you supply the details of the release,
     1. give an appropriate version number e.g., `v0.1`
     1. attach the JAR file where it says `Attach binaries by dropping them ...`.
</box>



{% call show_ai_guidance("A-Jar") %}

<tabs>
  <tab header="Sample prompt (less AI)">
{% call mdblock() %}
How do I update the `build.gradle` to create a fat JAR file for this project using the shadowJar plugin?
Also explain how to create, locate, and run that JAR file.
{% endcall %}
  </tab>
  <tab header="Sample prompt (more AI)">
{% call mdblock() %}
Update the relevant files so that I can create a fat JAR file for this project using the shadowJar plugin.
Explain the steps you took. Also explain how to create, locate, and run that JAR file.
{% endcall %}
</tab>
</tabs>

{% endcall %}
