{% from "common/macros.njk" import as_tag, embed_topic, thumb_small with context %}

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