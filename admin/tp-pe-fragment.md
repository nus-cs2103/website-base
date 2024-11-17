{% from "common/macros.njk" import embed_topic, get_date, show_faq with context %}

#### <span class="badge bg-success">PE</span> <span class="text-success">Overview</span>

<div id="pe-overview">

* **PE is not entirely a pleasant experience, but is an essential component** that aims to increase the quality of the tP work, and the rigor of tP grading.
<div class="indented-level1">
<panel header="more details on the motivation and objectives..." minimized>

* **The upfront objective of the PE is to increase the rigor of project grading.** Assessing most aspects of the project involves an element of subjectivity. As the project counts for a large percentage of the final grade, it is not prudent to rely on evaluations of tutors alone as there can be significant variations between how different tutors assess projects. That is why we collect more data points via the PE to minimize the chance of your project being affected by evaluator-bias.
* **PE also evaluates your testing skills**, done as the following two-parts:
  1. **You will be given a chance to find bugs in a different software.** Furthermore, you will be given an opportunity to ~~defend your bug reports against any possible objections~~ interact with the developers (anonymously) to refine the bug report further %%e.g., correct the severity level if the level you chose initially was incorrect%%. If you report possible bugs that turn out to be actual bugs, you earn marks (provided the product actually had bugs in the first place).
  2. **Your product will be subjected to a rigorous testing** and you will be given a chance to point out any inaccuracies in the bugs reported. You will lose marks for any bugs that turned out to be real bugs, but only if your work has more bugs than a certain bar.
* **The above two can lead to high-rigor, <tooltip content="based on how well you achieve the objectives of testing, as opposed to indirect measures such as number of test cases">_outcome-based_</tooltip> evaluation of your testing skills**. The alternative is to rely solely on other easy-to-measure metrics %%(e.g., the number of test cases, test coverage, test LoC etc.)%% which we don't think as good representations of your actual testing skills.
**The _ultimate_ objective of the PE is not even the higher rigor of grading.** Because of the PE, you will realize that any bugs are very likely to be detected, which means you will work extra hard to avoid bugs; and THAT is the real benefit. Ultimately, <span class="text-success">**what we want is for you to internalize a higher standard for testing and a lower tolerance for bugs in your own code**</span> -- something that can have a longer-lasting impact on your future careers, beyond the mere course grade.
* **Problem: There is no way we can carry out the above-mentioned** two-part evaluation at a high-level of rigor if using tutors as testers, or using an automated testing script. %%e.g., some tutors might not have the motivation to try hard enough to find bugs, and it will be hard to find tutors willing to spend many hours testing products so near to their own exams.%%<br>
  **Solution: Get the two parts of the evaluation to feed each other** by getting student to test each other's products.
* **The fact that you are testing products created by your classmates and objecting to bugs reported by your classmates can make this a rather 'unpleasant' experience**. You might feel like _being pitted against each other_, or as if _you are forced to bring down each other_. But as you read above, it is a necessary evil for this evaluation to be even possible. Given the actual goal is to get you to create products with very few bugs, we think switching off the 'collaborative learning' mode for just a few days is a price worth paying to achieve that goal. After all, the PE is an evaluation activity (not a _learning activity_) and happens _after_ the regular learning period is over.
* **You are not taking marks from someone else** -- at least, don't think of it that way. The point of contention is 'is this really a bug?' which is independent of the people involved. Furthermore, the reward for detecting a bug and the penalty for having a bug in your code are calculated independently.
* **Still, _none of us_ likes it when others point out problems of our work**. Some of us don't even like pointing out problems of others' work. But ==we just have to learn not to take bug reports personally==. Another important intended outcome is to be able to report bugs in a way that doesn't feel like you are _attacking_ or trying to _sabotage_ the dev team.
* **PE also evaluates aspects other than testing** e.g., your product evaluation skills, effort estimation skills etc. When evaluating those aspects in particular, they are ==not graded solely based on peer ratings==. Rather, PE data are cross-validated with tutors' grades to identify cases that need further investigation. When peer inputs are used for grading, they are usually combined with tutors' grades with appropriate weight for each. In some cases ratings from team members are given a higher weight compared to ratings from other peers, if that is appropriate.
</panel><p/>
</div>

* **The PE is divided into four phases**:
  * ****Phase 1: Bug Reporting****{.text-success}: <span id="pe-p1-desc">In this phase, you will test the allocated product and report bugs, similar to PE-D. This phase is divided further into parts I, II, and III (done during the lecture slot), and part IV (done the day after the PE slot).</span>
    * <span class="badge bg-success">Phase 1 - part I</span> **Product Testing** [60 minutes] -- to focus on reporting bugs in the product (but can report documentation bugs too)
    * <span class="badge bg-success">Phase 1 - part II</span> **Evaluating Documents** [30 minutes] -- to focus on reporting bugs in the UG and DG (but can report product bugs too)
    * <span class="badge bg-success">Phase 1 - part III</span> **Overall Evaluation** [15 minutes] -- to give overall evaluation of the product, documentation, effort, etc.
    * <span class="badge bg-success">Phase 1 - part IV</span> **Trimming Bugs** [~half a day] -- For testers to select up to 7 bugs to send to the dev team.
  * ****Phase 2: Developer Response****{.text-success}: <span id="pe-p2-desc">This phase is for you to respond to the bug reports you received. Done during Sun-Mon after PE </span>
  * ****Phase 3: Tester Response****{.text-success}: <span id="pe-p3-desc">In this phase you will receive the dev teams response to the bugs you reported, and will give your own counter response (if needed). Done during Tue-Thu after PE</span>
  * ****Phase 4: Tutor Moderation****{.text-secondary}: <span id="pe-p4-desc">In this phase tutors will look through all dev responses you objected to in the previous phase and decide on a final outcome. Students are not usually involved in this phase.</span><br><br>

