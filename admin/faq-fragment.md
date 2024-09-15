{% from "common/macros.njk" import as_tag, embed_topic with context %}

<!-- =============================================================== -->
<div id="faq-whereIsEverything-Q">Where is everything?</div>
<div id="faq-whereIsEverything-A">

<p class="lead">The {{ url_schedule }} presents all you need to know in chronological order (for each week) while the other pages have some of the same content organized by topic.
</p>

The <span class="font-weight-bold">{{ url_schedule }}</span> is ==_the_ one page you need to refer weekly==. Although there is a lot of content in the <span class="font-weight-bold">{{ url_admin }}</span> and the [**Textbook page**]({{baseUrl}}/se-book-adapted/index.html) -- which you are welcome to read in those respective pages -- the same content is also cross-embedded in the corresponding weekly schedule pages. Such cross-embedded extracts usually appear in expandable panels and can be identified by the symbol {{ icon_embedding }} in the panel title.

</div>
<!-- =============================================================== -->
<div id="faq-tVsNonT-Q">What are the differences between CS2103T and CS2103?</div>
<div id="faq-tVsNonT-A">

Same content, same assessments, same exam. Separate tutorials, separate grading. Unless specified otherwise, whatever is stated for one course applies to the other.

</div>
<!-- =============================================================== -->
<div id="faq-aPlus-Q">What are the extra requirements to get an A+?</div>
<div id="faq-aPlus-A">

In {{ course_pair }}, A+ is not given simply based on the final score. To get an A+ you should,

* score enough to be close to the higher end of the `A` grade band.
* be considered technically competent by peers and tutor (based on peer evaluations and tutor observations).
* be considered helpful by peers (based on peer evaluations and tutor observations).
* In particular, you are encouraged to be active on the [forum]({{url_forum}}) and give your inputs to ongoing discussions so that other students can benefit from your relatively higher expertise that makes you deserve an A+.
* Whenever you can, go out of your way to review pull requests created by other team members.
</div>
<!-- =============================================================== -->
<div id="faq-beanCounting-Q">Why so much bean counting?</div>
<div id="faq-beanCounting-A">

<pic eager src="{{baseUrl}}/admin/images/small things matter.png" width="600" height="300"/>

Sometimes, small things matter in big ways. e.g., all other things being equal, a job may be offered to the candidate who has the neater looking CV although both have the same qualifications. This may be unfair, but that's how the world works. Students forget this harsh reality when they are in the protected environment of the school and tend to get sloppy with their work habits. That is why we reward all positive behavior, even small ones (e.g., following precise submission instructions, arriving on time etc.).

But unlike the real world, we are forgiving. That is why you can still earn full marks for participation even if you miss a few things here and there.
</div>
<!-- =============================================================== -->
<div id="faq-separateWebsite-Q">Why use a separate website instead of Canvas?</div>
<div id="faq-separateWebsite-A">

We have a separate website because some of the course information does not fit into the structure imposed by Canvas.
</div>
<!-- =============================================================== -->
<div id="faq-slideFormat-Q">Why slides are not detailed?</div>
<div id="faq-slideFormat-A">

<pic eager src="{{baseUrl}}/admin/images/slides not detailed enough.png" width="733" height="221"/>

Slides are not meant to be documents to print and study for exams (the textbook is the resource more suitable for exam prep). Their purpose is to support the {{ lecture_name_short }} delivery and keep you engaged during the {{ lecture_name_short }}. That's why our slides are less detailed and more visual.
</div>
<!-- =============================================================== -->
<div id="faq-narrowProjectScope-Q">Why very narrow project scope?</div>
<div id="faq-narrowProjectScope-A">

Defining your own unique project is more fun.

But, wider scope → more diverse projects → harder for us to go deep into your project. The collective know-how we (i.e., students and the teaching team) have built up about SE issues related to the project become shallow and stretched too thinly. It also affects fairness of grading.

<pic eager src="{{baseUrl}}/admin/images/limited project scope.png" width="772" height="296"/>

