{% from "common/macros.njk" import ask_chatgpt, mdblock, show_ai_guidance, show_duke_extension_title with context %}

{{ show_duke_extension_title("A-Packages", "Divide classes into packages", "primary") }}

Organize the classes into suitable Java packages.

<box type="warning" seamless>

Note that `src/main/java` should be kept as the <tooltip content="root folder for Java source code">source root</tooltip> folder, as some tools we'll be using later will look for the Java source code in that folder by default.

For example, suppose you have the following structure now, and you wish to move `Duke.java` into a package `duke.ui`.

<tree>
:far-folder: [project root] %%e.g., C:\courses\project\\%%
  :far-folder: #g#src##\
    :far-folder: #g#main##\
      #g#:fas-folder: java##\ #g#[source root]##
        :far-file: Duke.java (not in a package)
</tree>

The correct way to do so is:

<tree>
:far-folder: [project root] %%e.g., C:\courses\project\\%%
  :far-folder: #g#src##\
    :far-folder: #g#main##\
       #g#:fas-folder: java##\ #g#[source root]##
        :far-folder: ==duke==\
          :far-folder: ==ui==\
            :far-file: Duke.java (in package `duke.ui`)
</tree>

Do not convert `src`, `main`, `java` into packages. For example, the following is #r#incorrect##:
<tree>
:far-folder: [project root] #r#[source root]##
  :far-folder: #g#src##\
    :far-folder: #g#main##\
      :far-folder: #g#java##\
        :far-file: Duke.java (in package `src.main.java`)
</tree>
</box>

* **Minimal**: put all classes in one package e.g., `duke`
* **Stretch goal**: divide into multiple packages as the number of classes increases e.g., `duke.task`, `duke.command`


{% call show_ai_guidance("A-Packages") %}
You can work with the AI to decide how to organize the classes into packages. Here is an example:

{% call mdblock() %}
The requirement: Organize the classes into suitable Java packages. The `src/main/java` should be kept as the source root folder.

Suggest a suitable package structure for the classes in the project. Do not implement it yet.
{% endcall %}

After some back-and-forth with the AI to settle on a package structure, you can ask it to go ahead and implement it.
{% endcall %}