* **Grading**:
  * Your performance in the practical exam will affect your final grade and your peers', as explained in [_Admin: Project Grading_]({{ baseUrl }}/admin/tp-grading.html) section.
  * As such, we have put in measures to identify and ==penalize insincere/random evaluations==.
  * Also see:

{{ embed_topic("tp-grading-bugs-fragment.md#bugCalculationNotes", "Admin " + icon_embedding + " tP Grading → Notes on how marks are calculated for PE", "3", indent="2") }}

</div>

------------------------------------------------------------------------------------ {.thick-2 .border-success}

<div id="pe-preparation">

#### <span class="badge bg-success">PE</span> <span class="text-success">Preparation, Restrictions</span>

<div id="pe-mode-info">

* **Mode: you can choose between remote or F2F** (we'll use a Canvas survey to collect your preferred mode):
  * **Remote mode**: This is the ==recommended mode==. Proctored via Zoom. You'll need to join the Zoom session from a quiet place (i.e., conducive to an exam) at which you can set up a Zoom device for proctoring.<br>
    Choose this mode only if you are able to comply with the Zoom proctoring requirements given further down.
  * **F2F mode**: Attend the PE at the lecture venue ({{ lecture_venue }}).<br>
    Choose only if you are unable to use the remote mode (reason: higher the number of F2F attendees, higher the risk of Wi-Fi speed issues and GitHub throttling issues).
</div>

* **Those opting for the F2F mode can ignore any Zoom-related points** in the instructions below.

* **When**: ==Last lecture slot of the semester== ({{ get_date(date_w13_start, 4, format=format_normal, time="") | trim }}).

{{ show_faq("tpPeEndTime") }}

* **PE Phase 1 will be conducted under exam conditions. For the remote mode, ==we will be following the [SoC's E-Exam SOP](https://mysoc.nus.edu.sg/academic/e-exam-sop-for-students/)==**, combined with the deviations/refinements given below. Any non-compliance will be dealt with similar to a non-compliance in the final exam.<br>


<div id="pe-proctoring-info">

* **Remote mode proctoring will be done via Zoom.** No admission if the following requirements are not met.{% if cs2103 %}
  * **You need two Zoom devices** (PC: chat, audio ~~video~~, Phone: video, ~~audio~~), unless you have an external webcam for your PC.
  * {{ icon_tip }} To change the Zoom display name as required by the PE, join the Zoom call, go to the 'Participation' panel, and search for yourself. Then, click on 'More', followed by 'Rename'.
  * **Add your `[PE_seat_number]` in front of the _first name_ of your Zoom display name**, in your Zoom devices. ==Seat numbers can be found in [here](https://docs.google.com/spreadsheets/d/e/2PACX-1vSUbcJpMC5OdJkr_K6VxDwAkkrwJsqAFSPwHmZq88EbOdAWIPMeYvDQDYOUEcsEYVwACmAz5hH0W0ZY/pubhtml?gid=0&single=true)== about 2 days before the PE. e.g.,
    * `[M18] John Doe` (`M18` is the seat number)
    * `[M18][PC] John Doe` (for the PC, if using a phone as well){% elseif cs2113 %}
  * You will be ==notified of the zoom session== that you should log in at least 1 day in advance via Canvas. ==**Remember: we will NOT use the same zoom session as the lectures**==
  * **You need two Zoom devices** (PC: chat, audio ~~video~~, Phone: video, ~~audio~~), unless you have an external webcam for your PC.
  * Set your zoom display name to show your actual name as shown on Canvas.
  * **Add `[PC]` in front of the _first name_ of your zoom display name on the pc**.
    * E.g., `John Doe` (for the zoom session connected via the phone)
    * `[PC] John Doe` (for the zoom session on PC){% endif %}
  * **Set your camera** so that _all_ the following are visible:
    1. your face (side view, ==no mask==)
    1. your hands
    1. the work area (i.e., the tabletop)
    1. the computer screen<br>
    <pic eager src="images/zoomCameraExample.png" width="362"></pic>

</div>

* **Strongly recommended to join the Zoom waiting room ==15-30 minutes before the start time==.** Admitting you to the Zoom session can take some time. You need to be in the meeting and ready to start the PE by 4.05pm{% if cs2103 %}<br>
  **If on F2F mode:** Strongly recommended to arrive at lecture venue ({{ lecture_venue }}) around 10-15 minutes early. We can allow only 5 minutes (i.e., until 4.05pm) for you to get ready to start the PE.{% endif %}
* **In case of Zoom outage**, we'll fall back on MS Teams (MST).{% if cs2103 %} Make sure you have MST running and have joined the [MST Team for the class]({{ url_ms_teams_class }}).{% elseif cs2113 %} Make sure you have MST running; proctoring will be done via individual tutorial MST teams that we have been using.{% endif %}
* **Recording the screen is not required.**
* **You are allowed to use head/ear phones.** But no talking allowed (unless you are talking to the invigilator) -- so, no talking/singing to yourself as this can be mistaken for a rule violation.
* **==Only one screen== is allowed** (for both remote mode and F2F mode). If you want to use the secondary monitor, you should switch off (or cover up) the primary monitor. The screen being used should be fully visible in the Zoom camera view.<br>
  If using a second device for Zoom proctoring, the screen of that device should only be used for Zoom.
* **Do not use the public chat channel to ask questions** from the prof. If you do, you might accidentally reveal which team you are testing.
* **Do not use more than one CATcher instance** at the same time. Our grading scripts will red-flag you if you use multiple CATcher instances in parallel.
* **Use MS Teams (not Zoom) private messages to communicate with the prof.**{% if cs2103%} Zoom sessions are invigilated by tutors, not the prof.{% endif %}
* **Do not view video Zoom feeds of others** while the testing is ongoing. Keep the video view minimized.
* **Bug reporting will be done using CATcher**, similar to,
<div class="indented-level1">

<panel type="primary" header="PE-D Preparation" minimized>

<include src="tp-testing-fragment.md#testingPreparations" var-pe_active_tab="1"/>
</panel>
</div>
<p/>

* **During the bug reporting periods (i.e., <span class="badge bg-success">PE Phase 1 - part I</span> and <span class="badge bg-success">PE Phase 1 - part II</span>), do not use websites/software not in the list given below.** If you need to visit a different website or use another software, please ask for permission first.
  * Website: Canvas
  * Website/software: MSTeams (only to communicate with the prof of Tech support)
  * Website: Course website %%(e.g., to look up PE info)%%
  * Software: CATcher
  * Software: any screen grab/recording software
  * Software: PDF reader %%(to read the UG/DG or other references such as the textbook)%%
  * Software: A text editor or word processing software %%(to keep notes while testing)%% -- use a simple text editor that doesn't have online collaboration features
* **Do not visit GitHub** unless you are visiting the team's GitHub page to find an information needed for testing.
* **Do not use any other software running** in the background e.g., Telegram chat.
* **This is a _manual_ testing session**. Do not use any test automation tools or custom scripts.
* **You may use any digital/physical notes** during the PE %%e.g., a list of things to check%%.
* **Recommended to read the guidelines the dev team will follow when responding to your bug reports later**, given in the panel below. This will help decide what kind of bugs to report.
* **Bugs reported during the PE should be the result of your own testing**. <span class="text-danger">Reporting bugs found by others as your own will be reported as a case of academic dishonesty</span> (severity is similar to cheating during the final exam).
<div class="indented-level1">
<panel type="info" header="Guidelines for the dev team to follow when triaging PE bugs" peek>

<include src="tp-pe-bug-triaging-guidelines-fragment.md"/>
</panel>
</div>
<p/>

* **[Within 24 hours prior to the PE] Get CATcher 'warmed-up' for the PE**.<br>
  ==Strongly recommended== to do the following about a day in advance, so that there is enough lead time to sort out any CATcher-related problems _before_ the PE.
  1. Login to [CATcher](https://catcher-org.github.io/CATcher/),
while choosing the `{{ course_pair }} PE` as the session.
  1. Allow CATcher to create a repo named `pe`, when asked.
  1. Create a dummy bug report. Edit it. Delete it.<br>
     Caution: Do not reuse these dummy bug reports (i.e., by editing them later) to submit real PE bugs.
     As they were created outside the PE duration, they will be ignored by PE bug processing scripts.
  1. If you encounter any problems, post in the [CATcher issue tracker](https://github.com/CATcher-org/CATcher/issues).
</div>

------------------------------------------------------------------------------------ {.thick-2 .border-success}

<div id="pe-phases">

#### <span class="badge bg-success">PE</span> <span class="text-success">Phase 1: Bug Reporting</span>

<include src="tp-pe-fragment.md#pe-p1-desc" inline /><p/>

-------------------------------------------------------------------------{.border-success}

#### <span class="badge bg-success">&rarr; PE Phase 1 - Part I</span> <span class="text-success">Product Testing [60 minutes]</span>

**Test the product and report bugs** as described below. You may report both product bugs and documentation bugs during this period.

<include src="tp-ped-fragment.md#tp-pe-testing-instructions" var-pe_active_tab="1"/>


**There will be a _mass identity check_** during this part of the PE:

<box type="info" header="**Mass identity check**" seamless id="identity-check-info" tags="m--cs2103">

When the invigilator announces an identity check,

1. remove mask (if any)
1. turn towards the camera
1. move closer to the camera (but do not adjust the camera position) -- no need to show the student card
1. hold that pose until the invigilator has taken a screenshot and asks you to go back to the PE activity.

<span class="text-danger">Please comply quickly</span> as non-compliance can delay the PE for everyone. This is expected to take no more than 15 seconds.
</box>

{{ show_faq("tpTestingLessBuggyProducts", is_compact="1") }}
{{ show_faq("tpNoBugsInTestedProduct", is_compact="1") }}
{{ show_faq("tpNeedToFindAllBugs") }}

-------------------------------------------------------------------------{.border-success}

#### <span class="badge bg-success">&rarr; PE Phase 1 - Part II</span> <span class="text-success">Evaluating Documents [30 minutes]</span>

* **Use this slot mainly to report documentation bugs** (but you may report product bugs too). You may report bugs related to the UG and the DG.<br>
  Only the content of the UG/DG PDF files (not the online version) should be considered.
* **For each bug reported, cite evidence and justify.** For example, if you think the explanation of a feature is too brief, explain what information is missing and why the omission hinders the reader.<br>
  Do not report bugs that are not contained within in the UG and DG pdf files (e.g., bugs in the `README.md`).

{{ embed_topic("tp-grading-bugs-fragment.md#ugBugs", "Admin " + icon_embedding + " tP Grading → **Possible UG Bugs**", "3", indent="1") }}
{{ embed_topic("tp-grading-bugs-fragment.md#dgBugs", "Admin " + icon_embedding + " tP Grading → **Possible DG Bugs**", "3", indent="1") }}
<p/>

* **You _may_ report grammar issues** as bugs but note that minor grammar issues that don't hinder the reader are allowed to be categorized as `response.NotInScope` (by the receiving team) -- such bugs earn only small amount or credit for the tester (hence, do not waste time reporting too many minor grammar errors).

-------------------------------------------------------------------------{.border-success}

#### <span class="badge bg-success">&rarr; PE Phase 1 - Part III</span> <span class="text-success">Overall Evaluation [15 minutes]</span>

* To be submitted via TEAMMATES. You are expected to complete this during the PE session itself, but ==you have until the end of the day to submit (or revise) your submissions==.<br>
  **If you have a valid reason to leave the PE early** (e.g., having another exam right after the PE), you may leave after part II has ended and do part III later -- but note that if you fail to submit this by the hard deadline (i.e., end of the day), you will receive an <span class="text-danger">automatic penalty</span>.
* The TEAMMATES email containing the submission link should have reached you the day before the PE. If you didn't receive it by then, you can request it to be resent from [this page](https://teammatesv4.appspot.com/web/front/help/session-links-recovery).
* **If TEAMMATES submission page is slow/fails to load** (all of you accessing it at the same time is likely to overload the server), wait 3-5 minutes and try again. <span class="text-danger">Do not refresh the page repeatedly</span> as that will overload the server even more, and recovery can take even longer.

<div class="indented">
<panel header="##### Important questions included in the evaluation" peek>

<div id="projectGrading-featureFit-instructions">

{{ icon_green_Q }} **Quality of the product design,**<br>
Evaluate based on the User Guide and the actual product behavior.

 Criterion | Unable to judge | Low | Medium | High
-----------|-----------------|-----|--------|-----
`target user` | Not specified | | | Clearly specified and narrowed down appropriately
`value proposition`| Not specified | The value to target user is low. App is not worth using | Some small group of target users might find the app worth using | Most of the target users are likely to find the app worth using
`optimized for target user` | | Not enough focus for CLI users | Mostly CLI-based, but cumbersome to use most of the time | Feels like a fast typist can be more productive with the app, compared to an equivalent GUI app without a CLI
`feature-fit` | | Many of the features don't fit with others | Most features fit together but a few may be possible misfits | All features fit together to for a cohesive whole
</div>
<p/>
<div id="projectGrading-userGuide-instructions">

{{ icon_green_Q }} **Compared to AddressBook-Level3 (AB3), the overall quality of the UG you evaluated is,**<br>
Evaluate based on fit-for-purpose, from the perspective of a target user.
For reference, the AB3 UG is [here]({{ url_ab3_upstream_website }}/UserGuide.html).<br>

- ( )  Significantly lower
- ( )  Slightly lower
- ( )  Similar
- ( )  Higher

</div>
<p/>
<div id="projectGrading-devGuide-instructions">

{{ icon_green_Q }} **Compared to AB3, the overall quality of the DG you evaluated is,**<br>
Evaluate based on fit-for-purpose from the perspective of a new team member trying to understand the product's internal design by reading the DG.
For reference, the AB3 DG is [here]({{ url_ab3_upstream_website }}/DeveloperGuide.html).<br>

- ( )  Significantly lower
- ( )  Slightly lower
- ( )  Similar
- ( )  Higher

</div>
<p/>
<div id="projectGrading-effort-instructions">

<div tags="m--cs2103">

{{ icon_green_Q }} **If the implementation effort required to create AB3 from scratch is 10, the estimated implementation effort of this team is,** [`0`..`20`] e.g., if you give `5`, that means the team's effort is about 50% of that spent on creating AB3. We expect most typical teams to score near to `5`.
* Do read the DG appendix named `Effort`, if any.
* ==Consider implementation work only (i.e., exclude testing, documentation, project management etc.)==
* Do not give a high value just _to be nice_. ==Your responses will be used to evaluate your effort estimation skills.==
* Do ==not consider the team size== when deciding this rating. We'll factor in the team size later.
</div>
<div tags="m--cs2113">

{{ icon_green_Q }} **[For each member] The functional code contributed by the person is,**<br>
==Consider implementation work only (i.e., exclude testing, documentation, project management etc.)==<br>
The _typical iP_ refers to an iP where all the requirements are met at the minimal expectations given.<br>
Use the person's PPP and RepoSense page to evaluate the effort.

- ( )  Unable to judge
- ( )  Significantly less than a typical iP
- ( )  Slightly less than a typical iP
- ( )  At least as much as a typical iP
</div>

</div>

{{ icon_green_Q }} **[Optional] Concerns or any noteworthy observations about the product you evaluated**

<div tags="m--cs2103">

{{ icon_green_Q }} **Finally, what did you like about the product you tested?**
</div>

</panel>
<p/>
</div>

-------------------------------------------------------------------------{.border-success}

#### <span class="badge bg-success">&rarr; PE Phase 1 - Part IV</span> <span class="text-success">Trimming bugs</span>

**This segment gives testers a second chance revisit their bug reports, and choose upto 7 bugs that they wish to send to the dev team.** They will be allowed to change bug type/severity too (but will not be allowed to change bug title or the description).

**Objectives:**
  * To give testers a chance to correct their type/severity choices in case they chose incorrectly during the PE due to time pressure.
  * To filter out lower-impact (or low-confidence) bugs so that there is less work for the dev team during the next phase.

**Deadline:** Saturday 23:59

<box type="tip" seamless>

**Bonus marks for high accuracy rates!**{.text-success}

You will receive bonus marks if a high percentage (e.g., some bonus if >50%, a substantial bonus if >70%) of your bugs are _**accepted as reported**_ (i.e., the eventual `type.*` and `severity.*` of the bug match the values you chose initially and the bug is accepted by the team).
</box>

****Procedure:****

1. **Wait for the announcement** declaring this part of the PE to be open -- expected to be Friday night or Saturday morning.
1. **Open CATcher** as before (i.e., go to [CATcher Web app](https://catcher-org.github.io/CATcher/), and login to the profile `{{ course_pair }} PE`).
1. **Revise severity and bug type** of your bug reports as you see fit.
   * {{ icon_important_big_red }} #r#Do not change the title or the description.##<br>
     What if I updated the title/description by mistake? Not to worry, they will be reverted to the previous version (i.e., as at the end of part II) by our processing script.
   * =={{ icon_tip }} **When in doubt, choose the lower severity:**== If the severity of a bug seems to be smack in the _middle_ of two severity levels, choose the lower severity (unless much closer to the higher one than the lower one).
     * Reason: The teaching team follow the same policy when adjudicating disputed severity levels in the last phase of the PE.
     * As the tester, you might feel like you are throwing away marks by choosing a lower priority; but the lower priority has a lower risk of being disputed by the dev team, giving you (and the dev team) a better chance of earning bonus marks for accuracy.
1. **Decide which bugs should be sent to the dev team**. You may select ==no more than 7==.<br>
   **Of these bugs, ==the highest scoring 5 bugs will be used for your tP grading==.** %%We allow you to select up to 7 bugs (instead of 5), to reduce your decision-stress (i.e., one or two wrong choices will not affect your marks).%%
   * **Choose based on,**<br>
     * **severity** -- %%because higher severity will earn higher marks.%% {{ bullet_tick_green }}
     * **confidence** level that it is indeed a bug %%-- if the bug is eventually rejected, it will not earn any marks.%%
     * **but not bug type** -- for this purpose, consider all bug types as equal. {{ bullet_x_red }}
1. **Delete the remaining bug reports** using CATcher.
   * What if I deleted a bug that I intended to keep? When you 'delete' a bug using CATcher, the corresponding issue is closed (but not deleted) in GitHub issue tracker. So, the deleting can be reversed by going to GitHub and re-opening that issue.
   * What if I keep more than 7 bugs? In that case, we take the 7 bugs with the highest severity. When choosing between two bugs with same severity, we take the bug that was created earlier (i.e., the one with a lower issue number).

------------------------------------------------------------------------------------ {.thick-2 .border-success}

#### <span class="badge bg-success">PE</span> <span class="text-success">Phase 2: Developer Response</span>

<include src="tp-pe-fragment.md#pe-p2-desc" inline /><p/>

==**Deadline:** {{ get_date(date_w13_start, 7 if S == 2 else 7) }}==

<box type="important" >

****Yes, that can be better!**** For each bug report you receive, if you think a software engineer who takes pride in their own work would say "yes, that can be better!", accept it graciously, even if you can come up with _some_ BS argument to justify the current behavior. <br>
  Even when you still want to defend the current behavior, instead of pretending that the behavior was a deliberate choice to begin with, you can say something like,
  > "Thanks for raising this. Indeed, it didn't occur to us. But now that we have thought about it, we still feel ..."

**_Some_ bugs are 'expected'.** Given the short time you had for the tP and your inexperience in SE team projects, this work is not expected to be totally bug free. The grading scheme factors that in already -- i.e., your grade will not suffer if you accept a few bugs in this phase.
</box>

<box type="tip" seamless>

**Bonus marks for high accuracy rates!**{.text-success}

You will receive bonus marks if a high percentage (e.g., some bonus if >60% substantial bonus if >80%) of bugs are _**accepted as triaged**_ (i.e., the eventual `type.*`, `severity.*`, and `response.*` of the bug match the ones you chose).
</box>

<box type="important" seamless>

**It's not bargaining!**{.text-danger}

When the tester and the dev team cannot reach a consensus, the teaching team will select either the dev team position or the tester position as the final state of the bug, whichever appear to be closer to being reasonable. <span class="text-danger">The teaching team will not come up with our own position, or choose a middle ground.</span>

Hence, do not be tempted to argue for an unreasonable position in the hope that you'll receive something less than asked but still in your favor e.g., if the tester chose `severity.High` but you think it should be `severity.Medium`, don't argue for `severity.VeryLow` in the hope that the teaching team will decide a middle ground of `severity.Low` or `severity.Medium`. It's more likely that the teaching team will choose the tester's position as yours seems unreasonable.

More importantly, this is not a bargaining between two parties; it's **an attempt to determine the true nature of the bug, and your ability to do so (which is an important skill)**.
</box>

<box type="tip" seamless>

==**Favor `response.NotInScope` over `response.Reject`**=={.text-success}

If there is even the slightest chance that the change directly suggested (or indirectly hinted at) by a bug report is an improvement that you *might* consider doing in a future version of the product, choose `response.NotInScope`.<br/>
 Choose `response.Reject` only for bug reports that are clearly incorrect (e.g., the tester misunderstood something).<br>
Accordingly, it is typical a team to have a lot more `response.NotInScope` bugs and very few `response.Reject` bugs.

Note that `response.NotInScope` bugs earn a small amount of credit for the tester without any penalty for the dev team, unless there is an unusually high number of such bugs for a team.
</box>

Bug reviewing is recommended to be done as a team as some of the decisions need team consensus.

<box>

**Instructions for Reviewing Bug Reports**

* **Don't freak out if there are a lot of bug reports.** Many can be duplicates and some can be _false positives_. In any case, we anticipate that all of these products will have some bugs and our penalty for bugs is not harsh. Furthermore, it depends on the severity of the bug. Some bug may not even be penalized.
* **Nit-picking is a good sign**: If you receive a lot of nit-picking type of bugs that make you roll your eyes, it means testers were unable to find more serious bugs. That's a good thing.
* **Not exactly zero-sum**: As mentioned earlier, the penalty for having a specific bug is not the same as the reward for reporting that bug (it's not a _zero-sum_ game). For example, the reward for testers will be higher (because we don't expect the products to have that many bugs after they have gone through so much prior testing)

<box type="info" seamless>

**Penalty for a minor bug (e.g., <tooltip content="an indicative value only; the actual value depends on the severity, type, and the number of assignees">-0.15</tooltip>) is unlikely to make a difference in your final grade**, especially given that the penalty applies only if you have more than a certain amount of bugs.<br>

For example, in a typical case a developer might be assigned 5+ `severity.VeryLow` bugs before the penalty even starts affecting their marks.

Accordingly, we hope you'll **accept bug reports graciously** (rather than fight tooth-and-nail to reject _every_ bug report received) if you think the bug is within the ballpark of 'reasonable'. Those minor bugs are really not worth stressing/fighting over.
</box>


<tabs>
<tab header="Using CATcher">

<box type="info" icon=":fas-hard-hat:">

* CATcher does not come with a UG, but the UI is fairly intuitive (there are tool tips too). Do post in the forum if you need any guidance with its usage.
* Tip: If you think others might be editing the same issues at the same time, use the `Sync` button at the top to force-sync your view with the latest data from GitHub.
</box>

* Go to [CATcher Web app](https://catcher-org.github.io/CATcher/), and login to the profile `{{ course_pair }} PE`. It will show all the bugs assigned to your team, divided into three sections:
  1. `Issues Pending Responses` - Issues that your team has not processed yet.
  1. `Issues Responded` - Your job is to get all issues to this category.
  1. `Faulty Issues` - e.g., Bugs marked as duplicates of each other, or causing circular _duplicate_ relationships. Fix the problem given so that no issues remain in this category.
* Respond to the bug reports shown.
</tab>
<tab header="Not using CATcher">
<div class="indented-less">

<div id="warning-use-catcher">

<box type="wrong">

**You must use CATcher. You are strictly prohibited from editing PE bug reports using the GitHub Web interface** as it can render bug reports unprocessable by CATcher, sometimes in an irreversible ways, and can affect the entire class. Please contact the prof if you are unable to use CATcher for some reason.
</box>
</div>

</div>
</tab>
</tabs>
<p/>

* **If a bug seems to be for a different product** (i.e. wrongly assigned to your team), let us know ASAP.
* **If the bug is reported multiple times**,
  * Mark <span class="text-danger">all copies ==EXCEPT one==</span> as duplicates of the one left out (let's call that one the _original_) using the :fas-check-square: `A Duplicate of` tick box.
  * For each group of duplicates, all duplicates should point to one _original_ i.e., no multiple levels of duplicates, and no cyclical duplication relationships.
  * If the duplication status is eventually accepted, all duplicates will be assumed to have inherited the `type.*` and `severity.*` from the _original_.
* **If you cannot reproduce the bug based on the info given by the tester** you are still expected to make a _reasonable attempt_ to go beyond the information provided by the tester to reproduce the bug, if there is clear evidence of something wrong.<br>
 For example, the screenshot in the bug report clearly shows an error message that should not appear, but you can't reproduce the error message based on the info given by the tester. Perhaps the error was caused by something else the tester did although the tester didn't realize it is connected to the error. In this case, based on the error message, you might be in a better position to figure out the real cause of the error. If you don't, the decision can go against you in a later phase if either the tester or the moderator figures out how to reproduce the error and the moderator decides that it is something you should have been able to figure out yourself.
<p/>

* **Apply one of these labels** (if missing, we assign: `response.Accepted`)

<div class="indented">
<box>

**Response** Labels:
* `response.Accepted`: You accept it as a valid bug.
* `response.NotInScope`: It is a valid issue, but fixing it is less important than the work done in the current version of the product %%e.g., it was not related to features delivered in {{ version_final }} or lower priority than the work already done in {{ version_final }}%%.
* `response.Rejected`: What tester treated as a bug is in fact the _expected_ and _correct_ behavior (from the user's point of view), or the tester was mistaken in some other way. %%Note: Disagreement with the bug severity/type given by the tester is not a valid reason to reject the bug.%%
* `response.CannotReproduce`: You are unable to reproduce the behavior reported in the bug after multiple tries.
* `response.IssueUnclear`: The issue description is not clear. Don't post comments asking the tester to give more info. The tester will not be able to see those comments because the bug reports are anonymous.

Only the `response.Accepted` bugs are counted against the dev team. While `response.NotInScope` are not counted against the dev team, they can earn a small amount of consolation marks for the tester. The other three do not affect marks of either the dev team or the tester, except when calculating bonus marks for accuracy.


</box>
</div>


* **If you disagree with the original bug type assigned to the bug**, you may change it to the correct type.

<div class="indented" id="type-labels">
<box>

**Type** labels:
* `type.FunctionalityBug`: A functionality does not work as specified/expected.
* `type.FeatureFlaw`: Some functionality missing from a feature delivered in {{ version_final }} in a way that the feature becomes less useful to the intended target user for _normal_ usage. i.e., the feature is not 'complete'. In other words, an acceptance-testing bug that falls within the scope of {{ version_final }} features.<br>
  These issues are counted against the _product design_ aspect of the project. Therefore, other design problems (e.g., low testability, mismatches to the target user/problem, project constraint violations etc.) can be put in this category as well.<br>
  Features that work as specified by the UG but _should have been designed to work differently_ (from the end-user's point of view) fall in this category too.
* `type.DocumentationBug`: A flaw in the documentation %%e.g., a missing step, a wrong instruction, typos%%
</box>
</div>

**If a bug fits multiple types _equally_ well**, the team is free to choose the one they think the best match, but keep the type chosen by the tester if it is one of the types that fits the bug equally well.

* **If you disagree with the original severity assigned to the bug**, you may change it to the correct level.

<div class="indented">
<include src="appendixE-gitHub.md#bug-severity" />
</div>

* **If you need the teaching team's inputs when deciding on a bug** %%(e.g., if you are not sure if the UML notation is correct)%%, post in the [forum]({{ url_forum }}). Remember to ==quote the issue number shown in CATcher== (it appears at the end of the issue title).<br/>
  Keep in mind that the bug triaging accuracy affects your marks, and therefore, the teaching team prefers not to dictate a specific response, type, or severity for a particular bug report (i.e., that decision should be yours). Nevertheless, we can provide some general comments relevant to the issue at hand. Additionally, we encourage other students to chime in with their opinions, as such discussions have learning value.

<div class="indented-level1" id="additionalGuidelinesForBugTriaging">

<panel type="info" header="##### Guidelines for bug triaging" expanded>
<include src="tp-pe-bug-triaging-guidelines-fragment.md" />
</panel>
<p/>
</div>

* **Decide who should take responsibility for the bug**. Use the `Assignees` field to assign the issue to that person(s). There is no need to actually fix the bug though. It's simply an indication/acceptance of responsibility. The penalty for the bug (if any) will be divided among the assignees %%e.g., if the penalty is -0.4 and there are 2 assignees, each member will be penalized -0.2%%.
  * If it is not easy to decide the assignee(s), we recommend (but not enforce) that the feature owner should be assigned bugs related to the feature, Reason: The feature owner should have defended the feature against bugs using automated tests and defensive coding techniques.
  * It is also fine to not assign a bug to anyone, in which case the penalty will be divided equally among team members.
<p/>

* As far as possible, ==**choose the correct `type.*`, `severity.*`, `response.*`, assignees, and duplicate status even for bugs you are not accepting**==. Reason: your _non-acceptance_  may be rejected in a later phase, in which case we need to grade it as an accepted bug.<br>
  **If a bug's 'duplicate' status was rejected later** %%(i.e., the tester says it is not really a duplicate and the teaching team agrees with the tester)%%, it will inherit the response/type/severity/assignees from the 'original' bug that it was claimed to be a duplicate of.

* **Justify your response.** For all the following cases, ==you must add a comment justifying your stance==. Testers will get to respond to all those cases and will be considered by the teaching team in later phases (when resolving disputed bug reports).<br>
  {{ icon_important_big_red }} If you don't provide a justification and the tester disagrees with your decision, the teaching team will have no choice but to rule in favor of the tester.
  * downgrading severity
  * non-acceptance of a bug
  * changing the bug type
  * non-obvious duplicate

{{ show_faq("tpJustifyBugsAcceptedAsIs") }}
{{ show_faq("tpMoreCodeMeansHigherPenalty") }}
{{ show_faq("tpRealBugWrongLabel") }}
{{ show_faq("tpCorrectBugIncorrectSuggestion") }}
<p/>
</box>

* You can also refer to the below guidelines:

{{ embed_topic("tp-grading-bugs-fragment.md#bugCalculationNotes", "Admin " + icon_embedding + " tP Grading → Grading bugs found in the PE", "pe-gradingBugsFoundInPe", indent=1) }}

------------------------------------------------------------------------------------ {.thick-2 .border-success}

#### <span class="badge bg-success">PE</span> <span class="text-success">Phase 3: Tester Response</span>

<include src="tp-pe-fragment.md#pe-p3-desc" inline /><p/>

**Start:** Within 1 day after Phase 2 ends.<br>

<div class="indented">

{{ icon_important_big_red }} While you are waiting for Phase 3 to start, comments will be added to the bug reports in your `/pe` repo, to indicate the response each received from the receiving team. <span class="text-danger">Please do not edit any of those comments or reply to them via the GitHub interface.</span> Doing so can invalidate them, in which case the grading script will assume that you agree with the dev team's response. Instead, wait till the start of the Phase 3 is announced, after which you should use CATcher to respond.
</div>

==**Deadline:** {{ get_date(date_w13_start, 10) }}==

* In this phase you will get to state whether you agree or disagree with the dev team's response to the bugs you reported. If a bug reported has been subjected to any of the below by the dev team, you can record your objections and the reason for the objection.
  * not accepted
  * severity downgraded
  * bug type changed
  * bug flagged as duplicate %%(Note that you still get credit for bugs flagged as duplicates, unless you reported both bugs yourself. Nevertheless, it is in your interest to object to incorrect duplicate flags because when a bug is reported by more testers, it will be considered an 'obvious' bug and will earn slightly less credit than otherwise)%%

<div class="indented">
<box type="important">

**Don't feel upset if the dev team did not totally agree** with most of the bugs you reported. That is to be expected, given you had very short time to make those bug decisions while the dev team had a lot more time to deliberate about them. Some may have given unreasonable (in your opinion) arguments against your bug reports; not to worry, just give your counter-arguments and leave it to the teaching team to decide (in the next phase) which position is more reasonable.

However, ==if the dev team's argument is not too far from 'reasonable', **it may be better to agree than disagree**==.<br>
  Reason: an incorrect counterargument at this phase will lower your _accuracy_ more than an incorrect decision made during the testing phase (because you now have more time to think about the bug) i.e., changing your position after you had more time to think of it and after having seen more information is encouraged, compared to sticking to your initial position 'no matter what'.
</box>
</div>

* **If you would like to revise your own initial type/severity** in response to the team's inputs, you can state that in your explanation %%e.g., you rated the bug `severity.High` and the team changed it to `severity.Low` but now you think it should be `severity.Medium`%% (do not change the original labels yourself though).
* You can also refer to the below guidelines, mentioned during the previous phase as well:

{{ embed_topic("tp-pe-fragment.md#additionalGuidelinesForBugTriaging", "Admin " + icon_embedding + " PE → Phase 2 → Additional Guidelines for Bug Triaging", "pe-additionalGuidelinesForBugTriaging", indent=1) }}

{{ embed_topic("tp-grading-bugs-fragment.md#bugCalculationNotes", "Admin " + icon_embedding + " tP Grading → Grading bugs found in the PE", "pe-gradingBugsFoundInPe", indent=1) }}

* If the dev team disagreed with an aspect (i.e., type/severity/<tooltip content="i.e., accept vs not accept">validity</tooltip>) and you now agree with the dev team's position, it will not hurt your accuracy rating. Here are some examples (for the `severity.*`):

{% set up %}<span class="text-success">:fas-arrow-up:</span>{% endset %}
{% set down %}<span class="text-danger">:fas-arrow-down:</span>{% endset %}
<div class="indented-level1">

Tester choice | Dev choice | Tester reaction | Teacher decision | Dev accuracy  | Tester accuracy
----------|-----------------|---------------|---------------------|--------------------|--------------------
`High`    | agreed          |               |                     | {{ up }}           | {{ up }}
`High`    | `Low`           | agreed        |                     | {{ up }}           | no effect
`High`    | `Low`           | disagreed     | `High`              | {{ down }}         | {{ up }}
`High`    | `Low`           | disagreed     | `Low `              | {{ up }}           | {{ down }}
</div>

* If you do not respond to a dev response, we'll assume that you agree with it.
* Procedure:

<div class="indented-level2">

<tabs>
<tab header="Using CATcher">

* When the phase has been announced as open, login to [CATcher](https://catcher-org.github.io/CATcher) as usual (profile: `{{ course_pair }} PE`).
* For each issue listed in the `Issues Pending Responses` section:
  * Click on it to go to the details, and read the dev team's response.
  * If you disagree with any of the items listed, tick on the `I disagree` tick box and enter your justification for the disagreement, and click `Save`.
  * If you are fine with the team's changes, click `Save` without any other changes upon which the issue will move to the `Issue Responded` section.
* No action is required for the bugs the team accepted _exactly as you reported them_ (i.e., no change to type or severity). They are shown in CATcher for your reference only.

</tab>
<tab header="Not using CATcher">

<div class="indented-less">

<include src="tp-pe-fragment.md#warning-use-catcher" />
</div>
</tab>
</tabs>
</div>


{{ show_faq("tpTesterAddingMoreInfoLater") }}
{{ show_faq("tpBugRejectedWithReason") }}
<p/>

------------------------------------------------------------------------------------ {.thick-2 .border-success}

#### <span class="badge bg-success">PE</span> <span class="text-success">Phase 4: Tutor Moderation</span>

<include src="tp-pe-fragment.md#pe-p4-desc" inline />

</div>
