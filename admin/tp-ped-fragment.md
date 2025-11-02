{% from "common/macros.njk" import embed_topic, get_date with context %}

#### <span class="badge bg-primary">PE-D</span> <span class="text-primary">Overview</span>

**What**: The product version released by the {{ version_penultimate }} iteration is subjected to a round of peer _acceptance/system testing_, also called the _Practical Exam (PE) Dry Run_ as this round of testing will be similar to the graded <trigger trigger="click" for="modal:projectDeliverablesPeDryRun-pe">Practical Exam that will be done at {{ version_final }}</trigger>.

**When**: To be done within a period of about 6 hours at the start of week {{ (ped_week | int) }} &rarr; {{ (ped_week | int) + 1 }} transition point (i.e., {{ get_date(date_w11_start if ped_week=='11' else date_w12_start, 4, time='1200-1800') }}). We recommend that you spend about 1-1.5 hours of the lecture slot (the one that falls inside the above period) for this task.

**Where**: You can do the PE-D from anywhere. There is ==no need to join a Zoom meeting== during the PE-D (or the PE).

<modal large header="Admin {{ icon_embedding }} tP → Practical Exam" id="modal:projectDeliverablesPeDryRun-pe">
<include src="tp-pe.md#tp-practicalexam"/>
</modal>

{{ icon_important_big_red }} **Grading**: The PE dry run ==affects your grade in the following ways==.
* You can earn ==up to 2 marks== (in your final tP score) for your performance in the PE-D.{% if cs2103 %}<br>
 Graded ==based on the usefulness and the quality of your bug reports==, as evaluated by the receiving team.{% endif %}
* PE dry run is a way for you to practice for the actual PE.
* Taking part in the PE dry run will earn you participation points.
* There is ==no penalty for bugs reported== in your product. Every bug you find is a win-win for you and the team whose product you are testing.

**Why**:
* **To train you** to do system and acceptance testing, bug reporting, bug <tooltip content="assigning of priority order">triaging,</tooltip> bug fixing, communicating with users/testers/developers, evaluating products etc.
* **To help you improve your product** before the final submission.

#### <span class="badge bg-primary">PE-D</span> <span class="text-primary">Preparation</span>

<include src="tp-testing-fragment.md#testingPreparations" var-pe_active_tab="0" var-pe_session="ped" var-pe_session_name="PE-D"/>

#### <span class="badge bg-primary">PE-D</span> <span class="text-primary">During the session</span>

**Use MS Teams private messages to contact prof** {{ "Damith (name: `Damith Chatura RAJAPAKSE`, NUSNET: `dcsdcr`)" if cs2103 else ''}}  via MS Teams if you need help during the PE-D. You may also use email to contact the teaching team.

<box type="warning" seamless>

****How many bugs to report?****

Report as many bugs as you can find during the given time. If you can't find many bugs at this stage when the product is largely untested, you are unlikely to be able to find enough bugs in the better-tested final submission later. So, all the more reasons to spend more time and find more bugs now.

For reference, here are what we consider as qualities of a good bug report:
<box>
<div id="bug-report-quality-criteria">

* has a descriptive title {icon="fas-check" i-class="text-success"}
* has enough details e.g., ==steps to reproduce, expected, actual, and screenshots==.
* severity/type labels chosen are not too far off
* is written in a non-confrontational tone
* points out a potentially problematic behavior (or a good way to improve the product)
</div>
</box>

{% if cs2113 %}
**Insincere bug reports** will not count for credit %%i.e., don't submit 'fake' bug reports to increase the bug count.%%

**The median number of bugs reported in the previous semester's PE-D was 9.** Someone reporting just a 2-3 bugs is usually a sign of a half-hearted attempt rather than lack of bugs to find. If you really can't find bugs, at least submit suggestions for improvements.

{% elseif cs2103 %}
#r#**Evaluation rubric:**##

-   |Meets expectations | Exceeds expectations | Greatly exceeds expectations
----|----|----|----
Number of 'good' bug reports | 3-5 | 6-8 | >9
Marks | participation points (PP) only | PP, **#g#+1## mark** added to tP score | PP, **#g#+2## marks**

**The 'good' bug reports count is determined by the team receiving your bugs.** As you can't be sure which of your bug reports will be considered as _good_ (the last criterion in particular) by the receiving team, we recommend that you aim to submit at least 8-10 bug reports in total if you aim for +1 mark, more if you are aiming for +2 marks. The **median bug reports count in the last round was 9**.
{% endif %}
</box>

