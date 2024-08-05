{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_faq with context %}

{% call show_admin_page("programmingLanguages") %}
<div id="main">

<table class="two-column-content">
<tbody>
<tr>
<td width="160px">
 <pic eager src="{{baseUrl}}/admin/images/JamesGosling.png" width="150px"></pic>
</td>
<td>

**The main language used in this course is Java**. You should use
Java for all programming activities, the project, and exam answers.

<span tags="m--cs2103">

The course doesn’t “teach” Java. We assume you already know Java basics.
We expect you to learn on your own any Java constructs not covered in your previous courses.
The exam expects you to know Java to the extent that you should be familiar with it as a result of using it in the course exercises/projects.
</span>

</td>
</tr>
</tbody>
</table>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We require you to use **Java 17** (the [Oracle version](https://www.oracle.com/java/technologies/downloads/#java17) or another alternative such as the OpenJDK version) for all course work. It is your duty to ensure the code you write (and executables you produce) are compatible with that version of Java. ==Any incompatibilities will be considered as bugs==.

**If you have Java 8** (a particularly 'sticky' version of Java) in your computer, we recommend removing it, to prevent using it unintentionally.

{% if cs2103 %}

<panel type="danger" header="[IMPORTANT] Advisory for :fab-apple: Mac users" expanded >

Mac users should use the specific Azul JDK 17 distribution specified in [this guide](https://se-education.org/guides/tutorials/javaInstallationMac.html).

To reiterate, #r#it is not enough that you have Java 17##, it needs to be ==the precise version specified== in the page linked above.

<!--
**The problem:** You might not be able to run the JAR files produced by some of the classmates due to various incompatibility issues between your environment and theirs, although you can still get your own JAR files to work in your computer.

**How to find if it applies to you:** If you are a Mac user, here are the steps to check if it applies to you:

1. Download the latest `addressbook.jar` from [here](https://github.com/se-edu/addressbook-level3/releases).
1. Open a terminal and navigate to the location where you saved the above file.
1. Check if you are using Java 11 by running the `java -version` command.
1. Launch the JAR using the `java -jar addressbook.jar` command.
1. If the text in the GUI appears garbled/unreadable, this advisory applies to you.

**Solution:** Some of our tutors looked into this problem and found a specific build of OpenJDK that doesn't seem to have these problems. If you are among the affected Mac users, please switch to that version of OpenJDK by following the instructions below.

Download and install the Azul build of OpenJDK 11 version found [here](https://www.azul.com/downloads/?version=java-11-lts&os=macos&architecture=arm-64-bit&package=jdk-fx) (scroll to the bottom of the page) -- it supports fat JAR files compiled by all other systems that we have tested. ==Remember to choose the `JDK FX`version (not any other versions)==.

![image](https://user-images.githubusercontent.com/1673303/133399726-93f98ee4-6efb-4f37-830d-46a72298ab49.png)

{{ icon_tip }} You can use https://sdkman.io to install Java e.g., `sdk install java 11.0.19.fx-zulu`

Recommended: Remove the other versions of OpenJDK so that you do not accidentally launch the JAR using the wrong version (this [video](https://www.youtube.com/watch?v=wwV_L3lKYYw) shows how)

After installation, the command `java --version` should give an output similar to the below:
```{.no-line-numbers}
openjdk 11.0.__ ____-__-__ LTS
OpenJDK Runtime Environment Zulu11.__+__-CA (build 11.0.__+_-LTS)
OpenJDK 64-Bit Server VM Zulu11.__+__-CA (build 11.0.__+_-LTS, mixed mode)
```

And `whereis java` should output `/usr/bin/java`

Recommended: Set the `JAVA_HOME`/`JDK_HOME` system variables to point to `/Library/Java/JavaVirtualMachines/zulu-11.jdk/Contents/Home`

If you encounter problems while doing the above or need more info, please ask in the forum.
-->
</panel>


{% endif %}

{{ show_faq("java21") }}
</box>

</div>

{% endcall %}
