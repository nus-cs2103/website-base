{% from "common/macros.njk" import embed_topic, get_date with context %}

##### General:

* **Don't freak out if there are a lot of bug reports.** Many can be duplicates and some can be _false positives_. In any case, we anticipate that all of these products will have some bugs and our penalty for bugs is not harsh. Furthermore, it depends on the severity of the bug. Some bug may not even be penalized.
* **Nit-picking is a good sign**: If you receive a lot of nit-picking type of bugs that make you roll your eyes, it means testers were unable to find more serious bugs. That's a good thing.
* **Not exactly zero-sum**: As mentioned earlier, the penalty for having a specific bug is not the same as the reward for reporting that bug (it's not a _zero-sum_ game). For example, the reward for testers will be higher (because we don't expect the products to have that many bugs after they have gone through so much prior testing)

<box type="info" seamless>

**Penalty for a minor bug (e.g., <tooltip content="an indicative value only; the actual value depends on the severity, type, and the number of assignees">-0.15</tooltip>) is unlikely to make a difference in your final grade**, especially given that the penalty applies only if you have more than a certain amount of bugs.<br>

For example, in a typical case a developer might be assigned 5+ `severity.VeryLow` bugs before the penalty even starts affecting their marks.

Accordingly, we hope you'll **accept bug reports graciously** (rather than fight tooth-and-nail to reject _every_ bug report received) if you think the bug is within the ballpark of 'reasonable'. Those minor bugs are really not worth stressing/fighting over.
</box>

* **If you cannot reproduce the bug based on the info given by the tester** you are still expected to make a _reasonable attempt_ to go beyond the information provided by the tester to reproduce the bug, if there is clear evidence of something wrong.<br>
 For example, the screenshot in the bug report clearly shows an error message that should not appear, but you can't reproduce the error message based on the info given by the tester. Perhaps the error was caused by something else the tester did although the tester didn't realize it is connected to the error. In this case, based on the error message, you might be in a better position to figure out the real cause of the error. If you don't, the decision can go against you in a later phase if either the tester or the moderator figures out how to reproduce the error and the moderator decides that it is something you should have been able to figure out yourself.
* **If you need the teaching team's inputs when deciding on a bug** %%(e.g., if you are not sure if the UML notation is correct)%%, post in the [forum]({{ url_forum }}). Remember to ==give the URL of the issue== in your post.<br/>
  Keep in mind that the bug triaging accuracy affects your marks, and therefore, the teaching team prefers not to dictate a specific response, type, or severity for a particular bug report (i.e., that decision should be yours). Nevertheless, we can provide some general comments relevant to the issue at hand. Additionally, we encourage other students to chime in with their opinions, as such discussions have learning value.