While PE and PE-D are primarily _manual_ testing sessions, **you may also use any test automation tools or test scripts too.**

**Test the product and report bugs** as described below, after the start of the PE-D period (i.e., Friday 1200).

{% set pe_active_tab="0" %}

<div id="tp-pe-testing-instructions">

<box>

##### <div class="text-white bg-secondary p-1">**Testing instructions for PE and PE-D**</div>

###### <div class="text-white bg-secondary p-1">a) Downloading and launching the JAR file</div>

<tabs active="{{ pe_active_tab }}">
<tab header="PE Dry Run (at **{{ version_penultimate }}**)">

A few hours before the PE-D starts, you will be notified via email which team you will be testing in the PE-D. After sending out those emails. we'll also announce it in Canvas. %%FYI, team members will be given different teams to test, and the team you test in PE-D is different from the team you test in the PE.%%

{{ icon_important_big_red }} #r#You are not allowed to##,

* reveal the team you are testing in the PE-D/PE to anyone## or put that information in a place where others can see it. {{ bullet_x_red }}
* to share your PE-D/PE bug reports with anyone.
* to involve anyone else in your PE-D or PE tasks -- both are individual assignments, to be done by yourself.

Do the following steps ==#r#after 12 noon on the PE-D day -- get started at least by 4pm##==.
* First, download the _latest_ `.jar` file and UG/DG `.pdf` files from the team's releases page, if you haven't done this already.
* Then, you can start testing it and reporting bugs.

</tab>
<tab header="PE (at **{{ version_final }}**)">

