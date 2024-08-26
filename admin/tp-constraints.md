{% from "common/macros.njk" import embed_topic with context %}

{% macro show_constraint(constraint_id, recommendation=false) -%}
{% set constraint_style = "info" if recommendation else "warning text-dark" %}
{% set constraint_icon = ":far-thumbs-up:" if recommendation else ":fas-ban:" %}
<div id="{{ constraint_id }}">

#### <span class="badge bg-{{ constraint_style }} text-monospace">{{ constraint_icon }} {{ constraint_id }}</span>
<div class="indented-level2">

{{ caller() }}
</div>
</div>
{%- endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-constraints") %}
<div id="main">

**Your project should comply with the following constraints.** %%**Reason**: to increase comparability among projects and to maximize applicability of course learning outcomes in the project.%%

<span tags="m--cs2103">

{% call show_constraint("Constraint-Brownfield") -%}
The final product should be a result of evolving/enhancing/morphing the given codebase. However, you are allowed to replace all existing code with new code, as long as it is done incrementally. %%e.g. done in small steps, each producing a working product%%<br/>
%%**Reason:** To simulate a brownfield project.%%
{%- endcall  %}
</span>

{% call show_constraint("Constraint-Typing-Preferred") -%}
The product should be targeting users who can type fast and prefer typing over other means of input.<br>
%%**Reason**: by enforcing some similarity among target users of the projects, we hope to make the projects more comparable with each other.%%
{%- endcall  %}

{% call show_constraint("Constraint-Single-User") -%}
The product should be for a single user i.e. (not a multi-user product).<br>
Not allowed: Application running in a shared computer and different people using it at different times.<br>
Not allowed: The data file created by one user being accessed by another user during regular operations (e.g., through a shared file storage mechanism).<br>
%%**Reason**: multi-user systems are hard to test, which is unfair for peer testers who will be graded based on the number of bugs they find.%%
{%- endcall  %}

{% call show_constraint("Constraint-Incremental") -%}
The product needs to be developed in a breadth-first incremental manner over the project duration. While it is fine to do less in some weeks and more in other weeks, a reasonably consistent delivery rate is expected. For example, it is not acceptable to do the entire project over the recess week and do almost nothing for the remainder of the semester.<br>
%%**Reasons**: 1. To simulate a real project where you have to work on a codebase over a long period, possibly with breaks in the middle. 2. To learn how to deliver big features in small increments.%%
{%- endcall  %}

{% call show_constraint("Constraint-Human-Editable-File") -%}
The data should be stored locally and should be in a human editable text file.<br/>
%%**Reason:** To allow advanced users to manipulate the data by editing the data file.%%

<panel type="seamless" header="FAQ: Is it OK to encrypt the data file?">

Generally, not recommended. It can be allowed only if the application provides an easy way to decrypt the file, and encrypt it again after editing it manually.

Followup question: What if the data in the file is confidential, and therefore, it is risky to leave it in plaintext format?<br>
While this is a valid concern, you can assume/require that the app is used in a secure environment in which data are protected by default e.g., a personal computer already password protected.
</panel>
{%- endcall  %}

{% call show_constraint("Constraint-No-DBMS") -%}
Do not use a <tooltip content="Database Management System e.g., MySQL">DBMS</tooltip> to store data.<br/>
%%**Reason:** Using a DBMS to store data will reduce the room to apply OOP techniques to manage data. It is true that most real world systems use a DBMS, but given the small size of this project, we
need to optimize it for {{ course_pair }}
course learning outcomes; covering DBMS-related topics will have to be left to database courses or level 3 project courses.%%
{%- endcall  %}

{% call show_constraint("Constraint-OO") -%}
The software should follow the Object-oriented paradigm primarily (but you are allowed to mix in a bit other styles when justifiable).<br/>
%%**Reason:** For you to practice using OOP in a non-trivial project.%%
{%- endcall  %}

{% call show_constraint("Constraint-Platform-Independent") -%}
The software should work on the Windows, Linux, and OS-X platforms. Even if you are unable to manually test the app on all three platforms, deliberately avoid using OS-dependent libraries and OS-specific features.<br/>
%%**Reason:** Peer testers should be able to use any of these platforms.%%
{%- endcall  %}

{% call show_constraint("Constraint-Java-Version") -%}
The software should work on a computer that has version 17 of Java %%i.e., no other Java version installed%%.
{%- endcall  %}

{% call show_constraint("Constraint-Portable") -%}
The software should work without requiring an installer.<br>
%%**Reason:** Testers may not want to install your product on their computer.%%
{%- endcall  %}

{% call show_constraint("Constraint-No-Remote-Server") -%}
The software should not depend on your own remote server.<br>
%%**Reason:** Anyone should be able to use/test your app any time, even after the semester is over.%%
{%- endcall  %}

{% call show_constraint("Constraint-External-Software") -%}
The use of third-party frameworks/libraries/services is allowed but only if they,
* are free, open-source (this doesn't apply to services), and have permissive license terms %%(E.g., trial version of libraries that require purchase after N days/uses are not allowed)%%.
* do not require any installation by the user of your software.<br>
  In case of services, requiring the user to create an account on a third-party service is strongly discouraged as it can result in your product for 'low testability'.
* do not violate other constraints.

and is subjected to prior approval by the teaching team.<br>
%%**Reason:** We will not allow third-party software that can interfere with the learning objectives of the course.%%

Please ==post in the [forum]({{url_course_org}}/forum/issues) your request to use a third-party libraries/services== _before_ you start using the library. Once a specific software has been approved for one team, other teams may use it without requesting permission again.<br/>
%%**Reason:** The whole class should know which external software are used by others so that they can do the same if they wish to.%%
{%- endcall  %}


<span tags="m--cs2103">

{% call show_constraint("Constraint-Screen-Resolution") -%}
The GUI should _work well_ (i.e., should not cause any resolution-related inconveniences to the user) for,
* standard screen resolutions 1920x1080 and higher, and,
* for screen scales 100% and 125%.

In addition, the GUI should be _usable_ (i.e., all functions can be used even if the user experience is not optimal) for,
* resolutions 1280x720 and higher, and,
* for screen scales 150%.


{%- endcall %}
</span>

{% call show_constraint("Constraint-Single-File") -%}
Package everything into a single JAR file.<br>
%%**Reason:** Requiring the users to download more files can cause complications in the final peer testing session.%%

If you are unable to package everything into a JAR file, package the JAR file and other files needed into a single zip file.
{%- endcall  %}

{% call show_constraint("Constraint-File-Size") -%}
The file sizes of the deliverables should be reasonable and not exceed the limits given below. <br>
<div tags="m--cs2113 m--cs2103">

%%**Reason:** It is hard to download big files during the practical exam due to limited WiFi bandwidth at the venue. Plus, there is no reason to use space/bandwidth without a proportional benefit.%%</div>

* <span class="text-danger">Product (i.e., the JAR/ZIP file): 100MB</span> (Some third-party software -- e.g., Stanford NLP library, certain graphics libraries -- can cause you to exceed this limit)

* <span class="text-danger">Documents (i.e., PDF files): 15MB/file</span> (Not following [the recommended method of converting to PDF format](https://se-education.org/guides/tutorials/savingPdf.html) can cause big PDF files. Another cause is using unnecessarily high resolution images for screenshots).

In addition, do ==ensure that the final JAR/PDF files are not bloated unnecessarily==. Such <span class="text-danger">bloat can be reported as a bug</span>.
Some suggestions:

* Check if the the assets (e.g., images, audio, data) included in the JAR files are all strictly necessary and the quality is not unnecessarily high (e.g., images with higher resolution than necessary).
* Check if the third-party libraries in the JAR file are strictly necessary or whether they have lighter versions that are still enough for your purpose.
* Using [JavaFX WebView](http://tutorials.jenkov.com/javafx/webview.html) allows you to display a Web page within your application but it adds about 70MB to your JAR file. If you decide to use that library, ensure the benefit is worth the increase in size.
{%- endcall  %}

{% call show_constraint("Constraint-PDF-Friendly") -%}
The DG and UG should be PDF-friendly. Don't use expandable panels, embedded videos, animated GIFs etc. <br>

%%**Reason:** The UG and DG used in the final grading will be in PDF format%%
{%- endcall  %}

-----------------------------------------------------------------------------------------------------------------------

**In addition, you are strongly encouraged to follow these recommendations** as they can help increase your project score.

{% call show_constraint("Recommendation-Minimal-Network", recommendation=true) -%}
It is OK to use a reliable public API %%e.g., Google search%% but we recommend that you have a fallback mechanism (e.g., able to load data using a data file if the network is down).<br>
  %%**Reason:** During the mass peer-testing session, the network access can be intermittent due to high load. If your feature cannot be tested due to lack of Internet, that will have to be counted as a major bug, to be fair to those whose app is being tested and bugs found being penalized.%%<br>
  ==If you use NUS data== (e.g., scrape data from an NUS website), please work with [NUS IT](https://nusit.nus.edu.sg/contact/) directly to get their approval first. Even well-intentioned use of NUS data without approval can get you into serious trouble (has happened before). The teaching team will not be able to get approval for you as the use of NUS data is not a course requirement.
{%- endcall %}

{% call show_constraint("Recommendation-Testability", recommendation=true) -%}
Avoid implementing hard-to-test (both for manual testing as well as automated testing) features or features that make your product hard-to-test.<br>
%%**Reason**: ==_testability_ is a grading criterion.== If you choose to implement such a feature, you will need to spend an extra effort to reach an acceptable level of testability.%%
Here are some examples of features that are hard-to-test:
* Features that depend heavily on remote APIs: Those APIs can block your access if they mistake your automated tests as a bot attack. Some remote APIs require setting up accounts, keys, login etc, that will irritate the testers of your product and give a low rating to the testability of your work.
* Audio-related features: The peer testing of your product is done under exam conditions where it is not appropriate to play audio.
* Features that require creating user accounts, login, logout etc.
{%- endcall %}

<span tags="m--cs2113">

{% call show_constraint("Recommendation-No-GUI", recommendation=true) -%}
Creating a good Java GUI takes a lot of extra effort, which can easily push the tP effort beyond the expected range. In addition, good GUI design is not a learning outcome of this course. Therefore, you are strongly discouraged from creating a GUI application. Choose the GUI path only if you are willing to take the extra workload on top of the course's normal load.
{%- endcall %}
</span>


{% call show_constraint("Recommendation-CLI-First", recommendation=true) -%}
Following from the _Constraint-Typing-Preferred_, if the app is optimized for the target user (graded under the _product design_ criterion), ==a user who can type fast should be able to accomplish most tasks faster via a command line interface (CLI), compared to a hypothetical GUI-only version of the app.== %%For example, adding a new entity via the CLI should be faster than entering the same data through a GUI form.%%<br>
Therefore, the input to the app needs to be primarily CLI. <span tags="m--cs2103">The GUI is used primarily to give visual feedback to the user. This does not mean the app need to have a text UI (CLI is not the same as text UI) or it needs to work in a command console -- it simply means the input to the app should be a text command, which can even be entered using a GUI (similar to how AB3 does it).</span><span tags="m--cs2113">If you do implement a GUI, that GUI should primarily be used to give visual feedback to the user.</span> While we don't prohibit non-CLI inputs (e.g., clicking of a button), note that such inputs will reduce the suitability of the product to target users. Therefore, give CLI alternatives to mouse/GUI inputs, if applicable.<br>
Also keep in mind:
* Regular typing is usually faster than using key combinations.
* <tooltip content="typing the full command and hitting ENTER will complete the task">One-shot commands</tooltip> are faster over <tooltip content="prompting the user to input one parameter at a time">multi-step commands</tooltip>. If you provide a multi-step command to help new users, it is recommended that you also provide a one-shot equivalent for regular/expert users.<br>
{%- endcall %}

{% call show_constraint("Recommendation-Realistic", recommendation=true) -%}
Keeping the target usage of the application 'realistic' can be helpful when making product design decisions later. For example, _a patient tracking app for a big hospital_ is not realistic usage scenario because a big hospital is unlikely to use a small standalone desktop application for that purpose. However, it is more realistic for an independent home-based healthcare worker (e.g., a physical therapist) to use such an app to keep track of his/her patients.
{%- endcall %}

<box type="warning">

If you are not sure if your product complies with a certain constraint/recommendation, please seek clarification by posting in the [forum]({{url_course_org}}/forum/issues) (preferred) or email prof.
</box>

</div>

{% endcall %}