* **If a bug report contains multiple bugs** (i.e., despite instructions to the contrary, a tester included multiple bugs in a single bug report), you have to choose one bug and ignore the others. If there are valid bugs, choose from valid bugs. Among the choices available, choose the one with the highest severity (in your opinion). In your response, mention which bug you chose.
* **If a bug report has broken image links**, check with the prof instead of rejecting them outright using the missing image as an excuse -- the missing image may be due to a technical problem in the PE issue transfer script.
* **What bugs can be considered duplicates?** It is up to the dev team to prove conclusively that a bug is a duplicate. If the proof is not convincing enough, they will be considered as 'not duplicates'. Only the following cases can be considered duplicates:<br>
  (a) The exact same bug reported multiple times.<br>
  (b) Multiple buggy behaviors that are actually caused by the same defect and ==cannot be fixed independently== (i.e., fixing one fixes the others automatically).<br>
  <br>
  In real projects, similar bugs (e.g., the same typo in multiple places) tend to get combined into a single issue/PR; in the PE, we have to keep independently-fixable things as separate bugs, to avoid complications in grading. After all, having the same typo in two places is not exactly the same as having it in only one place.<br>
  If an independently-fixable yet similar problem appears in more than five distinct places, get our permission to combine them as one bug (in which case we'll require you to increase the severity to match the frequency of the bug).

<div id="how-to-prove-out-of-scope">

* **How to prove that something is `response.NotInScope`**: In general, a flaw (e.g., a missing feature, a suboptimal design of a feature, a known bug) can be considered `NotInScope` ==if rectifying it is less important than the work that has been done already== (because it is fine to delay lower priority work until future iterations) %%i.e., the supposedly 'better' implementation will take more effort than the current implementation, reducing the effort available to spend on other more important tasks%%<br>
  In addition, the following (at least one) need to be satisfied:
  * The UG specifies it as not supported or coming in a future version.
  * The user cannot attempt to use the missing feature or when the user does so, the software fails gracefully, possibly with a suitable error message i.e., the software should not crash.

<div class="indented-level1">

{{ icon_info }} If a bug qualifies for `response.NotInScope`, the dev team will not be penalized, but the bug reporter will earn a small amount of credit for reporting it.{% if cs2103 %}

{{ icon_info }} If a bug matches an enhancement listed in the 'Appendix: Planned Enhancements' of the DG, that bug can be rejected (the tester should not have reported it at all).{% endif %}
</div>
</div>

* **Even bugs inherited from AB3 are counted**. As the current development team, you are responsible for all bugs in the product, irrespective of when it was created.

* **Listing something as a known issue** in the UG can reduce the severity of the issue %%(because informing users about the issues, possibly how to avoid/circumvent the issue reduces the impact of the issue to some extent)%% but that does not mean it is totally immune from being considered a bug.

<div id="triaging-functionality-bugs">

##### Functionality bugs

* **Problems caused by _extreme_ user behaviors**:
  * If the problem happens only in case of a deliberate sabotage %%(e.g., user entered a 30-digit telephone number)%%, it will not be considered a bug (in our context).<br>
However, if it is possible for a user mistake to cause such inputs %%(e.g., the user missed out typing the space between two parameters)%%, they should not cause harm e.g., such mistakes should not crash the app, corrupt the data, or make it unusable.
  * Problems caused by integer overflows -- apply the guideline in the previous point.
* **Problems caused by very long input values**: When a user input is unusually long %%e.g., a very long name, a very large number%%, it can cause problems e.g., the UI layout can get messed up, some part of it might get cut off.<br>
  * These can be considered cosmetic issues (i.e., `severity.VeryLow`) of `type.FunctionalityBug` (or of `type.FeatureFlaw`, depending on the nature of the problem).<br>
  However, if the problem can hinder the user %%(e.g., not seeing the last part of a very long name might not hinder the user, but it does hinder the user if only the first few characters of the name is shown)%%, the severity can be `Low` or higher.
  * It is also fine to restrict the size/length of inputs as long as the limits are reasonable. For example, limiting the phone number to 8 digits is not reasonable unless you are targeting users whose telephone numbers are _guaranteed_ to be not more than 8 digits.
* **Use of symbols in input values**: It is acceptable to disallow certain characters in input values if there is a justification (e.g., because using those symbols in an input value makes the command harder to parse), but they can still be considered `FeatureFlaw` bugs if they cause inconvenience to the user. For example, disallowing `s/o` in a person name because `/` is used as a command delimiter can cause a major problem if the input is expected to match the legal name of the person.
* **Mismatch between the UG and the feature**: If the feature behavior needs to be changed, it is either a `type.FunctionalityBug` or `type.FeatureFlaw`. But if it is the UG that needs to be updated, it is a `type.DocumentationBug`.{% if cs2103 %}
* **Issues with the output shown in the terminal**: While the terminal output is not critical to the functioning of the product, it is expected to 'behave' in a reasonably presentable manner e.g., avoid showing misleading or alarming information to the user who happens to glance at the terminal output. Therefore, issues related to the terminal can be classified at comparatively lower severities and might qualify to be `NotInScope`.
* **Handling manual edits to the data file**: AB3 UG specifies [the current level of support for manually editing the data file](https://se-education.org/addressbook-level3/UserGuide.html#editing-the-data-file) i.e., 'if you edit the file correctly, things will work; but if you edited it wrongly, there's no guarantee that things will work'. At least that level of support should be provided in the product as well. Bugs can be filed in the following cases:<br>
 (a) The product's support for editing the data files is less than that of AB3.<br>
 (b) The UG promises more support than AB3 but the product doesn't deliver that support.<br>
 (c) The data file format is not suitable for manual editing at all (it violates [Constraint-Human-Editable-File]({{ baseUrl }}/admin/tp-constraints.html#constraint-human-editable-file)).
{% endif %}

</div>
<div id="triaging-feature-flaws">

##### Feature flaws

<modal large id="modal:bugTriaging-whenOutOfScope">
<include src="tp-pe-bug-triaging-guidelines-fragment.md#how-to-prove-out-of-scope"/>
</modal>

* Missing features and problems in how a feature is designed are considered feature flaws i.e., `type.FeatureFlaw`.
* **Feature flaws can be claimed as `NotInScope`**, if they qualify as per <trigger trigger="click" for="modal:bugTriaging-whenOutOfScope">rules explained above</trigger>, except for these cases:
  * if fixing the feature flaw is essential for the app to be reasonably useful
  * if the feature is implemented to work in a certain way but it could have been implemented to work in a better way (from the end-user's point of view) without much additional effort
* **Bugs related to duplicate detection**: Duplicate detection (e.g., detecting if two persons in the address book are the same) is not trivial; often, detecting only the exact string/value matches is not enough. For example, `John Doe` and `john  doe` are likely to be the same person. Similarly, extra white space %%(e.g., the user typed an extra space between the two names)%% is unlikely to mean they are two different persons. Typically, it is best if you can give a warning in such _near match_ cases so that the user can make the final decision. <br>
  If you app has a duplicate detection feature, make sure its limitations are made clear to the user so that users are not led to believe that duplicates are being detected while many potential duplicate cases go undetected. Otherwise, it can be considered a `type.FeatureFlaw`.
* **Overzealous input validation**: This is a common problem in UIs designed by programmers, because programmers tend to define 'valid' in strict data type point of view, whereas it should be defined based on the user's point of view. In general, it is better to warn rather than to block when inputs are not compliant with the expected format, unless accepting such inputs can hinder the operations of the software. Allowing such flexibility can in turn allow the software to be used in ways you didn't even anticipate while overzealous rejection of inputs can annoy the user:<br>
  %%Example 1: While your software allows only one phone number in input values, a user might want to input `1234 5678 (HP) 1111-3333 (Office)` -- blocking that input might not add any value but allowing it does.%%<br>
  %%Example 2: A user might want to enter an appointment/deadline that occurred in the past, just for record keeping purposes (note how Google Calendar doesn't prevent users from creating events in the past -- instead, it shows the event in a lighter color to warn that it is in the past).%%<br>
  Such overzealous input blocking can be considered a `type.FeatureFlaw`.<br>
  However, it is fine (and recommended) to show a warning for such inputs to guard against the deviation being a mistake rather than intentional.<br>
  At the same time, the lack of proper handling (either blocking or warning) potentially harmful invalid inputs can be considered a `type.FeatureFlaw` bug too.
* **Specificity of error message**: Error messages can be correct but not specific enough %%(e.g., it says the input is 'invalid' without giving the reason, or gives too many possible reasons without pointing out the specific reason)%%. These cases can be considered `type.FeatureFlaw`.<br>
  Calling an invalid value a 'format error' and vice versa is a `severity.Low` bug e.g., if a date input is required to be in `YYYY-MM-DD` format, `2021-13-28` is a _format_ error (reason: `MM` should be in `1..12`) but `2021-02-30` is an _invalid_ input (reason: February doesn't have 30 days). However, issuing a 'Invalid date or incorrect format' error message for such a case (i.e., covering both bases) is acceptable if differentiating between the two qualifies as `NotInScope`.
* **Unnecessarily complicated (or hard-to-type) command formats** can be considered a `type.FeatureFlaw` as it is expected that the input formats will be optimized to get things done fast. Some examples: using very long keywords when shorter ones do, or making keywords case-sensitive when there is no need for it, using hard-to-type special characters in the format when it is possible to avoid them. On the other hand, limiting to short but hard-to-remember keywords can be problematic too. A better approach is to support both a short version (easier to type) and a longer (easier to remember) version for a keyword %%(an example from the Git world: flags `--no-verify` and `-n` are equivalent)%%.
* **Case sensitivity**: In general, case sensitivity of something should follow the case sensitivity of the real world entity it represents e.g., as person names are not case-sensitive in the real world, they shouldn't be case-sensitive in the app either. The same applies for search keywords. Incorrect case sensitivity can be considered a `FeatureFlaw`.
* **A features less useful than it can be** is a `FeatureFlaw`. Some examples related to search-related features:
  * If search keywords are case-sensitive, the user needs to remember the exact case of the words she is looking for. A case-insensitive search is usually more useful.
  * Applying an AND constraint on search keywords means the user will miss out potentially useful search results unless she remembers exactly the words she is looking for. But if an OR constraint is used, the user can retrieve results even if she mis-remembers some of the search terms %%(searching for `Alice` `Richards` can return both `Alice Davidson`, `Alison Richards` one of which is likely to be what the user was looking for)%%.
</div>


##### Documentation bugs
* **Broken/incorrect links**: Severity can be `Low` or `Medium` depending on how much inconvenience they cause to the reader.
* **Extra white space** introduced by the PDF conversion: Not counted as bugs unless it hinders the reader. Cases such as a diagram being split between pages are considered bugs, because they hinder the reader.<br>
  {{ icon_info }} **'Hinder' the reader?** Don't interpret 'hinder' as 'impossible to read'. Even formatting issues such as too much/little padding, font size, alignment, inconsistencies, etc. can 'hinder' the reader in the sense they can slow down the reader or require the reader to put more effort than necessary. Those things that 'need to be fixed' are still bugs but of lower severities (depending on how much they hinder the reader -- most likely `severity.VeryLow` if the issue is purely cosmetic).
* **UML notation variations** caused by the diagramming tool: Can be rejected if not contradicting the standard notation (as given by the textbook) i.e., extra decorations that are not misleading.<br>
  Omitting optional notations is not a bug as long it doesn't hinder understanding.
* **UML notation errors** %%(e.g., using dashed line where a solid line should be used)%%:<br>
  When deciding the severity, consider how much the notation error hinders the reader, but also keep in mind that notation errors hurt the credibility of the diagram (i.e., if even the notation is incorrect, how much can we trust this diagram :thinking:?). The latter pushes up the severity further than otherwise. So, the severity can be `Low` or higher.
* **Details missing from a diagram**: In a similar vein to the above, omitting details from a diagram is OK if it does not mislead/hinder the reader.<br>
  Forgetting to include something is not the same as a deliberate decision to omit something in order to simplify the diagram %%e.g., the latter could accompany a note to the reader to mention which/some parts have been omitted, _if_ it is worthwhile for the reader to know the omission.%%<br>
 While many UML notations are optional, haphazard omissions without a good reason can affect consistency which affects readability e.g., it can be considered a minor bug if a sequence diagram omits an activation bars in some places but not in other places and yet the omission doesn't make the diagram any easier to read.
* **Nitty-gritty details missing from the UG** is not a bug long as the user is informed of those details using other means such as error messages or in-app help.
* **Minor typos**: These are still considered as `severity.VeryLow` `type.DocumentationBug` bugs (even if it is in the actual UI) which carry a very tiny penalty.<br>
  As avoiding/correcting obvious typos does not take a significant extra effort, they should not have been postponed to a future version. {% if cs2103 %}Plus, correcting typos is allowed during the feature freeze. {% endif %}So, they don't qualify for `response.NotInScope`.
* **Minor grammar errors**: You may categorize a minor grammar bug as `severity.VeryLow` `type.DocumentationBug`. And, a grammar bug can be marked as `response.NotInScope` if it doesn't hinder the reader.
* **Severity of bugs related to _missing requirements_** (e.g., missing user stories)? Depends on the potential damage the omission can cause. Keep in mind that not documenting a requirement increases the risk of it not getting implemented in a timely manner (i.e., future developers will not know that feature needs to be implemented).
* **Unfulfilled NFRs**: If the DG mentions non-functional requirements that are not met by the product, it can be a `severity.Low` `DocumentationBug` if the NFR was unreasonable in the first place. Otherwise, it can be `type.FeatureFlaw` bug.
* **Details in the diagram too small**: This is usually a symptom of having too much info in the diagram. A common example is sequence diagrams showing low-level details of multiple components (recommended: A sequence diagram should show internal interactions of at most one component i.e., treat other components as black boxes).<br>
 While the reader can zoom to see smaller details, this can still be considered a cosmetic issue (i.e., `severity.VeryLow`).
* **Tester misunderstandings can be caused by inadequate documentation**. Some bug reports that arose from a tester misunderstanding something could be due to a flaw in the documentation e.g., something was not explained clearly enough in the document.
* **Undocumented features:**
  * If the said feature is not visible to the user and very unlikely for the user to detect it by accident, we can assume the feature was never meant to be released in the current version, which should be fine.
  * If the feature is simple, easily discoverable, and intuitive to use, it is fine to be omitted from the UG, especially if the inclusion seems adding noise rather than value.
  * Other cases point to some issue, either an omission in the UG, or a WIP feature not properly protected/hidden/disabled in the released product.