That is why a strictly-defined project is more suitable for a first course in SE that focuses on nuts-and-bolts of SE. After learning those fundamentals, in higher level project courses you can focus more on the creative side of software projects without being dragged down by nuts-and-bolts SE issues (because you already know how to deal with them). However, we would like to allow some room for creativity too. That is why we let you build products that are slight variations of a given theme.

Also note: **The freedom to do 'anything' is not a necessary condition for creativity**. Do not mistake being different for being creative. In fact, the more constrained you are, the more you need creativity to stand out.
</div>
<!-- =============================================================== -->
<div id="faq-favoriteTool-Q">Why can't I use my favorite tool/framework/language etc.?</div>
<div id="faq-favoriteTool-A">

<pic eager src="{{baseUrl}}/admin/images/I'm not allowed to use my favorite tool.png" width="750" height="287"/>

We have chosen a basic set of tools after considering ease of learning, availability, typical-ness, popularity, migration path to other tools, etc. There are many reasons for limiting your choices:

Pedagogical reasons:

* **Sometimes 'good enough', not necessarily the best, tools are a better fit for beginners**: Most bleeding edge, most specialized, or most sophisticated tools are not suitable for a beginner course. After mastering our toolset, you will find it easy to upgrade to such high-end tools by yourself. We do expect you to eventually (after this course) migrate to better tools and, having learned more than one tool, to attain a more general understanding about a family of tools.
* **We want you to learn to thrive under given conditions**: As a professional Software Engineer, you must learn to be productive in any given tool environment, rather than insist on using your preferred tools. It is usually in small companies doing less important work that you get to chose your own toolset. Bigger companies working on mature products often impose some choices on developers, such as the project management tool, code repository, IDE, language etc. For example, Google used SVN as their revision control software until very recently, long after SVN fell out of popularity among developers. Sometimes this is due to cost reasons (tool licensing cost), and sometimes due to legacy reasons (because the tool is already entrenched in their codebase).
 While programming in school is often a solo sport, programming in the industry is a team sport. As we are training you to become professional software engineers, it is important to get over the psychological hurdle of needing to satisfy individual preferences and get used to making the best of a given environment.

Practical reasons:

* Some of the topics are tightly coupled to tools. Allowing more tools means tutors need to learn more tools, which increases their workload.
* We provide learning resources for tools. e.g. 'Git guides'. Allowing more tools means we need to produce more resources.
* When all students use the same tool, the collective expertise of the tool is more, increasing the opportunities for you to learn from each others.

Meanwhile, feel free to share with peers your experience of using other tools.

</div>
<!-- =============================================================== -->
<div id="faq-manySubmissions-Q">Why so many small submissions?</div>
<div id="faq-manySubmissions-A">

<pic eager src="{{baseUrl}}/admin/images/frequent submissions.png" width="759" height="359"/>

The high number of submissions is not meant to increase workload but to spread it across the semester. Learning theory and applying them should be done in parallel to maximize the learning effect. That can happen only if we spread theory and 'application of theory' (i.e., project work) evenly across the semester.

In addition, spreading the work across the semester aligns with the <tooltip content="revisiting concepts at spaced intervals">'spaced repetition'</tooltip> technique that we apply in this course to increase your retention of concepts learned.
</div>
<!-- =============================================================== -->
<div id="faq-cs2101Difference-Q">Why submission requirements differ between CS2103T and CS2101?</div>
<div id="faq-cs2101Difference-A">

<pic eager src="{{baseUrl}}/admin/images/Submission requirements differ.png" width="300"/>

{{ course }}T communication requirements are limited to a very narrow scope (i.e., communicate about the product to users and developers). CS2101 aims to teach you technical communication in a much wider context. While you may be able to reuse some of the stuff across the two courses, submission requirements are not intended to be exactly the same.
</div>
<!-- =============================================================== -->
<div id="faq-java21-Q">Why not move to a newer Java version (e.g., 21)?</div>
<div id="faq-java21-A">

