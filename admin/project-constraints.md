{% macro show_main_text() %}
<div id="main">

**Your project should comply with the following constraints.** %%**Reason**: to increase comparability among projects and to maximize applicability of module learning outcomes in the project.%%

* **Constraint-Brownfield**: The final product should be a result of evolving/enhancing/morphing the given code base. However, you are allowed to replace all existing code with new code, as long as it is done incrementally. %%e.g. one feature/component at a time%%<br/>
  %%**Reason:** To ensure your code has a decent quality level from the start.%%

* **Constraint-Typing-Preferred**: The product should be targeting users who can type fast and prefer typing over other means of input.<br>
  %%**Reason**: to increase comparability of products, and to make feature evaluation easier for peer evaluators.%%

* **Constraint-Single-User**: The product should be for a single user i.e. (not a multi-user product).<br>
  %%**Reason**: multi-user systems are hard to test, which is unfair for peer testers who will be graded based on the number of bugs they find.%%

* **Constraint-Incremental**: The product needs to be developed incrementally over the project duration. While it is fine to do less in some weeks and more in other weeks, a reasonably consistent delivery rate is expected. For example, it is not acceptable to do the entire project over the recess week and do almost nothing for the remainder of the semester.<br>
  %%**Reasons**: 1. To simulate a real project where you have to work on a code base over a long period, possibly with breaks in the middle. 2. To learn how to deliver big features in small increments.%%

* **Constraint-Human-Editable-File**: The data should be stored locally and should be in a human editable text file.<br/>
  %%**Reason:** To allow advanced users to manipulate the data by editing the data file.%%

* **Constraint-No-DBMS**: Do not use a <tooltip content="Database Management System e.g., MySQL">DBMS</tooltip> to store data.<br/>
  %%**Reason:** Using a DBMS to store data will reduce the room to apply OOP techniques to manage data. It is true that most real world systems use a DBMS, but given the small size of this project, we need to optimize it for {{ module_pair }} module learning outcomes; covering DBMS-related topics will have to be left to database modules or level 3 project modules.%%

* **Constraint-OO**: The software should follow the Object-oriented paradigm primarily (but you are allowed to mix in a bit other styles when justifiable).<br/>
  %%**Reason:** For you to practice using OOP in a non-trivial project.%%

* **Constraint-Platform-Independent**: The software should work on the Windows, Linux, and OS-X platforms. Even if you are unable to manually test the app on all three platforms, consciously avoid using OS-dependent libraries and OS-specific features.<br/>
  %%**Reason:** Peer testers should be able to use any of these platforms.%%

* **Constraint-Portable**: The software should work without requiring an installer.<br>
  %%**Reason:** Testers may not want to install your product on their computer.%%

* **Constraint-No-Remote-Server**: The software should not depend on your own remote server.<br>
  %%**Reason:** Anyone should be able to use/test your app any time, even after the semester is over.%%

* **Constraint-External-Software**: The use of third-party frameworks/libraries is allowed but only if they,
    * are free, open-source, and have permissive license terms %%(E.g., trial version of libraries that require purchase after N days are not allowed)%%.
    * do not require any installation by the user of your software.
    * do not violate other constraints.

  and is subjected to prior approval by the teaching team.<br> 
  %%**Reason:** We will not allow third-party software that can interfere with the learning objectives of the module.%%

  Please ==post in the [forum]({{module_org}}/forum/issues) your request to use a third-party libraries== _before_ you start using the library. Once a specific library has been approved for one team, other teams may use it without requesting permission again.<br/>
  %%**Reason:** The whole class should know which external software are used by others so that they can do the same if they wish to.%%

**In addition, you are strongly encouraged to follow these recommendations** as they can help increase your project score.

* **Recommendation-Minimal-Network**: It is OK to use a reliable public API %%e.g., Google search%% but we recommend that you have a fallback mechanism (e.g., able to load data using a data file if the network is down).<br>
  %%**Reason:** During the mass peer-testing session the network access can be intermittent due to high load. If your feature cannot be tested due to lack of Internet, that will have to be counted as a major bug, to be fair to those whose app is being tested and bugs found being penalized.%%<br>
  ==If you use NUS data== (e.g., scrape data from an NUS website), please work with [NUS IT](https://nusit.nus.edu.sg/contact-us/) directly to get their approval first. Even well-intentioned use of NUS data without approval can get you into serious trouble (has happened before). The teaching team will not be able to get approval for you as the use of NUS data is not a module requirement.

* **Recommendation-Testability**: Avoid implementing hard-to-test (both for manual testing as well as automated testing) features or features that make your product hard-to-test.<br>
  %%**Reason**: _testability_ is a grading criterion. If you choose to implement such a feature, you will need to spend an extra effort to reach an acceptable level of testability.%%
  Here are some examples of features that are hard-to-test:
  * Features that depend heavily on remote APIs: Those APIs can block your access if they mistake your automated tests as a bot attack. Some remote APIs require setting up accounts, keys, login etc, that will irritate the testers of your product and give a low rating to the testability of your work.
  * Audio-related features: The peer testing of your product is done under exam conditions where it is not appropriate to play audio.
  * Features that require creating user accounts.


<span id="constraint-cli">

* **Recommendation-CLI-First**: As per _Constraint-Typing-Preferred_, the input to the app needs to be primarily CLI. The GUI can be used to give visual feedback to the user rather than to collect input. While we don't prohibit non-CLI inputs, note that such inputs will reduce the suitability of the product to target users, which will be graded under the _product design_ criterion.<br>
  Some suggestions:
  * Give keyboard alternatives to mouse/GUI inputs, if any.
  * Regular typing is usually faster than using key combinations. Design the app in a way that you can do stuff faster by typing compared to mouse actions or key combinations.
  * <tooltip content="typing the full command and hitting ENTER will complete the task">One-shot commands</tooltip> are faster over <tooltip content="prompting the user to input one parameter at a time">multi-step commands</tooltip>. If you provide a multi-step command to help new users, you can also provide a one-shot equivalent for regular/expert users.<br>
   %%&nbsp;Reason: We want the user to be able to accomplish tasks faster using CLI than a GUI; having to enter commands part-by-part will slow down the user.%%
</span>

<box type="warning">

If you are not sure if your product complies with a certain constraint/recommendation, please seek clarification by posting in the [forum]({{module_org}}/forum/issues) (preferred) or emailing the supervisor.
</box>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-constraints", show_main_text) }}
