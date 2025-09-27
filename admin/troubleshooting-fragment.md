{% from "common/macros.njk" import as_tag, embed_topic, thumb_small with context %}

<!-- =============================================================== -->
<div id="ts-jarBreaksOnOtherOs-E">My JAR file works on my OS, but not other OSes</div>
<div id="ts-jarBreaksOnOtherOs-S">

Ensure your `build.gradle` specifies JavaFX dependencies for all three OSes, as specified in our [JavaFX tutorials](https://se-education.org/guides/tutorials/javaFxPart1.html#setting-up-java-fx).

</div>
<!-- =============================================================== -->
<div id="ts-uiPngRed-E">`Ui.png` is not green in the dashboard even after I've added it to the repo.</div>
<div id="ts-uiPngRed-S">

* Ensure you've named it exactly as `Ui.png` (case-sensitive) and put it in the expected folder.
* If you changed the case of your local file, ensure the file in your remote repo has the same name upper/lower case as the local file. Git does not propagate case changes in file names through pushes. You'll need to do some extra Git actions to propagate the case change to the remote repo.<br>
  e.g., Although you changed `UI.png` to `Ui.png` in your local file, the remote repo's copy will remain `UI.png` even after you push changes to the remote repo.
* Ensure you have published your iP website using GitHub pages, and the screenshot appears in the [iP Showcase page](ip-showcase.md).

</div>
<!-- =============================================================== -->
<div id="ts-markdownTablesNotRendering-E">Markdown tables render correctly in GitHub file preview but not in the iP website.</div>
<div id="ts-markdownTablesNotRendering-S">

Ensure there is a blank line separates the table from the content just above it. This is a requirement of the Markdown syntax -- the Markdown parser used by GitHub's file preview forgives violations of this rule but not the parser used by the website renderer.

</div>

<!-- =============================================================== -->
<div id="ts-missingJavafxComponent-E">Error when running JAR file: `JavaFX runtime components are missing`</div>
<div id="ts-missingJavafxComponent-S">

Ensure your `build.gradle` specify the `Launcher` class as the `mainClass`.

```groovy
application {
    mainClass.set("myduke.Launcher")
}
```
</div>

<!-- =============================================================== -->
<div id="ts-pipelineNotFound-E">Error when running JAR file: `Error initializing QuantumRenderer: no suitable pipeline found`</div>
<div id="ts-pipelineNotFound-S">

Ensure you used the [exact Java version](programmingLanguages.md) we prescribe to build the JAR file, especially if you are on macOS.
</div>

<!-- =============================================================== -->
<div id="ts-moreRecentJavaVersion-E">Error when running JAR file: `... compiled by a more recent version of the Java Runtime`</div>
<div id="ts-moreRecentJavaVersion-S">

Ensure you used the [exact Java version](programmingLanguages.md) we prescribe to build the JAR file.
</div>

<!-- =============================================================== -->