While we are aware that Java 21 is a more recent LTS version of Java, we are sticking with Java 17 for the time being. We plan to move to Java 21 in a future semester when its adoption is sufficiently high.
</div>
<!-- ===============================================================
  iP
=============================================================== -->
<div id="faq-ipHowTagsUsed-Q">How are the iP git tags used in grading?</div>
<div id="faq-ipHowTagsUsed-A">

Adding a git tag in the iP is a self-declaration that you _think_ you are done with the iP increment. We take your word for it. We don't check the code to see if you have actually done the said increment. Therefore, it is just a mechanism for you to self-declare progress and for us to monitor those progress declarations.
</div>
<!-- =============================================================== -->
<div id="faq-ipBugAfterIncrementDone-Q">What if I discovered a bug after I finished an increment?</div>
<div id="faq-ipBugAfterIncrementDone-A">

Go ahead and fix it in a subsequent commit. There is no need to update the previous commit or move the corresponding tag to the new commit. As we do not test your code at every tag, earlier bugs will not affect your grade as long as they are fixed eventually. Similarly, feel free to improve the code of previous increments later.
</div>
<!-- =============================================================== -->
<div id="faq-ipMultipleIncrementsInSameCommit-Q">I did multiple increments in the same commit. How to fix?</div>
<div id="faq-ipMultipleIncrementsInSameCommit-A">

You can add the corresponding tags to the same commit.<br>
Optionally, if you haven't pushed the commit to the fork yet, you can try to figure out how to split that commit into multiple commits.
</div>
<!-- =============================================================== -->
<div id="faq-ipIncrementAlreadyDone-Q">The requirements of an increment scheduled for this week is already satisfied by the work I did in an earlier week. What now?</div>
<div id="faq-ipIncrementAlreadyDone-A">

