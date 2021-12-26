{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("programmingLanguages") %}
<div id="main">

<table class="two-column-content">
<tr>
<td width="160px">
 <img src="{{baseUrl}}/admin/images/JamesGosling.png" width="150px">
</td>
<td>

==**The main language** used in this module is Java==. You should use
Java for all programming activities, the project, and exam answers.

<span tags="m--cs2103">

The module doesn’t “teach” Java. We assume you already know Java basics.
We expect you to learn on your own any Java constructs not covered in your previous modules.
The exam expects you to know Java to the extent that you should be familiar with it as a result of using it in the module exercises/projects.
</span>

</td>
</tr>
</table>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We require you to use **Java 11** (the [Oracle version](https://www.oracle.com/java/technologies/downloads/#java11) or another alternative suc as the OpenJDK version) for all module work. It is your duty to ensure the code you write (and executables you produce) are compatible with that version of Java. ==Any incompatibilities will be considered as bugs==.

**If you have Java 8** in your computer, we recommend removing it, to prevent using it unintentionally.

**Why not move to Java 17?**: Yes, we are aware that Java 17 is a more recent LTS version of Java. We hope to move to it soon, but not this semester.

{% if cs2103 or tic4002 %}

<panel type="danger" header="[IMPORTANT] Advisory for :fab-apple: Mac users" minimized >

This advisory applies to **all M1 Mac users (and those who used Rosetta to get their iP to work)**

It turns out that you might not be able to run the JAR files produced by some of the classmates due to various incompatibility issues between your environment and theirs, although you may have got your own JAR file to work in your computer. Some of our tutors looked into this problem and found a specific build of OpenJDK that doesn't seem to have these problems. If you are among the affected Mac users, please switch to that version of OpenJDK by following the instructions below.

**Instructions:**
Download and install the Azul build of OpenJDK 11 version found [here](https://www.azul.com/downloads/?version=java-11-lts&os=macos&architecture=arm-64-bit&package=jdk-fx) (scroll to the bottom of the page) -- it supports fat JAR files compiled by all other systems that we have tested.

![image](https://user-images.githubusercontent.com/1673303/133399726-93f98ee4-6efb-4f37-830d-46a72298ab49.png)

Recommended: Remove the other versions of OpenJDK so that you do not accidentally launch the JAR using the wrong version (this [video](https://www.youtube.com/watch?v=wwV_L3lKYYw) shows how)

After installation, the command `java --version` should give the following output:
```{.no-line-numbers}
openjdk 11.0.12 2021-07-20 LTS
OpenJDK Runtime Environment Zulu11.50+19-CA (build 11.0.12+7-LTS)
OpenJDK 64-Bit Server VM Zulu11.50+19-CA (build 11.0.12+7-LTS, mixed mode)
```

And `whereis java` should output `/usr/bin/java`

Recommended: Set the `JAVA_HOME`/`JDK_HOME` system variables to point to `/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home`

If you encounter problems while doing the above or need more info, please ask in the forum.
</panel>



{% endif %}
</box>

</div>

{% endcall %}
