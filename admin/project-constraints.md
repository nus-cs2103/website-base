{% macro show_main_text() %}
<div id="main">

Your project should comply with the following constraints.
%%**Reason**: to increase comparability among projects and to maximize applicability of module learning outcomes in the project.%%

* **Constraint-Morph**: The final product should be a result of morphing the given code base. i.e. enhance and/or evolve the given code to arrive at the new software. However, you are allowed to replace all existing code with new code, as long as it is done incrementally. %%e.g. one feature/component at a time%%<br/>
  %%**Reason:** To ensure your code has a decent quality level from the start.%%
  
* **Constraint-Incremental**: The product needs to be developed incrementally over the project duration. While it is fine to do less in some weeks and more in other weeks, a reasonably consistent delivery rate is expected. For example, it is not acceptable to do the entire project over the recess week and do almost nothing for the remainder of the semester. %%Reasons: 1. To simulate a real project where you have to work on a code base over a long period, possibly with breaks in the middle. 2. To learn how to deliver big features in small increments.%%

<span id="constraint-cli">

* **Constraint-CLI**: Command Line Interface is the primary mode of input. The GUI should be used primarily to give visual feedback to the user rather than to collect input. Some minimal use of mouse is OK (e.g. to click the minimize button), but the primary input should be command-driven. 
  * Mouse actions should have keyboard alternatives. 
  * Typing is preferred over key combinations. Design the app in a way that you can do stuff faster by typing compared to mouse actions or key combinations.
  * <tooltip content="typing the full command and hitting ENTER will complete the task">One-shot commands</tooltip> are preferred over <tooltip content="prompting the user to input one parameter at a time">multi-step commands</tooltip>. If you provide a multi-step command to help new users, you should also provide a one-shot equivalent for regular users. %%&nbsp;Reason: We want the user to be able to accomplish tasks faster using CLI than a GUI; having to enter commands part-by-part will slow down the user.%%
  * {{ icon_important_big_red }} While we don't prohibit <tooltip content="i.e. no CLI equivalent">GUI-only</tooltip> features, such features will be ignored during grading.

</span>

* **Constraint-Human-Editable-File**: The data should be stored locally and should be in a human editable text file.<br/> 
  %%**Reason:** To allow advanced users to manipulate the data by editing the data file.%%

* **Constraint-OO**: The software should follow the Object-oriented paradigm.<br/> 
  %%**Reason:** For you to practice using OOP in a non-trivial project.%%  
    
* **Constraint-No-DBMS**: Do not use a <tooltip content="Database Management System e.g., MySQL">DBMS</tooltip> to store data.<br/>
  %%**Reason:** Using a DBMS to store data will reduce the room to apply OOP techniques to manage data. It is true that most real world systems use a DBMS, but given the small size of this project, we need to optimize it for {{ module_pair }} module learning outcomes; covering DBMS-related LOs will have to be left to database modules or level 3 project modules.%%

* **Constraint-Platform-Independent**: The software should work on the Windows, Linux, and OS-X platforms. Even if you are unable to manually test the app on all three platforms, consciously avoid using OS-dependent libraries and OS-specific features.<br/>
  %%**Reason:** Peer testers should be able to use any of these platforms.%%

* **Constraint-No-Installer**: The software should work without requiring an installer. Having an optional installer is OK as long as the portable (non-installed) version has all the critical functionality.  
  %%**Reason:** We do not want to install all your projects on our testing machines when we test them for grading.%%

* **Constraint-Minimal-Network**:
  * The software should not depend on your own remote server. %%**Reason:** Anyone should be able to test your app any time, even after the semester is over.%%
  * It is OK to use a reliable public API e.g., Google search but we recommend that you have a fallback mechanism (e.g., able to load data using a data file if the network is down). %%**Reason:** During the mass peer-testing session the network access can be intermittent due to high load. If your feature cannot be tested due to lack of Internet, that will have to be counted as a major bug, to be fair to those whose app is being tested and bugs found being penalized.%%
  * Also be cautioned that automated testing of such features will be harder, and public APIs can block your access if they mistake your automated tests as a bot attack.

* **Constraint-External-Software**: The use of third-party frameworks/libraries is allowed but only if they,
    *   are free, open-source, and have permissive license terms %%(E.g., trial version of libraries that require purchase after N days are not allowed)%%.
    *   do not require any installation by the user of your software.
    *   do not violate other constraints.

  and is subjected to prior approval by the teaching team.<br> 
  %%**Reason:** We will not allow third-party software that can interfere with the learning objectives of the module.%%

  Please ==post in the [forum]({{module_org}}/forum/issues) your request to use a third-party libraries== _before_ you start using the library. Once a specific library has been approved for one team, other teams may use it without requesting permission again.<br/>
  %%**Reason:** The whole class should know which external software are used by others so that they can do the same if they wish to.%%


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-constraints", show_main_text) }}