* Download the zip file from the given location (to be given to you at least a few hours before the PE), if you haven't done that already.
* The file is zipped using a two-part password.
  * We will email you the second part in advance, via email (it's unique to each student). Keep it safe, and have it ready at the start of the PE.
  * At the start of the PE, we'll give you the first part of the password (common to the whole class), via a Canvas announcement. Use combined password to unzip the file, which should give you another zip file with the name suffix `_inner.zip`.
  * Unzip that second zip file normally (no password required). That will give you a folder containing the JAR file to test and other PDF files needed for the PE. ==Warning: do not run the JAR file while it is still inside the zip file==.<br>
  Ignore the `padding_file` found among the extracted files. %%Its only purpose is to mask the true size of the JAR file so that someone cannot guess which team they will be testing based on the zip file size.%%<br>
    :fab-apple: Some macOS versions will automatically unzip the inner zip file after you unzip the outer zip file using the password.
  * {{ icon_tip }} Strongly recommended: Try above steps using the [this sample zip file](https://github.com/nus-cs2103/website-base/files/14849276/JohnDoe.zip) if you wish (first part of the password: `password1-`, second part: `password2` i.e., you should use `password1-password2` to unzip it).<br>
    Use the JAR file inside it to try the steps given below as well, to confirm your computer's Java environment is as expected and can run PE jar files.
</tab>
</tabs>
<p/>

<box type="important" id="tp-jar-testing-steps" seamless>

****Steps for testing a tP JAR file**** (please follow closely)

1. Put the JAR file ==in an empty folder== in which the app is allowed to create files %%(i.e., do not use a write-protected folder)%%.<br>
1. Open a command window. Run the `java -version` command to ensure you are using Java 17.<br>
  {{ icon_important_big_red }} Do this again even if you did this before, as your OS might have auto-updated the default Java version to a newer version.
1. Check the UG to see if there are extra things you need to do before launching the JAR file %%e.g., download another file from somewhere%%<br>
  {{ icon_info }} You may visit the team's _releases_ page on GitHub if they have provided some extra files you need to download.
1. Launch the jar file ==using the `java -jar` command== rather than double-clicking %%(reason: to ensure the jar file is using the same java version that you verified above)%%. Use double-clicking as a last resort.<br>
  {{ icon_info }} We strongly recommend surrounding the jar filename with double quotes, in case special characters in the filename causes the `java -jar` command to break.<br>
  e.g., `java -jar "[{{ course }}-F18-1][Task Pro].jar"`<br>
  :fab-windows: Windows users: use the DOS prompt or the PowerShell (not the WSL terminal) to run the JAR file.{% if cs2103 %}<br>
  :fab-linux: Linux users: If the JAR fails with an error labelled `Gdk-CRITICAL` (happens in Wayland display servers), try running it using `GDK_BACKEND=x11 java -jar jar_file_name.jar` command instead.{% endif %}
</box>

<box type="info">

**++If the product doesn't work at all:++** If the product fails catastrophically %%e.g., cannot even launch, or even the basic commands crash the app%%, {% if not cs2103 %}contact the Prof (via MS Teams, and failing that, via email) to receive a _fallback_ team to test.{% else %}do the following:

1. **Check the UG** of the team, to see if there are extra things you need to do before launching the JAR.<br>
   **Confirm that you are using Java 17** and using the `java -jar` command to run the JAR, as explained in points above.
1. **Contact prof Damith** via MS Teams (name: `Damith Chatura RAJAPAKSE`, NUSNET: `dcsdcr`) and give him<br>
(a) **a screenshot** of the error message, and<br>
(b) **your GitHub** username.
1. **Wait for him to give you a fallback** team to test.<br>
   Expected response times: [12 noon - 4pm] 20 minutes, [4-6pm] 5 minutes, [after 6pm] not available #r#(i.e., you need to resolve these issues before 6pm)##.<br>
   Contact the prof via email if you didn't get a response via MSTeams.
1. **Close bug reports you submitted for the previous team** (if any).
1. **You should not go back to testing the previous team** _after_ you've been given a fallback team to test.
{% endif %}
</box>


###### <div class="text-white bg-secondary p-1">b) What to test</div>

#g#In the scope of PE/PE-D## | #r#Not in the scope##
-------------------|---------------------
{{ icon_tick_green }} The behaviour of product jar file<br>{{ icon_tick_green }} UG (pdf file only)<br>{{ icon_tick_green }} DG (pdf file only) | {{ icon_x_red }} The product website, including `.md` files such as README.md<br>{{ icon_x_red }} Data and config files that comes with the app (unless they affect the app behavior)<br>{{ icon_x_red }} Terminal output (unless it attracts the attention of the user and worries/alarms him/her unnecessarily)<br>{{ icon_x_red }} Code quality issues (but there is no restriction on examining code to identify product/UG/DG bugs)

* **Test ==based on the Developer Guide== (Appendix named _Instructions for Manual Testing_) ==and the User Guide== PDF files.** The testing instructions in the Developer Guide can provide you some guidance but if you follow those instructions strictly, you are unlikely to find many bugs. You can deviate from the instructions to probe areas that are more likely to have bugs.<br>
 **If the provided UG/DG PDF files have serious issues** (e.g., some parts seem to be missing) you can report it as a bug, and then, use the Web versions of UG/DG for the testing.{% if cs2103 and pe_session=='pe' %}
* **[==PE-only== (not applicable to PE-D)] The DG appendix named _Planned Enhancements_** (if it exists) gives some enhancements the team is planning for the near future. The feature flaws these enhancements address are 'known' -- reporting them will not earn you any credit.<br/>
  However, you can report `type.FeatureFlaws` bugs if you think these enhancements themselves are flawed/inadequate.<br/>
  You can also report `type.DocumentationBug` bugs if any of the enhancements in this list combines more than one enhancement.
{% endif %}
* **You may do both _system testing_ and _acceptance testing_**.
* **Focus on product testing first**, before expanding the focus to reporting documentation bugs.<br>
  Reason: If there are serious issues with the jar file that makes product testing impossible, you need to find that out quickly (within the first 10 minutes) so that you can switch to a different product to test. If you find yourself in such a situation much later, the time spent testing the previous product would go to waste.
* {{ icon_tip }} **Be careful when copying commands from the UG** (PDF version) to the app as some PDF viewers can affect the pasted text. If that happens, you might want to open the UG in a different PDF viewer.<br>
  If the command you copied spans multiple lines, check to ensure the line break did not mess up the copied command.

###### <div class="text-white bg-secondary p-1">c) What bugs to report?</div>

* You may **report #g#++functionality bugs++, ++feature flaws++, ++UG bugs++, and ++DG bugs++##.**
<div class="indented-level1">

{{ embed_topic("tp-grading-bugs-fragment.md#functionalityBugs", "Admin " + icon_embedding + " tP Grading → **Functionality Bugs**") }}<br>
{{ embed_topic("tp-grading-bugs-fragment.md#featureFlaws", "Admin " + icon_embedding + " tP Grading → **Feature Flaws**") }}<br>
{{ embed_topic("tp-grading-bugs-fragment.md#ugBugs", "Admin " + icon_embedding + " tP Grading → **Possible UG Bugs**") }}<br>
{{ embed_topic("tp-grading-bugs-fragment.md#dgBugs", "Admin " + icon_embedding + " tP Grading → **Possible DG Bugs**") }}<br>
</div><p/>


* Do not post suggestions but if the product is missing a critical functionality that makes the product less useful to the intended user, it can be reported as a bug of type `Type.FeatureFlaw`. The dev team is allowed to reject bug reports framed as mere suggestions or/and lacking in a convincing justification as to why the omission or the current design of that functionality is problematic.

* **It may be useful to read the PE guidelines the dev team will follow when responding to bug reports**, given in the panel below. You can ignore the `General:` section though.
<div class="indented-level1">
<panel type="info" header="Guidelines for the dev team to follow when triaging PE bugs" peek>

<include src="tp-pe-bug-triaging-guidelines-fragment.md"/>
</panel>
</div>
<p/>


###### <div class="text-white bg-secondary p-1">d) How to report bugs</div>

* #r# Bug reports created/updated after the allocated time will not count.##</span>
<div class="indented-level1">

{% set pe_session = 'ped' if (current_week | int) < 11 else 'pe' %}
{% set pe_session_name = 'PE-D' if (current_week | int) < 11 else 'PE' %}

<panel header="Where to post {{ pe_session_upper }} bugs" expanded>

<include src="tp-testing-fragment.md#pe-create-repo" var-pe_session="ped" var-pe_session_name="PE-D" />
</panel>
<p/>


</div>

###### <div class="text-white bg-secondary p-1">e) Bug report format</div>


* **Each bug should be a separate issue** %%i.e., do not report multiple problems in the same bug report.%%<br>
  If there are multiple bugs in the same report, the dev team will select only one of the bugs in the report and discard the others.
* **When reporting similar bugs, it is safer to report them as separate bugs** because there is no penalty for reporting duplicates. But as submitting multiple bug reports take extra time, if you are quite sure they will be considered as _duplicates_ by the dev team later, you can report them together, to save time.
* **The whole description of the bug should be in the issue description** i.e., ==do not add comments to the issue==. Any such comments will be ignored by our scripts.

* **Assign exactly one `*.severity` label.**<br>
  If multiple `severity.*` labels are assigned, we'll pick the one with the lowest severity.<br>
  If no `severity.*` labels is assigned, we'll pick `severity.Low` as the default.

<div class="indented-level1">
<include src="appendixE-gitHub.md#bug-severity" />
</div>

* **Assign exactly one `type.*` label.**<br>
  If multiple `type.*` labels are assigned, we'll pick on of the selected ones at random.<br>
  If no `type.*` labels is assigned, we'll pick one at random.

<div class="indented-level1">
<include src="tp-pe-fragment.md#type-labels" />
</div>

* **Write good quality bug reports**; ==poor quality or incorrect bug reports will not earn credit==.<br>
  Remember to give enough details for the receiving team to reproduce the bug. If the receiving team cannot reproduce the bug, you will not be able to get credit for it.

<div class="indented-level1">
<panel type="seamless" header="Reminder: Qualities of a good bug report" minimized>

<include src="tp-ped-fragment.md#bug-report-quality-criteria" />
</panel>
</div>
<p/>

* **#r#Do not## create/assign sub-issues.** Each issue will count as a separate bug report, even if you link them together as sub-issues.
* **#r#Do not## refer one bug report from another** (e.g., `This bug is similar to #12`) as such links will no longer work after the bug report is copied over during later PE/PE-D phases.

* {{ icon_info }} **If you need to include `<` or `>` symbols in your bug report**, you can either use `\` to escape them   (i.e., use `\<` and `\>` e.g., `x \< y` instead of `x < y`) or wrap it inside back-ticks.<br>
Reason: GitHub strips out content wrapped in `<` and `>`, for security reasons.
</box>
</div>

<span id="after-ped">

#### <span class="badge bg-primary">PE-D</span> <span class="text-primary">After the session</span>
* **The relevant bug reports will be transferred to your team's tP issue tracker** within a day after the session is over. Once you have received the bug reports for your product, you can decide whether you will act on reported issues before the final submission {{ version_final }}. For some issues, the correct decision could be to reject or postpone to a version beyond {{ version_final }}.<br>
  Reminder: There is no penalty for any of the bugs you received in the PE-D.

<div class="indented-level1">

<box type="info" seamless icon=":fas-angry:">

****Dealing with "What the h___ the tester was thinking?" type bug reports****{.text-info}

Some bug reports will make you angry because they seem baseless, wrong, rude etc. It's still possible to get value from such bug reports though:
* After you got over the initial indignation, dig deeper to see if there's even the slightest possibility that there is a bug. For example, consider this scenario:
   1. The tester claims a certain command doesn't work.
   1. All your team members tried the exact same command and it works as advertised. What the h___ the tester is trying to pull here?
   1. In reality, the error is actually caused by a duplicate entry in the database resulting from a previous command; the tester didn't mention that command in the bug report (because s/he didn't realize the two are connected).
* The reported bug might be non-existent but the tester's screw up can indicate other areas to improve. For example, the tester reports a missing feature that is clearly mentioned as 'not implemented' in the UG, but perhaps the UG can be improved to make that fact harder to miss?
* What exactly about the bug report that makes you angry? Remind yourself not to do the same offence when you report bugs yourself in the future.

Use the pain of dealing with this kind of bug reports as an opportunity to develop the following mindset:

* **The product is _guilty until proven innocent_**: If the bug report has even a _hint_ of something amiss with the product, it's your (not the tester's) responsibility to try and prove if it is really a problem or not. Why? because finding a bug is a win for _you_ -- as you can then fix it and thereby avoid the embarrassment of releasing a buggy product.{ text="(a)" t-class="fw-bold" }

* **A crappy bug report is better than no bug report**: If the bug actually exists, it is better to have _some_ indication about it than none at all. In a real project, a tester that fails to find bugs can cause more harm to your career than a tester who finds bugs but doesn't report them well.{ text="(b)" }

* **I _used_ to get angry at bug reports, but not anymore**: If you work hard, take pride in the quality of your work, it's no wonder that you get angry when others find faults with your work incorrectly. Aim to move past that phase where you take bug reports personally. The sooner you can tackle any sh*tty bug report calmly and objectively, the sooner you'll rise to the 'professional' software engineer level.{ text="(c)" }
</box>
</div>


* **If you have received stray bug reports** (i.e., bug reports that seems to be about a different project), do let us know ASAP (write to the course email).
* **Aim to ==do a systematic triaging of issues received==**. Some suggestions:
  * Close duplicate issues.
  * Use labels (create new labels if necessary) to,
    * differentiate _bugs_ from the rest (e.g., feature suggestions/flaws).
    * indicate priority of the bugs that need fixing.
  * Assign each bug to the person who should fix it.
* **You may ignore `type/severity.*` labels given by the tester.** They will not affect you or the tester either way -- they were there just for the testers to practice. You may apply your own type/severity labels if you wish.<br>
  {{ icon_important_big_red }} In particular, beware of simply following the `type.*` given by the tester; it is your job to decide the correct type of the issue. e.g., What the tester labeled as a _bug_ might actually be a _feature flaw_.{% if cs2103 %}
* **If a bug report is simply a feature suggestion**, you can take note of it and close it (to reduce clutter in the issue tracker, and to make it easy for the teaching team to track your progress on dealing with PE-D issues). Similarly, you can close PE-D issues not relevant to {{ version_final }}.{% endif %}


<box type="wrong" seamless>

**Note that listing bugs as 'known bugs' in the UG or specifying _unreasonable_ constraints in the UG to make bugs 'out of scope' will not exempt those bugs from the final grading.** That is, PE testers can still earn credit for reporting those bugs and you will still be penalized for them.<br>
 However, a product is allowed to have 'known limitations' %%(e.g., a daily expense tracking application meant for students is unable to handle expenses larger than $999)%% as long as they don't degrade the product's use within the intended scope. They will not be penalized.
</box>
<box type="info" tags="m--cs2103" seamless>

**Even bugs inherited from AB3 need to be fixed.** As mentioned in a previous week, even bugs you inherited from AB3 need fixing %%(because "we inherited it from the previous dev team" is not a valid excuse to leave a bug unfixed)%%. If you are unsure if something is such a bug that need fixing, please post in the forum.
</box>
<box type="tip" seamless>

**Identify bugs you missed in the PE-D:** Visit the issue tracker of the team you tested and see bugs reported by others who tested the same product. Identify bugs you missed (if any). That knowledge might help you find similar bugs in your own product as well as find more bugs during the PE.
</box>
</span>
