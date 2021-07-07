{% from "common/macros.njk" import embed_topic with context %}

{% macro show_constraint(constraint_id, recommendation=false) -%}
{% set constraint_style = "info" if recommendation else "warning" %}
{% set constraint_icon = ":far-thumbs-up:" if recommendation else ":fas-ban:" %}
<div id="{{ constraint_id }}">

#### <span class="badge badge-{{ constraint_style }} text-monospace">{{ constraint_icon }} {{ constraint_id }}</span>
<div class="indented-level2">

{{ caller() }}
</div>
</div>
{%- endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-constraints") %}
<div id="main">

**Your project should comply with the following constraints.** %%**Reason**: to increase comparability among projects and to maximize applicability of module learning outcomes in the project.%%

<span tags="m--cs2103 m--tic4002">

{% call show_constraint("Constraint-Brownfield") -%}
The final product should be a result of evolving/enhancing/morphing the given code base. However, you are allowed to replace all existing code with new code, as long as it is done incrementally. %%e.g. done in small steps, each producing a working product%%<br/>
%%**Reason:** To simulate a brownfield project.%%
{%- endcall  %}
</span>

{% call show_constraint("Constraint-Typing-Preferred") -%}
The product should be targeting users who can type fast and prefer typing over other means of input.<br>
%%**Reason**: to increase comparability of products, and to make feature evaluation easier for peer evaluators.%%
{%- endcall  %}

{% call show_constraint("Constraint-Single-User") -%}
The product should be for a single user i.e. (not a multi-user product).<br>
%%**Reason**: multi-user systems are hard to test, which is unfair for peer testers who will be graded based on the number of bugs they find.%%
{%- endcall  %}

{% call show_constraint("Constraint-Incremental") -%}
The product needs to be developed in a breadth-first incremental manner over the project duration. While it is fine to do less in some weeks and more in other weeks, a reasonably consistent delivery rate is expected. For example, it is not acceptable to do the entire project over the recess week and do almost nothing for the remainder of the semester.<br>
%%**Reasons**: 1. To simulate a real project where you have to work on a code base over a long period, possibly with breaks in the middle. 2. To learn how to deliver big features in small increments.%%
{%- endcall  %}

{% call show_constraint("Constraint-Human-Editable-File") -%}
The data should be stored locally and should be in a human editable text file.<br/>
%%**Reason:** To allow advanced users to manipulate the data by editing the data file.%%
{%- endcall  %}

{% call show_constraint("Constraint-No-DBMS") -%}
Do not use a <tooltip content="Database Management System e.g., MySQL">DBMS</tooltip> to store data.<br/>
%%**Reason:** Using a DBMS to store data will reduce the room to apply OOP techniques to manage data. It is true that most real world systems use a DBMS, but given the small size of this project, we 
need to optimize it for {{ module_pair }}
module learning outcomes; covering DBMS-related topics will have to be left to database modules or level 3 project modules.%%
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
The software should work on a computer that has version 11 of Java %%i.e., no other Java version installed%%.
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
The use of third-party frameworks/libraries is allowed but only if they,
* are free, open-source, and have permissive license terms %%(E.g., trial version of libraries that require purchase after N days are not allowed)%%.
* do not require any installation by the user of your software.
* do not violate other constraints.

and is subjected to prior approval by the teaching team.<br> 
%%**Reason:** We will not allow third-party software that can interfere with the learning objectives of the module.%%

Please ==post in the [forum]({{url_module_org}}/forum/issues) your request to use a third-party libraries== _before_ you start using the library. Once a specific library has been approved for one team, other teams may use it without requesting permission again.<br/>
%%**Reason:** The whole class should know which external software are used by others so that they can do the same if they wish to.%%
{%- endcall  %}

{% call show_constraint("Constraint-Single-File") -%}
Package everything into a single JAR file.<br>
%%**Reason:** Requiring the users to download more files can cause complications in the final peer testing session.%%

If you are unable to package everything into a JAR file, package the JAR file and other files needed into a single zip file.
{%- endcall  %}

{% call show_constraint("Constraint-File-Size") -%}
The file sizes of the deliverables should not exceed the limits given below. <br>
<div tags="m--cs2113 m--cs2103 m--tic4002">

%%**Reason:** It is hard to download big files during the practical exam due to limited WiFi bandwidth at the venue%%:</div>

* <span class="text-danger">Product (i.e., the JAR/ZIP file): 100MB</span> (Some third-party software -- e.g., Stanford NLP library, certain graphics libraries -- can cause you to exceed this limit)

* <span class="text-danger">Documents (i.e., PDF files): 15MB/file</span> (Not following [the recommended method of converting to PDF format](https://se-education.org/guides/tutorials/savingPdf.html) can cause big PDF files. Another cause is using unnecessarily high resolution images for screenshots).
{%- endcall  %}

{% call show_constraint("Constraint-PDF-Friendly") -%}
The DG and UG should be PDF-friendly. Don't use expandable panels, embedded videos, animated GIFs etc. <br>

%%**Reason:** The UG and DG used in the final grading will be in PDF format%%:
{%- endcall  %}

-----------------------------------------------------------------------------------------------------------------------

**In addition, you are strongly encouraged to follow these recommendations** as they can help increase your project score.

{% call show_constraint("Recommendation-Minimal-Network", recommendation=true) -%}
It is OK to use a reliable public API %%e.g., Google search%% but we recommend that you have a fallback mechanism (e.g., able to load data using a data file if the network is down).<br>
  %%**Reason:** During the mass peer-testing session, the network access can be intermittent due to high load. If your feature cannot be tested due to lack of Internet, that will have to be counted as a major bug, to be fair to those whose app is being tested and bugs found being penalized.%%<br>
  ==If you use NUS data== (e.g., scrape data from an NUS website), please work with [NUS IT](https://nusit.nus.edu.sg/contact-us/) directly to get their approval first. Even well-intentioned use of NUS data without approval can get you into serious trouble (has happened before). The teaching team will not be able to get approval for you as the use of NUS data is not a module requirement.
{%- endcall %}

{% call show_constraint("Recommendation-Testability", recommendation=true) -%}
Avoid implementing hard-to-test (both for manual testing as well as automated testing) features or features that make your product hard-to-test.<br>
%%**Reason**: ==_testability_ is a grading criterion.== If you choose to implement such a feature, you will need to spend an extra effort to reach an acceptable level of testability.%%
Here are some examples of features that are hard-to-test:
* Features that depend heavily on remote APIs: Those APIs can block your access if they mistake your automated tests as a bot attack. Some remote APIs require setting up accounts, keys, login etc, that will irritate the testers of your product and give a low rating to the testability of your work.
* Audio-related features: The peer testing of your product is done under exam conditions where it is not appropriate to play audio.
* Features that require creating user accounts, login, logout etc.
{%- endcall %}

<span tags="m--cs2113 m--tic4001">

{% call show_constraint("Recommendation-No-GUI", recommendation=true) -%}
Creating a good Java GUI takes a lot of extra effort, which can easily push the tP effort beyond the expected range. In addition, good GUI design is not a learning outcome of this module. Therefore, you are strongly discouraged from creating a GUI application. Choose the GUI path only if you are willing to take the extra workload on top of the module's normal load.
{%- endcall %}
</span>


{% call show_constraint("Recommendation-CLI-First", recommendation=true) -%}
Following from the _Constraint-Typing-Preferred_, if the app is optimized for the target user (graded under the _product design_ criterion), ==a user who can type fast should be able to accomplish most tasks faster via CLI, compared to a hypothetical GUI-only version of the app.== %%For example, adding a new entity via the CLI should be faster than entering the same data through a GUI form.%%<br>
Therefore, the input to the app needs to be primarily CLI. <span tags="m--cs2103 m--tic4002">The GUI is used primarily to give visual feedback to the user.</span><span tags="m--cs2113 m--tic4001">If you do implement a GUI, that GUI should primarily be used to give visual feedback to the user.</span> While we don't prohibit non-CLI inputs, note that such inputs will reduce the suitability of the product to target users. Therefore, give CLI alternatives to mouse/GUI inputs, if applicable.<br>
Also keep in mind:
* Regular typing is usually faster than using key combinations.
* <tooltip content="typing the full command and hitting ENTER will complete the task">One-shot commands</tooltip> are faster over <tooltip content="prompting the user to input one parameter at a time">multi-step commands</tooltip>. If you provide a multi-step command to help new users, it is recommended that you also provide a one-shot equivalent for regular/expert users.<br>
{%- endcall %}

<box type="warning">

If you are not sure if your product complies with a certain constraint/recommendation, please seek clarification by posting in the [forum]({{url_module_org}}/forum/issues) (preferred) or emailing the supervisor.
</box>

</div>

{% endcall %}