You can add the corresponding tag to the earlier commit (or the latest commit -- it doesn't matter) and push the tag.
</div>
<!-- =============================================================== -->
<div id="faq-ipForgotToPushTag-Q">My iP increments are not detected by the dashboard because I forgot to push my tags earlier. What now?</div>
<div id="faq-ipForgotToPushTag-A">

Not to worry. Just push the tags now. They will be detected by the dashboard at the next update. There is no penalty if mistakes are detected and fixed soon after.
</div>
<!-- =============================================================== -->
<div id="faq-ipIncorrectTagOrBranch-Q">Oh no! I made a mistake in my tag/branch name.</div>
<div id="faq-ipIncorrectTagOrBranch-A">

It's OK; correct it now.
</div>
<!-- =============================================================== -->
<div id="faq-ipNotDoneInBranch-Q">What if I did the increment in the `master` branch, not in `branch-___` as required?</div>
<div id="faq-ipNotDoneInBranch-A">

It's fine. Be more careful in the future. Your iP marks will not be affected for missing an occasional deliverable such as this one.

If you still want to make that {{ as_tag("branch-___", tag_style="danger") }} item green in the iP dashboard, you can simply create a branch with the required branch name, do some commits in it, and merge it to `master`. The dashboard will accept it as long as it has the right name and merged to the `master` branch.
</div>
<!-- =============================================================== -->
<div id="faq-ipOtherDataFormats-Q">Can I use other data formats (e.g., serialized objects) to save tasks?</div>
<div id="faq-ipOtherDataFormats-A">

Yes, provided it doesn't require the user to install another  software.<br>
Also note that in the team project, there is a project constraint that requires the data to be saved in a human editable format.
</div>
<!-- =============================================================== -->
<div id="faq-ipMessedUpBranching-Q">Oops, I messed up my branching! Will I be penalized?</div>
<div id="faq-ipMessedUpBranching-A">

Not to worry. You are welcome to (but not _required_ to) try to rectify it. There is no penalty. Just take note of your mistake and try to avoid it in the future.

{{ icon_tip }} In addition, you can try to identify the intended learning objective of using branching requirement that you messed up, and try to achieve it on your own. For example, if the iP increment was intended for you to practice parallel branches, you can try to do some other iP code changes as parallel branches so that you replicate a branch graph similar to the one intended by the iP increment.
</div>
<!-- =============================================================== -->
<div id="faq-temp-Q"></div>
<div id="faq-temp-A">


</div>
<!-- =============================================================== -->
<!-- ===============================================================
  Participation FAQ
=============================================================== -->

<div id="faq-whenCanWeSeeQuizAnswers-Q">When can we see the quiz answers?</div>
<div id="faq-whenCanWeSeeQuizAnswers-A">

In most quizzes, answers will be released within a day after the quiz deadline.

On a related note, if you are not confident about the answer you've selected for a question, ==you are welcome to discuss it in the [forum]({{ url_forum }}), even if the submission deadline is not over yet== (but one question per thread please).

</div>
<!-- =============================================================== -->

<!-- ===============================================================
  Tutorial FAQ
=============================================================== -->
<div id="faq-tutorialWhatTutorsCanAnswer-Q">What kind of questions _can_ I ask the tutor?</div>
<div id="faq-tutorialWhatTutorsCanAnswer-A">

TLDR: In this course, tutor's main job is to deliver tutorials. Hence, tutors can answer questions related to (and arising from) the tutorial delivery. But they are not allowed to answer admin questions. They are not allowed to help with technical issues.

* {{ good }} *I did not understand your explanation of that question. Why did you say "a b c"?*<br>
  %%**Reason**: This question is a follow-up from a tutorial discussion.%%
* {{ good }} *This is how I understood coupling. Is that correct?*<br>
  %%**Reason**: This question shows you have put in some effort to learn the topic and seeking further clarification from the tutor.%%
* {{ bad }} *What is coupling?* | *What is SLAP?*<br>
  %%**Reason**: These are concept covered in the textbook and other resources provided.%%{% if cs2103 %}
* {{ bad }} *How will this be graded?* | *What happens if this submission is late?*<br>
  %%**Reason**: Tutors are not allowed to answer admin questions.%%
* {{ bad }} *My program crashes with this error; what to do?*<br>
  %%**Reason**: Tutors are not allowed to help with technical issues (post your issue in the forum instead).%%{% endif %}
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhatIfMissedDueToValidReason-Q">What if I can't attend a tutorial due to a valid reason (e.g., MC)?</div>
<div id="faq-tutorialWhatIfMissedDueToValidReason-A">

See the following course policy:

{{ embed_topic("appendixB-policies.md#policy-validAbsences", "Admin " + icon_embedding + " Policy on absences due to valid reasons") }}
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhatIfMissedDueToOtherReason-Q">What if I can't attend a tutorial due to another commitment (e.g., interview)?</div>
<div id="faq-tutorialWhatIfMissedDueToOtherReason-A">

Our tutorial participation bar has enough of a buffer to allow an occasional absence (irrespective of the reason for absence). While we are not able to make special arrangements for absences due to reasons not accepted as valid by NUS (e.g., due to family event, interview, travel delays, overslept etc.), such absences are unlikely to affect your participation marks unless frequent.

* You are welcome to keep your tutor informed of such absences as a courtesy, but it is not a requirement.
* If you miss a tutorial, do try to catch up as best as you can {% if cs2103 %} e.g., by watching the tutorial recording{% endif %}.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialLength-Q">Can the tutorial be made longer (e.g., 2 hours)?</div>
<div id="faq-tutorialLength-A">

In the past, many students have requested to increase the tutorial duration because a mere hour is barely enough to get through all the tutorial tasks. Increasing the tutorial time is not possible due to lack of venues and tutors. Instead, let's try to make the best of the one hour available by coming well-prepared and starting on time. Note that ==the better prepared you are, the higher the chance of completing all activities allocated to a tutorial== within time.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhyZoomInF2f-Q">WHAT? Why use Zoom when we are already F2F?</div>
<div id="faq-tutorialWhyZoomInF2f-A">

Zoom is still needed for,<br>
(a) screen-sharing the slides,<br>
(b) collecting answers via PM or polls,<br>
(c) recording the tutorial for your future reference.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialByZoom-Q">Are you allowed to attend the tutorial via Zoom instead?</div>
<div id="faq-tutorialByZoom-A">

By default, no.<br>
Reason: it goes against the purpose of F2F tutorials (i.e., to get the whole team to meet physically) and the NUS directive to move all small classes to F2F mode.<br>
However, you can request (by emailing `{{ course | lower }}@comp.nus.edu.sg`) to attend the tutorial of a specific week via Zoom, if you have a valid reason (e.g., MC, taking part in an NUS-related event).
</div>
<!-- =============================================================== -->
<div id="faq-tutorialZoomWithoutPermission-Q">What happens if I join a tutorial via Zoom, without getting permission to do so?</div>
<div id="faq-tutorialZoomWithoutPermission-A">

There is no penalty, but that tutorial will not count for participation. See [here](participation.html#:~:text=Sufficient%20tutorial%20attendance/participation) for the bar you need to meet for tutorial participation.
</div>
<!-- =============================================================== -->

<!-- ===============================================================
  tP FAQ
=============================================================== -->
<div id="faq-tpWhyNarrowTarget-Q">Why the need to narrow down the user profile?</div>
<div id="faq-tpWhyNarrowTarget-A">

* It is an opportunity to exercise your product design skills because optimizing the product to a very specific target user requires good product design skills.
* It minimizes the overlap between features of different teams which can cause plagiarism issues. Furthermore, higher the number of other teams having the same features, less impressive your work becomes especially if others have done a better job of implementing that feature.
</div>
=============================================================== -->
<div id="faq-tpHowNarrowTargetCanBe-Q">How narrow can we make the target market?</div>
<div id="faq-tpHowNarrowTargetCanBe-A">

The size of the target market is not a grading criterion. You can make it as narrow as you want. Even a single user target market is fine as long as you can define that single user in a way others can understand (reason: project evaluators need to evaluate the project from the point of view of the target users).
</div>
=============================================================== -->
<div id="faq-dgDetailsLevel-Q">How detailed the DG should be? Do we have to describe every feature/component?</div>
<div id="faq-dgDetailsLevel-A">

The DG is primarily meant to help current/future developers. Therefore, decide based on how the inclusion/exclusion affects that target audience (you belong to the target audience too!).
</div>
=============================================================== -->
<div id="faq-tpChangeDirectionLater-Q">Can we change the target user and value proposition later in the project?</div>
<div id="faq-tpChangeDirectionLater-A">

Yes. If the submission deadline is not over yet, use the same link to update the submission. If the submission deadline is over, email the updated name, target user, value proposition to `{{ course | lower }}@comp.nus.edu.sg`.
</div>
<!-- =============================================================== -->
<div id="faq-dgAddNewUml-Q">Is it enough to update existing UML content/diagrams or must we add new content/diagrams?</div>
<div id="faq-dgAddNewUml-A">

**You are welcome to add new content/diagrams**, but it is not a strict requirement. Consider costs %%(e.g., the effort required to add and maintain new content)%% vs benefits %%(how much the new content helps future developers)%% and decide accordingly.
**However, everyone is expected to contribute to the DG**, which means you should divide the DG-update work among team members.
</div>
<!-- =============================================================== -->
<div id="faq-githubWhoCreatesIssues-Q">Who should create issues?</div>
<div id="faq-githubWhoCreatesIssues-A">

We recommend that (when possible) the person allocated to perform the task should also create (and manage) the issue. This will help everyone practice this aspect of the project, and spread the workload among team members.
</div>
<!-- =============================================================== -->
<div id="faq-githubIssuesForNonCodingTasks-Q">Can we use issues to track non-coding tasks? e.g., a submission</div>
<div id="faq-githubIssuesForNonCodingTasks-A">

Yes ([an example](https://github.com/TEAMMATES/teammates/issues/12976)), although having too many non-coding tasks in the issue tracker can make it cluttered.

</div>
<!-- =============================================================== -->
<div id="faq-githubIssuesSubTasks-Q">How do we track 'sub-task' relationships between tasks?</div>
<div id="faq-githubIssuesSubTasks-A">

GitHub Issues does not have a direct way of doing this. However, you can use a task list in the issue description to indicate sub-tasks and corresponding issues/PRs -- ([an example](https://github.com/MarkBind/markbind/issues/1774))
</div>
<!-- =============================================================== -->
<div id="faq-githubMultipleIssueAssignees-Q">Is it OK to assign multiple members to the same task?</div>
<div id="faq-githubMultipleIssueAssignees-A">

This is discouraged in the tP, as it makes task allocations (and accountability) harder to track.<br>
Instead, shared tasks can be split into separate issues. For example, instead of creating an issue `Update teams page with own info` and assigning it to all team members (in which case, this issue can't be closed until all members do their part), you can create issues such as `Update teams page with John's info` that can be assigned to individual members.
</div>
<!-- =============================================================== -->
<div id="faq-githubIssueForEachPr-Q">Must there be a corresponding issue for each PR?</div>
<div id="faq-githubIssueForEachPr-A">

This is encouraged, while not a strict rule. Creating an issue indicates 'a task to be done', while a PR is 'a task being done'. These are not the same, and there can be a significant time gap between the two.<br>
 Furthermore, posting an issue in advance allows the team to,

* anticipate a PR is coming
* discuss more about the task (in the issue thread) e.g., alternatives, priority
* indicate who will be doing the task (by adding an assignee), when it should be done (by adding it to a milestone)
</div>
<!-- =============================================================== -->
<div id="faq-githubWhoMergesPrs-Q">Who should merge PRs? e.g., PR author, reviewer, team lead?</div>
<div id="faq-githubWhoMergesPrs-A">

It is up to the team to decide. However, we discourage unilateral PR merging i.e., you create and merge PRs without any reviews/oversight from others, unless the PR is trivial changes.
</div>
<!-- =============================================================== -->
<div id="faq-tpEnoughFeatures-Q">If our team implement features x, y, and z, is that enough?</div>
<div id="faq-tpEnoughFeatures-A">

Yes, if it requires each member to put in about a half an iP worth of effort.
</div>
<!-- =============================================================== -->
<div id="faq-tpMustWrite300Loc-Q">Is it a must to write at least 300 LoC?</div>
<div id="faq-tpMustWrite300Loc-A">

Not necessarily. It depends on the effort required, which in turn depends on what the code does. It is quite possible for 100 LoC that implements feature X to take more effort than 300 LoC that implements feature Y (i.e., it depends on the context). So, we measure the effort, not LoC (LoC figure given is just a rough estimate of the _equivalent_ effort).

</div>
<!-- =============================================================== -->
<div id="faq-tpFullMarksFor300Loc-Q">Still, if I write 300 LoC, I get full marks for implementation?</div>
<div id="faq-tpFullMarksFor300Loc-A">

There is no such guarantee, for two reasons:

1. Your implementation effort is graded based on how much functionality your team produced (based on peer-testers' and tutors' estimates) and how much of that work was contributed by you (based on team members' estimates). For example, simply copy-pasting 400+ LoC with only minor modifications is unlikely to meet this bar as it is less than an effort _equivalent_ to writing a typical 300-400 LoC (or half of a typical iP effort).
1. Implementation marks are based on both effort and quality, the latter being the primary driver (more info <trigger trigger="click" for="modal:tPexpectations-implementationGrading">here</trigger>). So, meeting the effort bar doesn't guarantee full marks for implementation.
</div>
<!-- =============================================================== -->
<div id="faq-tpIterationDeadline-Q">What's the deadline for tP iterations?</div>
<div id="faq-tpIterationDeadline-A">

The deadline for tP iterations is the `Thursday 23:59` in the week it is due, unless a different date is specified in the instructions of that iteration.
</div>
<!-- =============================================================== -->
<div id="faq-tpHowMuchToGetFullMarks-Q">How much code/features is enough to get full marks?</div>
<div id="faq-tpHowMuchToGetFullMarks-A">

Not surprisingly, a common question tutors receive is "can you look at our project and tell us if we have done enough to get full marks?". Here's the answer to that question:

**The tP _effort_ is graded primarily based on peer judgements** (tutor judgements are used too). That means you will be judging the effort of another team later, which also means you should be able to make a similar judgement for your own project now. While we understand effort estimating is hard for software projects, it is an essential SE skill, and we must practice it when we can.

**The expected minimum bar to get full marks for _effort_** is given <trigger trigger="click" for="modal:mid13-effortBar"> here</trigger>.

<modal large header="tP -> Expectations -> [Extract] Functionality Expectations" id="modal:mid13-effortBar">
<include src="tp-expectations.md#functionality-expectations"/>
</modal>

If you surpass the above bars (in your own estimation), you should be in a good position to receive full marks for the effort. But keep in mind that there are many other components in the [tP grading](tp-grading.md), not just the effort.
</div>
<!-- =============================================================== -->
<div id="faq-tpNotEnoughWorkToDivide-Q">What if the chosen user stories for MVP is not enough to do a meaningful work division among team members?</div>
<div id="faq-tpNotEnoughWorkToDivide-A">

In that case, at a later stage, you can add more user stories until there is enough for a meaningful work distribution. But at this point focus on selecting the smallest sub-set of _must_have_ user stories only.
</div>
<!-- =============================================================== -->
<div id="faq-tpShouldWeStartCoding-Q">Should we start implementing MVP now?</div>
<div id="faq-tpShouldWeStartCoding-A">

Not at all. That is scheduled several weeks later. For now, just figure out the minimal feature set required for the product. We'll let you know when it is time to start working on the MVP.
</div>
<!-- =============================================================== -->
<div id="faq-tpOmitStoriesInAb3-Q">Should we omit user stories that are already supported by AB3?</div>
<div id="faq-tpOmitStoriesInAb3-A">

No, you should still include them. Reason: The existing implementation might still require some work before it fits your product.
</div>
<!-- =============================================================== -->
<div id="faq-tpAllStoriesInAb3-Q">All the user stories we selected for MVP are already supported by AB3. What now?</div>
<div id="faq-tpAllStoriesInAb3-A">

That's fine. It means you can get to MVP with very little effort, which is a good thing. Once you've finished the MVP, if there is time left, you can add more things to it at that time.
</div>
<!-- =============================================================== -->
<div id="faq-tpIndividualOrTeam-Q">Is this a team task or an individual task?</div>
<div id="faq-tpIndividualOrTeam-A">

It's an individual task (note the icon {{ icon_individual }} above), to be done by each member, as we want _every_ member to be familiar with the codebase.
</div>
<!-- =============================================================== -->
<div id="faq-tpTestsForTutorial-Q">When doing this tP tutorial, do we have to write/update test cases too?</div>
<div id="faq-tpTestsForTutorial-A">

Not a strict requirement, but given the purpose of this tutorial is to learn the codebase, it's ideal if you do. It will familiarize you with the existing testing infrastructure. Otherwise, you can run into difficulties when you are writing test cases for your own features later.
</div>
<!-- =============================================================== -->

<div id="faq-tpHowManyFeaturesInMvp-Q">How many features should we put in the MVP?</div>
<div id="faq-tpHowManyFeaturesInMvp-A">

Aim for the _smallest set of features the product cannot do without_. Even a most basic version of those features is enough. After completing that feature set, you can add more if there is time left.
</div>
<!-- =============================================================== -->

<div id="faq-githubIssuesMultipleDocAuthors-Q">When all members are updating the same document, can we create one issue and assign it to all?</div>
<div id="faq-githubIssuesMultipleDocAuthors-A">

**A:** In the tP (in which our grading scripts track issues assigned to each member), it is better to create separate issues so that each person's work can be tracked separately. For example, suppose everyone is expected to update the User Guide (UG). You can create separate issues based on which part of the UG will be updated by which person e.g., `List-related UG updates` (assigned to John), `Delete-related UG updates` (assigned to Alice), and so on.
</div>
<!-- =============================================================== -->

<div id="faq-tpOneMemberNotDone-Q">What if a team member has not done this task? Can the rest proceed?</div>
<div id="faq-tpOneMemberNotDone-A">

If a team member fails to do this within a reasonable time, try to help that team member with this task, if needed. Failing that, the rest of the team can proceed with the remainder of the task. In the latter case, inform the tutor that you are proceeding with this task without waiting for that team member.
</div>
<!-- =============================================================== -->

<div id="faq-tpNoPrInIteration-Q">Will I lose marks if I couldn't merge any PRs in an iteration?</div>
<div id="faq-tpNoPrInIteration-A">

As it is the case with other similar tP requirements, there is no penalty for missing this expectation occasionally. But try not to miss it too often.
</div>
<!-- =============================================================== -->

<div id="faq-tpUpdateTestsWithCode-Q">Do we have to update tests when we update functional code?</div>
<div id="faq-tpUpdateTestsWithCode-A">

**In very early iterations,** ==try to keep the existing tests (and CI) working==. It is optional to add more tests.

**In general,** there are several options you can choose from:

1. Update/add tests every time you change functional code. This is what normally happens in stable production systems. For example, most OSS projects will not accept a PR that has failing tests or not enough new tests to cover the new functional code.
2. Disable failing tests temporarily until the code is stable. This is suitable when the functional code is in a highly volatile state (e.g., you are still experimenting with the implementation). The benefit is that you avoid the cost of writing tests for functional code that might change again soon after. Some costs: (a) harder to detect regressions during the period tests are disabled (b) testing work pile up which could distort your estimate of real progress (c) forgetting to enable the tests in time<br>
  This is still a viable option during some stages of a tP e.g., during the early part of an iteration, or while a PR is still in 'draft' state (i.e., for getting early feedback from the team).
4. Decide certain tests are not worth the effort to maintain, and delete them permanently. Result: Less test code to maintain but higher risk of undetected regressions.
</div>
<!-- =============================================================== -->

<div id="faq-tpUpdateDocsWithCode-Q">Do we need to update user/developer guides to match code changes?</div>
<div id="faq-tpUpdateDocsWithCode-A">

**In general**, it is better for a PR to update code, tests, and documentation together.

**In early iterations**, it is fine not to update documentation, to keep things simple. We can start updating docs in a later iteration, when the code is more stable.
</div>
<!-- =============================================================== -->

<div id="faq-tpWhyUpdateDiagramsEarly-Q">Why not wait till the end to add/update the DG diagrams?</div>
<div id="faq-tpWhyUpdateDiagramsEarly-A">

Here are some reasons:
* We want you to take at least two passes at documenting the project so that you can learn how to evolve the documentation along with the code %%(which requires additional considerations, when compared to documenting the project only once)%%.
* It is better to get used to the documentation tool chain early, to avoid unexpected problems near the final submission deadline.
* It allows receiving early self/peer/instructor feedback.
</div>
<!-- =============================================================== -->

<div id="faq-tpFeatureTakeovers-Q">What if someone took over a feature from another team member?</div>
<div id="faq-tpFeatureTakeovers-A">

In terms of effort distribution, it's up to the team to tell us who did how much. Same goes for assigning bugs. So, it's fine for someone to take over a feature if the team is able to estimate the effort of each member, and they have a consensus on who will be responsible for bugs in that feature.<br>
For code authorship, only one person can claim authorship of a line, and that person will be graded for the code quality of that line. By default, that will be the last person who edited it (as per Git data) but you can [override that behavior using `@@author` tags](tools.html#tool-reposense-for-authorship-tracking).
</div>
<!-- =============================================================== -->

<div id="faq-faqid-Q"></div>
<div id="faq-faqid-A">


</div>
<!-- =============================================================== -->

