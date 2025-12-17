{% from "common/macros.njk" import as_tag, embed_topic, thumb_small with context %}

<!-- =============================================================== -->
<div id="faq-howToDecideTooLongOrTooDeepMethods-Q">How to decide if a method is _too long_ (or if the nesting is _too deep_)?</div>
<div id="faq-howToDecideTooLongOrTooDeepMethods-A">

There are no hard-and-fast rules. While some numbers (e.g., 30 LoC, or 3 levels of nesting) may be mentioned as guidelines, it is always a case-by-case decision. For example, a method with 50 LoC may be considered as not 'too long' if its contents are justified or if the costs of shortening it outweigh the benefits.

</div>
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
<div id="faq-umlIsItUsedInIndustry-Q">Is UML even used in the industry? Is there any point learning it?</div>
<div id="faq-umlIsItUsedInIndustry-A">

**UML is not used very frequently by practitioners.** In particular, most would not bother to draw detailed UML diagrams _before_ (or in parallel to) coding.<br>
**UML diagrams can still provide practical value in some situations** e.g., when documenting internal design details, when discussing design alternatives. However, even when using UML is beneficial, some may avoid using it due to lack of proficiency. In fact an average programmer is likely to be able to survive without drawing any UML diagrams, and only occasionally having to interpret UML diagrams drawn by others.

However, **being able to communicate about code/design without referring to actual code is an essential skill**, as the code is not always available %%(e.g., it may not exist yet or the codebase may be too big for to be used for such communications)%%. While in some cases we can use ad hoc notations (simple boxes, arrows, labels) for such communications, using a standard modeling notation can make such communications universally understood. **UML is the leading general-purpose notation used for modelling software design.** It can be used for basic modelling irrespective of the domain of the software project. For more intense modeling needs, we can go for a domain-specific modelling notation %%e.g., Business Process Model and Notation (BPMN)%%.<br>

Besides, **UML is just a tool that we use to learn a more fundamental SE skill: the ability to model code visually**, especially at higher abstraction levels. This skill is necessary to be able to build mental models of large code bases in our head, even if you don't actually draw physical diagrams, UML or otherwise.

</div>
<!-- =============================================================== -->
<div id="faq-umlAreWeOverdoing-Q">OK, so there is _some_ value in learning UML. But do we have to spend _so much_ time on it?</div>
<div id="faq-umlAreWeOverdoing-A">

**It is true that we are 'overdoing' UML a bit in this course.** Because UML is not used frequently in the industry (especially, by junior developers), you will not have many chances to learn it 'on the job' in the early part of your career. Hence, **we try to ensure you learn UML well-enough to be able to use it a few years later**, even if you don't get to use it in the interim period.
</div>
<!-- =============================================================== -->
<div id="faq-umlWhenNotationNotEnough-Q">What do we do when the UML notation covered in the course is not enough to model what we want to illustrate?</div>
<div id="faq-umlWhenNotationNotEnough-A">

Here are some options you can consider:

* **Use the closest matching notation**, and use UML notes to provide the missing information.
* **Use an alternative means to communicate** %%(e.g., pseudocode, or even actual code)%%, instead of using a UML diagram.
* **Leave out the complex part from the diagram**, or give a simpler view in the model, if the complex part is not really relevant to the purpose of the diagram (but also mention that the model is a simplified view).

Caution: For course deliverables, it is best not to use UML notations not covered in the course.
</div>
<!-- =============================================================== -->
<div id="faq-umlWhyNoCorrespondenceBetweenUmlAndCode-Q">Why can't the code and the UML correspond to each other _exactly_, in both directions?</div>
<div id="faq-umlWhyNoCorrespondenceBetweenUmlAndCode-A">

There are several reasons:

* Some design concepts do not have direct translations to a mechanism in the programming language %%e.g., most programming languages do not have a direct way to implement a bidirectional association%%.
* Some programming language constructs might not have corresponding UML constructs %%e.g., lambdas%%
* Some implementations can choose to deviate from the intended design due to other valid reasons such as performance, code clarity, convenience etc.
</div>
<!-- =============================================================== -->
<div id="faq-umlHowToFindIntendedDesignFromCode-Q">When drawing UML diagrams from the code, how to find the 'intended' design from the code?</div>
<div id="faq-umlHowToFindIntendedDesignFromCode-A">

In a real project, in most cases, the person drawing the diagram is likely to be the same person who wrote the code, which means that person is likely to know the intended design already. If this is not the case, one can try to approximate the intended design based on one's own domain knowledge, consulting domain experts, from other sources such as project documentation (and code comments).

In an exam question, the missing info will be provided as part of the question, _if_ it is relevant to the expected answer.
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
* We provide learning resources for tools. e.g., 'Git guides'. Allowing more tools means we need to produce more resources.
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

While we are aware that Java 21 is a more recent <tooltip content="Long-Term Support">LTS</tooltip> version of Java, we are sticking with Java 17 for the time being. We plan to move to Java 21 in a future semester when its adoption is sufficiently high.<br>
Related: The industry is slow to move to new Java versions. It is likely the legacy Java systems you'll encounter in your internships/jobs are even older than Java 17.
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
<div id="faq-ipIncreaseDashboardFrequency-Q">Can the iP dashboard be updated more frequently?</div>
<div id="faq-ipIncreaseDashboardFrequency-A">

**Good news:** Even if an item in the iP dashboard turns red, it does not affect your marks if you fix it soon, turning it back to green subsequently.

**It is difficult to increase the dashboard update frequency** due to following reasons:

* **Resource limitations** e.g., limits on the number of GitHub API calls, GitHub Actions minutes, GitHub Actions bandwidth used, etc.
* **The updates cannot be fully automated** as some data sources do not allow programmatic access or require a staff account to access them (e.g., Canvas). Therefore, dashboard updates require some manual work, and is run in a local computer (not running on a server somewhere).<br>
  {{ icon_info }} While the stated update frequency is 24 hours, we do update it a few times each day.

**A high frequency of dashboard updates is also not _desirable_** because an over-reliance on an external verification mechanism to confirm if you 'did something correctly' is not conducive to learning.

**Recommendation:** Aim to finish tasks well in advance of the deadline so that, in the unlikely event that you make a mistake in your work and the item does not turn green, you will still have time to correct it before the deadline.
</div>
<!-- =============================================================== -->
<div id="faq-ipMarksForOptionalIncrements-Q">If I do optional increments, do I get more marks?</div>
<div id="faq-ipMarksForOptionalIncrements-A">

Not necessarily. The iP is intended to help you to learn the skills required for the tP. Almost all students are expected to receive full marks. See [here](ip-grading.md) for more info on iP grading.

If you are already experienced in using the concept covered by the optional increment, the value you gain from completing that increment is relatively low. But if you are not, there is value in doing that increment irrespective of how it affects iP marks.
</div>
<div id="faq-ipForkedTheWrongRepo-Q">I forked the iP repo from a previous semester. How to fix?</div>
<div id="faq-ipForkedTheWrongRepo-A">

Not to worry. Here are the steps to fix:

1. Delete the fork in your GitHub account.
1. Fork the [correct upstream repo]({{url_course_org}}/{{ ip_repo_name }}).
1. [Optional] Take a backup of your local repo folder.
1. Pull from your fork. Notes:
   * Because the URL of the previous fork is the same as the new fork, this will now pull from the new fork.
   * Pulling from the new fork is possible because your clone and both the old and the new fork have a shared ancestry (i.e., they all originated from the [same duke repo](https://github.com/se-edu/duke)).
1. If the new fork has commits that were not present in your old fork, the above pull operation will result in a merge conflict. [Resolve it]({{ baseUrl }}/book/gitAndGithub/mergeConflicts/) and commit.
1. Push to the fork. This will push your new commits to your new fork.
</div>
<!-- =============================================================== -->
<div id="faq-ipIncorrectTagOrBranch-Q">Oh no! used the wrong tag/branch name.</div>
<div id="faq-ipIncorrectTagOrBranch-A">

It's OK; correct it now.<br>
If you used the incorrect tag earlier, create and push the correct tag now. You are welcome to (but not required to) delete the previous tag.
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

Yes, provided it doesn't require the user to install another software.<br>
Also note that in the team project, there is a project constraint that requires the data to be saved in a human editable format.
</div>
<!-- =============================================================== -->
<div id="faq-ipMessedUpBranching-Q">Oops, I messed up my branching! Will I be penalized?</div>
<div id="faq-ipMessedUpBranching-A">

Not to worry. You are welcome to (but not _required_ to) try to rectify it. There is no penalty. Just take note of your mistake and try to avoid it in the future.

{{ icon_tip }} In addition, you can try to identify the intended learning objective of using branching requirement that you messed up, and try to achieve it on your own. For example, if the iP increment was intended for you to practice parallel branches, you can try to do some other iP code changes as parallel branches so that you replicate a branch graph similar to the one intended by the iP increment.
</div>
<!-- =============================================================== -->
<div id="faq-ipAspectsNotCoveredByTheStandard-Q">What to do if a certain aspect is not covered by the Java/Git standard?</div>
<div id="faq-ipAspectsNotCoveredByTheStandard-A">

When something is not covered by the given standard/convention, you are free to choose which style you want to follow for that, but try to be consistent with the existing code (if any), and ensure everyone in the team follows the same (if it is a team project).
</div>
<!-- =============================================================== -->
<div id="faq-ipCheckstyleMismatchWithCodingStandard-Q">What if the given sample Checkstyle config file doesn't match exactly with the Java coding standard?</div>
<div id="faq-ipCheckstyleMismatchWithCodingStandard-A">

In some areas, the sample Checkstyle rules file ([recommended by the SE-EDU guide](https://se-education.org/guides/tutorials/checkstyle.html)) may be slightly more permissive/restrictive than (but not contradictory to) the given Java coding standard. You are free to tweak the Checkstyle file if you wish. It is fine as long as your code is compliant with the given coding standard.
</div>
<!-- =============================================================== -->
<div id="faq-ipMoreCodeQualityFeedback-Q">Can we get another round of automated code quality feedback?</div>
<div id="faq-ipMoreCodeQualityFeedback-A">

(a) Evaluating,  and, (b)maintaining your own code quality are !!two!! things we hope you'll learn in this course.

* We do give you some automated feedback on code quality about half-way into the tP, to get you started. From then on you'll need to keep an eye on code quality, and make a judgement call on when to improve (and how much is enough).
* Later on, during the iP evaluation (which has a peer evaluation), you'll also get to evaluate the code quality and testing level of other iPs. This should serve as more practice.

That said, we'll still give you one more round of further code quality feedback, after the iP is over. That is to help you identify the things you missed yourself, and do an even better job in the tP.
</div>
<!-- =============================================================== -->
<div id="faq-ipMinimumRequirementNotGiven-Q">What if the minimum requirement for an increment is not specified? How do I decide how much work is enough?</div>
<div id="faq-ipMinimumRequirementNotGiven-A">

Deciding a feature’s behavior is a product design decision, and this is a good opportunity to practice that aspect of software engineering. So, decide for yourself: as a user of this product, what is the minimally acceptable behavior of this feature?
</div>
<!-- =============================================================== -->
<div id="faq-ipIfSubmissionBelowBar-Q">What if my iP final submission doesn't meet the bar for full marks? Do I get a chance to resubmit?</div>
<div id="faq-ipIfSubmissionBelowBar-A">

Yes, you will get a chance for resubmission, without any penalty.

That said, a resubmission is likely to be held to a higher bar than the standard bar for iP. So, it is in your interest to ensure your initial iP submission meets the bar for full marks.
</div>
<!-- =============================================================== -->
<div id="faq-ipEvaluationNoJar-Q">What if the student has not uploaded a JAR file, or the JAR file doesn't work at all?</div>
<div id="faq-ipEvaluationNoJar-A">

When you submit the evaluation (step 8 below), there will be a way to indicate that the JAR was not available, or any other serious issues you faced.
</div>
<!-- =============================================================== -->
<div id="faq-ipDeadlineExtensions-Q">How to get a deadline extension for the iP final submission?</div>
<div id="faq-ipDeadlineExtensions-A">

#r#**There is no need to ask for extensions**## to the iP final submission deadline.

**It is ideal if you finish the iP by original deadline**, but if you could not
finish it by that deadline, we'll be giving you an automatic 3-day deadline extension.
Further deadline extensions beyond that might be possible too, provided we see evidence of
you trying to progress in the previous deadline extension (and not simply postponing work to take advantage of the
deadline extensions).

* While there will be no penalty for such a deadline extension, keep in mind that the longer you take to finish the iP, the less time you'll have for the tP.
* To reiterate, the said deadline extension will be given automatically, _after_ the initial deadline is over: ==Please don't send us deadline extension requests in advance.==
* Caution: Unlike the iP, no free extensions will be available for the **t**P final submission deadline. Even a one-second delay will be considered a _late_ submission and will have to be penalized, as deadline compliance is a learning outcome of the course.
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
<div id="faq-participationTaskMissedDueToValidReason-Q">What if I missed a participation task due to a legitimate reason? %%(e.g., falling sick, taking part in university event)%%</div>
<div id="faq-participationTaskMissedDueToValidReason-A">

See the panel below:
{{ embed_topic("policies-fragment.md#policy-validAbsences", "Admin " + icon_embedding + " Policies → Absences due to valid reasons", "4", status='expanded', indent=1) }}
<p/>

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
<div id="faq-tutorialWhyTutorsCannotAnswerAdminQuestions-Q">Why are tutors not allowed to answer admin questions?</div>
<div id="faq-tutorialWhyTutorsCannotAnswerAdminQuestions-A">

The course has MANY admin details and there are subtle changes from semester to semester. Tutors might not be aware of those changes, increasing the risk that you receive subtly incorrect answers. Besides, it is not fair to expect tutors to know all the admin details, as they should be using their memory for things related to their own courses.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhyTutorsCannotGiveProjectFeedback-Q">Why are tutors not allowed to give feedback on project deliverables?</div>
<div id="faq-tutorialWhyTutorsCannotGiveProjectFeedback-A">

**Tutors are not allowed to give ad hoc feedback on yet-to-be-graded components** (e.g., iP or tP components, which accounts for a very high percentage of the overall grade),

* **to ensure the work you submit for grading is entirely your own** %%(for the same reasons why you are not allowed to ask invigilators for 'feedback' on your answers while you are answering the final exam paper)%%.
* **to ensure fairness across teams** %%(because if tutors were allowed to give feedback on their own, it will be impossible to ensure all tutors give the same level of feedback)%%.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialHowToImproveProjectWithoutTutorFeedback-Q">Huh? If tutors are not giving feedback on project deliverables, how can we improve our project work?</div>
<div id="faq-tutorialHowToImproveProjectWithoutTutorFeedback-A">

It is true that the teaching team will not give _ad hoc_ feedback on yet-to-be-graded project deliverables. **But you will receive systematic feedback at various points of the project**, in a way that ensures all of you receive the same level of feedback about the same things.

**More importantly, we aim to develop your <tooltip content="i.e., the ability to make decisions about the quality of one's own work
   and that of others">_evaluative judgement_ skills</tooltip>** thus reducing your reliance on someone else's feedback to decide how to improve. To this end, we have set up various learning tasks to help you judge your own work. Examples:

* Tutorial tasks that go through a 'sample' project aspect/artifact (e.g., use cases of a sample project) and find problems in it. This way, we can ensure that all of you encounter all the important learning points related to that aspect/artifact, even if some may not be relevant to your own project (which means you wouldn't have encountered them on your own).
* Peer evaluations of each other's work, within teams and between teams. This gives you a way to exercise your evaluative judgement skills.

</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhatIfMissedDueToValidReason-Q">What if I can't attend (or missed) a tutorial due to a valid reason (e.g., MC)?</div>
<div id="faq-tutorialWhatIfMissedDueToValidReason-A">

See the following course policy:

{{ embed_topic("appendixB-policies.md#policy-validAbsences", "Admin " + icon_embedding + " Policy on absences due to valid reasons") }}
<p/>

If you wish to attend a different tutorial timeslot in a specific week, please send your request to the course email (`{{ course_email  }}`).
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhatIfMissedDueToOtherReason-Q">What if I can't attend a tutorial due to another commitment (e.g., interview)?</div>
<div id="faq-tutorialWhatIfMissedDueToOtherReason-A">

Our tutorial participation bar has enough of a buffer to allow an occasional absence (irrespective of the reason for absence). While we are not able to make special arrangements for absences due to reasons not accepted as valid by NUS (e.g., due to family event, interview, travel delays, overslept etc.), such absences are unlikely to affect your participation marks unless frequent.

* You are welcome to keep your tutor informed of such absences as a courtesy, but it is not a requirement.
* If you miss a tutorial, do try to catch up as best as you can {% if cs2103 %} e.g., by watching the tutorial recording{% endif %}.
* If you wish to attend a different tutorial timeslot in a specific week, please send your request to the course email (`{{ course_email  }}`).

</div>
<!-- =============================================================== -->
<div id="faq-tutorialLength-Q">Can the tutorial be made longer (e.g., 2 hours)?</div>
<div id="faq-tutorialLength-A">

In the past, many students have requested to increase the tutorial duration because a mere hour is barely enough to get through all the tutorial tasks. Increasing the tutorial time is not possible due to lack of venues and tutors. Instead, let's try to make the best of the one hour available by coming well-prepared and starting on time. Note that ==the better prepared you are, the higher the chance of completing all activities allocated to a tutorial== within time.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhyZoomInF2f-Q">WHAT? Why use Zoom when we are already F2F?</div>
<div id="faq-tutorialWhyZoomInF2f-A">

Zoom is still needed for the following reasons:

* Screen-sharing the slides. {texts="['(a)', '(b)', '(c)']"}
* Collecting answers via PM or polls.<br>
  **Why insist on answering via PM?** This gives everyone a chance to think about the question and come up with their own answer, without being influenced by others' answers, and without being embarrassed for giving the wrong answer. Research has shown that this _attempt_ at answering increases retention of the correct answer received subsequently, irrespective of the correctness of the answer the student initially came up with.<br>
  As a bonus, this tutorial structure will also give you a good training for the final exam.
* Recording the tutorial for your future reference.<br>
  These recordings also help in improving tutorial quality (e.g., profs can review recordings of tutors and give feedback on how to improve).
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
<div id="faq-tutorialWhyF2f-Q">Why we need F2F tutorials? Why not do all tutorials via Zoom?</div>
<div id="faq-tutorialWhyF2f-A">

There are several reasons:

1. NUS policy requires all small classes to be F2F. Physical interaction with peers is an essential part of the university experience.
1. While Zoom is more convenient, they are not as effective in achieving some learning outcomes. For example, we are training you for working in team projects, and in technical communications, both of which sometimes need to be done in the F2F mode.
1. Your physical presence allows the tutor to observe team dynamics better. To give an example, sometimes even a team's seating positions can tell us the level of team cohesion.

</div>
<!-- =============================================================== -->
<div id="faq-tutorialCannotReachInTime-Q">What if I can't reach the F2F venue in time due to a reason beyond my control %%(e.g., previous class ended late)%%?</div>
<div id="faq-tutorialCannotReachInTime-A">

Note that we do track your arrival time, as late arrivals hinder your ability to participate in the tutorial fully.

If you anticipate a late arrival due to a reason beyond your control (e.g., due to the previous class ending late), here are some strategies to mitigate the impact:

* Prepare for the tutorial tasks in advance, especially the first one. This will allow you to complete the task in time even if you arrive a few minutes late.
* Join the Zoom meeting while you are on the way to the class.

</div>
<!-- =============================================================== -->
<div id="faq-warmUpTaskRushed-Q">Why is tutorial task 1 rushed? I couldn't update the Workspace file before it was downloaded by the tutor; will I be penalised? Can I do it later?</div>
<div id="faq-warmUpTaskRushed-A">

Not to worry; there is no penalty. No need to do it later either.

We download the workspace file at the task 1 cut-off point to discourage students from continuing with task 1 (which is just a warmup activity) after task 2 has started. Continuing to work on task 1 at that point may prevent students from getting the full value from task 2, which usually has more learning value than task 1.

We use the downloaded workspace files to identify students who consistently come prepared for tutorials and perform well in tutorial tasks (e.g., when selecting tutors or awarding bonus points). However, we do not penalise students based on the workspace files.

If you frequently find yourself being unable to finish task 1 in time, consider doing it in advance.
</div>
<!-- =============================================================== -->
<div id="faq-tutorialWhyTutorCannotGiveTechHelp-Q">Why tutors are not allowed to give tech help?</div>
<div id="faq-tutorialWhyTutorCannotGiveTechHelp-A">

The pedagogical reason: Learning how to solve technical problems, and <tooltip content="e.g., explaining the problem well">seek</tooltip>/give/receive help, **are learning outcomes of this course, and are critical skills for software engineers**. So, we want you to practice those things in this course as much as possible.

A practical reason: Unlike in lower-level programming courses, the technical problem you encounter in this course are varied and dependent on your OS and tool choices. It is not possible for one person (e.g., your tutor) to know how to help with problems related to all OS'es and all tools used by students under his/her care. It is more practical to troubleshoot such problems via the course forum, as that gives you a way to get help from all your peers in the class, the entire teaching team, and a group of past students who have volunteered to help current students solve technical problems. Based on past data, we know that more than 90% of the problems posted in the course forum get resolved within 24 hours. So, **by not allowing you to get tech help from tutors, we are directing you to a more effective way to resolve those issues, while learning valuable skills at the same time**.
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

The DG is primarily meant to help current/future developers. In general, the DG is expected to provide minimal yet sufficient guidance  for developers, serving them in the following ways:

* It act as a starting point for developers, before they can dive into the code itself %%e.g., by providing an architecture-level overview of the system%%
* It provides a roadmap to developers %%e.g., pointing out where important information can be found in the code%%
* It complements the code, providing info/perspectives not specified in the code %%(e.g., rationale for high-level design choices, details of dev ops)%%<br>
  or not easy to grasp from the code %%(e.g., architecture level view, visual models)%%.

Therefore, decide based on how the inclusion/exclusion affects that target audience (you belong to the target audience too!) in achieving the above objectives.
</div>
=============================================================== -->
<div id="faq-tpChangeDirectionLater-Q">Can we change the product name, the target user, and the value proposition later in the project?</div>
<div id="faq-tpChangeDirectionLater-A">

Yes. If the project direction submission deadline (in week 6) is not over yet, use the same link to update the submission. If the submission deadline is over, email the updated name, target user, value proposition to `{{ course | lower }}@comp.nus.edu.sg`.
</div>
<!-- =============================================================== -->
<div id="faq-dgAddNewUml-Q">Is it enough to update existing UML content/diagrams or must we add new content/diagrams?</div>
<div id="faq-dgAddNewUml-A">

**You are welcome to add new content/diagrams**, but it is not a strict requirement. Consider costs %%(e.g., the effort required to add and maintain new content)%% vs benefits %%(how much the new content helps future developers)%% and decide accordingly.
**However, everyone is expected to contribute to the DG (and contribute to UML diagram updates)**, which means you should divide the DG-update work among team members.
</div>
<!-- =============================================================== -->
<div id="faq-noEffectOnUml-Q">What if the features I added don't affect UML diagrams?</div>
<div id="faq-noEffectOnUml-A">

* **We expect all students to have _some_ experience working with DG UML diagrams**, to verify that you are able to handle similar diagramming tools in the future.
* If your code changes don't require updates to existing UML diagrams or adding new diagrams,
  * you can document a 'proposed' feature or a design change that you might do in a future iteration, which gives you an opportunity to add some UML diagrams.
  * Also take a closer look at the features you added -- not needing changes to UML might (but not always) be a sign that the features you added didn't go deep enough. In the context of the tP, it is better to add one big feature, rather than add many small insignificant features.
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

~~GitHub Issues does not have a direct way of doing this. However, you can use a task list in the issue description to indicate sub-tasks and corresponding issues/PRs -- ([an example](https://github.com/MarkBind/markbind/issues/1774))~~

You can use [this recently-added GitHub feature](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues) to mark an issue as a sub-task of another issue.
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
<div id="faq-tpPrReviewRigor-Q">How thorough should the PR reviews be?</div>
<div id="faq-tpPrReviewRigor-A">

**Course admin perspective:** It's up to you. We do not directly enforce any requirement on this. How well you do this can affect your grade indirectly though e.g., if PR reviews are weak, low quality code could get merged, which can in turn affect grading for code quality and bugs in the product. If you 'overdo' PR reviews, you'll waste time/effort and slow down the progress, which can affect marks as well.

**Teaching/learning perspective:** Learning to optimize the _process_ is an intended learning outcome. You can do this iteratively. That is, the team can decide your own policy/process, and tweak it as you go. For example, you can decide to have a minimum of n reviews at rigor level X for each PR. After doing that for a while, you can evaluate how it is working, and tweak if necessary (reduce n or lower X if you feel like it is slowing down the project too much without helping to increase quality that much | increase n or set a higher X if you think the code being merged is below-par quality).

**SE perspective:** This depends on many things, such as target quality (higher target quality requires high rigor PR reviews), availability of reviewers, level of other quality assurance mechanisms in place (e.g., automated checks done on the code, such as Checkstyle). Might even vary based on type of PR (some PRs need closer scrutiny than others).

Should reviewer run the code locally to ensure the code works? This also depends on if (and how well) the work in the PR is covered by automated tests run by the CI.

Most long-running projects in real world will establish their own policies/norms, either written down formally or passed down informally (i.e., new devs follow what current devs do).

</div>
<!-- =============================================================== -->
<div id="faq-tpMultiStepCmd-Q">Why not allow user to input the command one field at a time?</div>
<div id="faq-tpMultiStepCmd-A">

While this _multistep-command_ approach (i.e., giving the user a series of prompts to enter various data elements required to perform an action) has its benefits (e.g., no need to memorize the command format), a deeper look reveals why the _one-shot-command_ approach is better.

Before delving any further, note how leading CLI-centric software such as Git and Linux don't use the multistep approach either. Why?

The multistep approach basically results in a 'text-based GUI simulation' that is harder to use than an actual GUI (obviously), whereas a well-designed CLI in an expert's hands can perform tasks faster than an equivalent GUI (which is what we are going for). A person good at typing and remembers the command can type a command faster than a user going through a type-read-type-read sequence required by the multistep-command. Now imagine user made a mistake in the response to an earlier prompt -- correcting that would take a lot more work.

That being said, multistep commands can complement the one-shot-command approach in specific cases e.g.,

* as a crutch for new users to learn the command format
* to be used for rarely-used tasks or tasks requiring multiple steps (e.g., importing data from a file)

</div>
<!-- =============================================================== -->
<div id="faq-tpRationaleForCurrentDesign-Q">When refactoring AB3 code, I would like to find the rationale for the current design; how do I do that?</div>
<div id="faq-tpRationaleForCurrentDesign-A">

First, kudos for wanting to find the rationale before you change the current design. It's a good application of the [Chesterton's Fence Principle](https://fs.blog/chestertons-fence/).

Some options:

1. See if the rationale is documented in the developer documentation or code comments.
1. Dig into the Git and GitHub history to find if there are any clues there e.g., commit message of the relevant commit, or the discussion in the relevant PR. Git _blame_ feature can help you locate the relevant commit.
1. Try to speculate the possible motives, get views from other developers.
1. These days, you can also ask AI tools.
1. Play it safe and delay the refactoring until you have worked with the code for a while, in case the reason becomes apparent after working with the code for a while.
1. Tentatively refactor it, to see the effect. Sometimes this helps you discover why the code was in the original form in the first place.
1. Go ahead and refactor it, but do it in a way it can be easily reverted later e.g., break the refactoring into a series of small/medium stand-alone design changes and do them as separate PRs (or separate commits) so that they can be reverted later, if needed.

</div>
<!-- =============================================================== -->
<div id="faq-tpEnoughFeatures-Q">If our team implement features x, y, and z, is that enough?</div>
<div id="faq-tpEnoughFeatures-A">

Yes, if it requires each member to put in an implementation effort that is about 50% of the implementation effort you put into the iP.
</div>
<!-- =============================================================== -->
<div id="faq-tpMustWrite300Loc-Q">Is it a must to write at least 300 LoC?</div>
<div id="faq-tpMustWrite300Loc-A">

Note that 300 LoC is neither a target, nor a cap, nor a definitive measure. In fact, LoC is not a very reliable measure of effort. So, it is just a secondary indicator you can refer to. The primary indicator you should keep an eye on is if your tP implementation effort, which is expected to be around 50% of the iP implementation effort.

So, the answer is, "not necessarily". It depends on the effort required, which in turn depends on what the code does. It is quite possible for 100 LoC that implements feature X to take more effort than 300 LoC that implements feature Y (i.e., it depends on the feature). So, we measure the effort, not LoC (LoC figure given is just a rough estimate of the _equivalent_ effort).

</div>
<!-- =============================================================== -->
<div id="faq-tpIsBlankLinesCounted-Q">300 LoC is with or without blank lines?</div>
<div id="faq-tpIsBlankLinesCounted-A">

It does not matter. Peg your implementation effort to about 50% of the implementation effort of the iP. Let the LoC number fall where it may. We grade based on the effort, not the LoC count. The given LoC number is just a secondary indicator only.

</div>
<!-- =============================================================== -->
<div id="faq-tpFullMarksFor300Loc-Q">Still, if I write 300 LoC, I get full marks for implementation?</div>
<div id="faq-tpFullMarksFor300Loc-A">

There is no such guarantee, for two reasons:

1. Your implementation effort is graded based on how much functionality your team produced (based on peer-testers' and tutors' estimates) and how much of that work was contributed by you (based on team members' estimates). For example, simply copy-pasting 400+ LoC with only minor modifications is unlikely to meet this bar as it is less than an effort _equivalent_ to writing a typical 300-400 LoC (or half of a typical iP effort).
1. Implementation marks are based on both effort and quality, the latter being the primary driver (more info <trigger trigger="click" for="modal:tPexpectations-implementationGrading">here</trigger>). So, meeting the effort bar doesn't guarantee full marks for implementation.
</div>
<!-- =============================================================== -->
<div id="faq-tpIsLocGraded-Q">Is LoC graded in the tP?</div>
<div id="faq-tpIsLocGraded-A">

LoC is not graded. But if there is a significant mismatch between the LoC numbers and the 'effort' rating a student received, we take a closer look at the case to find out the reason for the mismatch, and revise marks if necessary.
</div>
<!-- =============================================================== -->
<div id="faq-tpUncontactableMembers-Q">What if a member is not contactable?</div>
<div id="faq-tpUncontactableMembers-A">

Given below is the relevant section from [Appendix F: Handling Team Issues](appendixF-teamworkIssues.md):

<include src="appendixF-teamworkIssues.md#team-problems-mia-member" />
</div>
<!-- =============================================================== -->
<div id="faq-tpIterationDeadline-Q">What's the deadline for tP iterations?</div>
<div id="faq-tpIterationDeadline-A">

The deadline for tP iterations is the `Thursday 23:59` in the week it is due, unless a different date is specified in the instructions of that iteration.
</div>
<!-- =============================================================== -->
<div id="faq-tpMissingIterationDeadlines-Q">What if we overshoot the deadline for a tP iteration?</div>
<div id="faq-tpMissingIterationDeadlines-A">

It is OK %%(i.e., no penalty)%% if you overshoot the deadline in initial iterations. Adjust subsequent iterations so that you can meet the deadline consistently %%(which is an important learning outcome of the tP)%% by the time you reach the end of the tP.
</div>
<!-- =============================================================== -->
<div id="faq-tpV11Scope-Q">What should be in `{{ version_practice }}`? Just task {{ thumb_small("1") }} or all three tasks?</div>
<div id="faq-tpV11Scope-A">

Ideally, all three. But if you can't finish all three by the iteration deadline, you may push some of the task {{ thumb_small("2") }} and {{ thumb_small("3") }} work to the following iteration (i.e., `{{ version_first }}`).
</div>
<!-- =============================================================== -->
<div id="faq-tpHowMuchToGetFullMarks-Q">How much code/features is enough to get full marks?</div>
<div id="faq-tpHowMuchToGetFullMarks-A">

Not surprisingly, a common question tutors receive is "can you look at our project and tell us if we have done enough to get full marks?". Here's the answer to that question:

**The tP _effort_ is graded primarily based on peer judgements** (tutor judgements are used too). That means you will be judging the effort of another team later, which also means you should be able to make a similar judgement for your own project now. While we understand effort estimating is hard for software projects, it is an essential SE skill, and we must practice it when we can.

**The expected minimum bar to get full marks for _effort_** is given [here](tp-expectations.md).

If you surpass the above bars (in your own estimation), you should be in a good position to receive full marks for the effort. But keep in mind that there are many other components in the [tP grading](tp-grading.md), not just the effort.
</div>
<!-- =============================================================== -->
<div id="faq-tpNotEnoughWorkToDivide-Q">What if the chosen user stories for MVP is not enough to do a meaningful work division among team members?</div>
<div id="faq-tpNotEnoughWorkToDivide-A">

In that case, at a later stage, you can add more user stories until there is enough for a meaningful work distribution. But at this point focus on selecting the smallest sub-set of _must_have_ user stories only.
</div>
<!-- =============================================================== -->
<div id="faq-tpNotEnoughMvpFeaturesToDivide-Q">What if the MVP feature list is smaller than team size? How to divide work?</div>
<div id="faq-tpNotEnoughMvpFeaturesToDivide-A">

In that case, you can add more features, taking higher priority features from the features not-yet-selected for the MVP.
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
<div id="faq-tpCodecovFails-Q">PR CI fails because Codecov reports a drop in code coverage. What to do?</div>
<div id="faq-tpCodecovFails-A">

In some cases the code edited by the PR is not covered by existing tests, which means Codecov will report it as not adhering to the current coverage targets.

First, find out which area of the code is causing the coverage drop. You can use Codecov or code coverage features of the IDE to do so.

Then you can do the following:

* Ignore those warnings, and merge the PR (a member with admin permissions can merge a CI-failing PR). Suitable for cases such as,
  * the coverage drop is in code that is not normally covered by automated tests and/or 'not worth the effort to' test automatically (e.g., GUI).
  * you deem that automated testing of that part of the code can be done at a later time (i.e., not a priority at the current time).
* Alternatively, update tests until the coverage is raised back to  sufficient level.

Note that Codecov is there to help you manage code coverage -- it is not graded. You may lower the test coverage targets set for Codecov as well.

For reference,

{{ embed_topic("tp-expectations.md#testing-expectations", "Admin " + icon_embedding + " tP → Grading → **Expectation on testing**", "3", indent="1") }}
</div>
<!-- =============================================================== -->
<div id="faq-tpIsCiPassingCompulsory-Q">Is it compulsory to keep CI passing?</div>
<div id="faq-tpIsCiPassingCompulsory-A">

Among other things, CI functions as **a safety mechanism that alerts you when a PR is introducing regressions to the codebase**. If your CI is failing continuously, you will lose the benefit of this important safety mechanism.

Therefore, if you break CI accidentally (or even deliberately -- e.g., CodeCov dropping due to changes in an 'untestable' part of the code), **we recommended that you get CI back to a passing state** soon after.

There is no direct penalty for occasionally failing CI. But #r#extended periods of CI failures can cost you marks directly or indirectly## (e.g., the failure could be due to a coding standard violation that can cost you marks if not fixed).
</div>
<!-- =============================================================== -->
<div id="faq-tpAddChangesInFeatureBranch-Q">Can we PR against a branch other than `master`, and merge that branch to `master` in a later iteration?</div>
<div id="faq-tpAddChangesInFeatureBranch-A">

While doing PRs against a separate 'feature branch' is not explicitly prohibited, it is discouraged because the longer you keep evolving a feature away from the main code base, the more,

* it brings in elements of a _depth-first iterative_ approach (instead of the intended _breadth-first iterative_ approach). Although technically you are doing multiple features in parallel, they are not synchronized with each other.<br>
  Note: **The ability to divide implementation work into small breadth-first incremental changes is one of the important intended learning outcomes we are aiming for** -- even more important than the mechanics of following the workflow correctly. Using feature branches is not aligned with this learning outcome.
* it moves towards [_big-bang integration_]({{ baseUrl }}/book/integration/approaches/bigBangVsIncremental/) (instead of the intended _incremental integration_) and [_late-and-one-time integration_]({{ baseUrl }}/book/integration/approaches/lateVsEarly/) (instead of the intended _early-and-frequent_ integration). Although you feature branch is running CI at each commit, when you integrate feature branches to the `master` branch at a later time, it can result in a 'big bang'.

So, even if you use feature branches,

* do it in moderation (not as the standard practice), only when you feel it is necessary.
* merge the feature branch to the `master` branch frequently, ==at least once per iteration==.<br>
  Note that only commits merged to the master branch will be recognized by the grading scripts.
* keep them synced with the latest `master` branch i.e., merge the `master` branch to the feature branch whenever there are new commits in the `master` branch.
</div>
<!-- =============================================================== -->
<div id="faq-tpTestsForTutorial-Q">When doing this tP tutorial, do we have to write/update test cases too?</div>
<div id="faq-tpTestsForTutorial-A">

Not a strict requirement, but given the purpose of this tutorial is to learn the codebase, it's ideal if you do. It will familiarize you with the existing testing infrastructure. Otherwise, you can run into difficulties when you are writing test cases for your own features later.
</div>
<!-- =============================================================== -->

<div id="faq-tpChangeFeatureSpec-Q">Are we allowed to deviate from the MVP Feature Specification submitted earlier?</div>
<div id="faq-tpChangeFeatureSpec-A">

Yes, the submitted _MVP Feature Specification_ is not binding (its purpose was to get you to think about feature details early -- we will not be looking at it again). You may change features as needed along the way. Just ensure your changes do not violate [tp constraints]({{ baseUrl }}/admin/tp-constraints.html).

No need to resubmit the Feature Spec either. However, if you change the product name, target user, or the value proposition, (which is allowed too) please email the updated values to `{{ course_email }}`.
</div>
<!-- =============================================================== -->

<div id="faq-tpHowManyFeaturesInMvp-Q">How many features should we put in the MVP?</div>
<div id="faq-tpHowManyFeaturesInMvp-A">

Aim for the _smallest set of features the product cannot do without_. Even a most basic version of those features is enough. After completing that feature set, you can add more if there is time left.
</div>
<!-- =============================================================== -->

<div id="faq-tpNeedForNewFeatureInMvp-Q">Is it a requirement for the MVP to have 'new' features not currently in AB3?</div>
<div id="faq-tpNeedForNewFeatureInMvp-A">

No, there is no such need. The MVP features can be same as, or a subset of, AB3 features.
</div>
<!-- =============================================================== -->

<div id="faq-tpAb3FeatureInMvpSpec-Q">Do we need to include existing AB3 features in the MVP feature spec?</div>
<div id="faq-tpAb3FeatureInMvpSpec-A">

Yes, even if you don't plan to change them.

Reasons:

* To show that you have examined, understood, and agree with, the current behavior of those features.
* AB3 does not have a feature spec covering those features (and the UG does not cover all details of a feature).

But you may copy-paste parts of the UG onto your feature spec if that helps.
Also, you may omit existing AB3 feature that are not _must-have_, and hence, need not be included in the MVP.

</div>
<!-- =============================================================== -->

<div id="faq-githubIssuesMultipleDocAuthors-Q">When all members are updating the same document, can we create one issue and assign it to all?</div>
<div id="faq-githubIssuesMultipleDocAuthors-A">

**A:** In the tP (in which our grading scripts track issues assigned to each member), it is better to create separate issues so that each person's work can be tracked separately. For example, suppose everyone is expected to update the User Guide (UG). You can create separate issues based on which part of the UG will be updated by which person e.g., `List-related UG updates` (assigned to John), `Delete-related UG updates` (assigned to Alice), and so on.
</div>
<!-- =============================================================== -->

<div id="faq-tpEncryptDataFile-Q">Is it OK to encrypt the data file?</div>
<div id="faq-tpEncryptDataFile-A">

  Generally, not recommended. It can be allowed only if the application provides an easy way to decrypt the file, and encrypt it again after editing it manually.

  Followup question: What if the data in the file is confidential, and therefore, it is risky to leave it in plaintext format?<br>
  While this is a valid concern, you can assume/require that the app is used in a secure environment in which data are protected by default e.g., a personal computer already password protected.

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

**In very early iterations,** ==try to keep the existing tests (and CI) working==. It is OK not to add new tests.

**In general,** there are several options you can choose from:

1. Update/add tests every time you change functional code. This is what normally happens in stable production systems. For example, most OSS projects will not accept a PR that has failing tests or not enough new tests to cover the new functional code.
2. Disable failing tests temporarily until the code is stable. This is suitable when the functional code is in a highly volatile state (e.g., you are still experimenting with the implementation). The benefit is that you avoid the cost of writing tests for functional code that might change again soon after. Some costs: (a) harder to detect regressions during the period tests are disabled (b) testing debt piles up which could distort your estimate of real progress (c) forgetting to enable the tests in time.<br>
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

<div id="faq-tpMustWeFixAllBugs-Q">Must we fix all bugs reported and all enhancements suggested by testers?</div>
<div id="faq-tpMustWeFixAllBugs-A">

Not necessarily. Choose based on importance.

In any project, there are always things that can be done 'if there was more time'. If fixing a certain bug has low impact on users, and fixing it is not as important as the work done (or intend to do in the current iteration), you can justify not fixing it with the reason 'not in scope' of the current iteration.

Similarly, a missing feature enhancement can be justified as 'not in scope' if implementing that could have taken resources away from other important project tasks.

Bugs and possible enhancements 'not in scope' will not be penalized.
</div>
<!-- =============================================================== -->

<div id="faq-tpDgKeepingProposedFeatures-Q">Can we remove 'proposed features' sections in the DG?</div>
<div id="faq-tpDgKeepingProposedFeatures-A">

Yes, you may remove them, but you are welcome to keep them too (they can be useful if a team member is unable to find any other UML diagram to update).

If you keep them in the DG, update them to match the current version of the product. Otherwise, outdated content can be reported as DG bugs.

</div>
<!-- =============================================================== -->

<div id="faq-tpCountingSimilarPlannedEnhancements-Q">When listing 'Planned Enhancements' in the DG, if enhancement X and Y are very similar, can we count them as one?</div>
<div id="faq-tpCountingSimilarPlannedEnhancements-A">

Only if adding one automatically adds the other. If one can be added without the other, they are counted as two enhancements.
</div>
<!-- =============================================================== -->

<div id="faq-tpFeatureTakeovers-Q">What if someone took over a feature from another team member?</div>
<div id="faq-tpFeatureTakeovers-A">

In terms of effort distribution, it's up to the team to tell us who did how much. Same goes for assigning bugs. So, it's fine for someone to take over a feature if the team is able to estimate the effort of each member, and they have a consensus on who will be responsible for bugs in that feature.<br>
For code authorship, only one person can claim authorship of a line, and that person will be graded for the code quality of that line. By default, that will be the last person who edited it (as per Git data) but you can [override that behavior using `@@author` tags](tools.html#tool-reposense-for-authorship-tracking).
</div>
<!-- =============================================================== -->

<div id="faq-tpFeatureDesignChoice-Q">How to choose between feature design choices?</div>
<div id="faq-tpFeatureDesignChoice-A">

Product design is hard (harder than programming). Feature design choices %%(e.g., to support sorting or not support sorting, sort descending or ascending, which sort order should be default, etc.)%% are subjective and is case-by-case.

General guidance: Choose by considering<br>
 **[A] what is best for the user** (specifically, with reference to the target user profile you chose for the product), but also factor in<br>
 **[B] what is _possible_ within your resources** (e.g., time, manpower, expertise) -- what is 'ideal' may not be practical.

**Implications for the practical exam (PE):**

<div class="indented-level1">

Keeping in mind that during the PE testers can file bug reports against design choices, whatever choice you make, be prepared to justify your choice (based in [A] and [B] above) in case a tester filed a bug report objecting to the current design.

Given these justifications are subjective, if both the developer's justification and the tester's justification seems to be equally valid, we will rule in favor of the developer (i.e., no penalty for the developer).

However, if the dev team went with an inferior choice while another superior choice could have been taken using roughly the same amount of resources, the current design choice is flawed. %%For example, if 'sorting items in ascending order by default' is clearly the better choice, but the dev team chose descending order to be the default, assuming implementing either order takes roughly the same amount of resources, the dev team's design choice is flawed.%%

</div>
</div>
<!-- =============================================================== -->

<div id="faq-tpHowMuchCodeInV12-Q">How much code changes is 'enough' for this iteration?</div>
<div id="faq-tpHowMuchCodeInV12-A">

The bar is, each member to merge at least one PR containing functional code changes. The more you do in the current iteration, the less you need to do in future iteration. So, try to do as much as your time/resources allow. But the more important thing in `{{ version_first }}` is to do those changes in small steps, without breaking the codebase.
</div>
<!-- =============================================================== -->

<div id="faq-tpDivideByComponent-Q">Is it OK if different members modified different components?</div>
<div id="faq-tpDivideByComponent-A">

No, we advise against that. Instead, divide the work based on features/enhancements instead of components.
But you should still allocate different members to be 'in charge of' different components.
</div>
<!-- =============================================================== -->

<div id="faq-tpOtherDiagrammingTool-Q">Instead of PlantUML, can I use some other tool?</div>
<div id="faq-tpOtherDiagrammingTool-A">

Yes, you may use any other tool too (e.g., PowerPoint). But wait; if you do, note the following:

* ==Choose a diagramming tool that has some 'source' format that can be version-controlled using git and updated incrementally== %%(reason: because diagrams need to evolve with the code that is already being version controlled using git)%%. For example, if you use PowerPoint to draw diagrams, also commit the source PowerPoint files so that they can be reused when updating diagrams later.
* Use the same diagramming tool for the whole project, except in cases for which there is a _strong_ need to use a different tool due to a shortcoming in the primary diagramming tool. %%Do not use a mix of different tools simply based on personal preferences.%%

So far, PlantUML seems to be the best fit for the above requirements.
</div>
<!-- =============================================================== -->

<div id="faq-tpIdeGeneratedDiagrams-Q">Can <tooltip content="i.e., automatically reverse engineered from the Java code">IDE-generated</tooltip> UML diagrams be used in project submissions?</div>
<div id="faq-tpIdeGeneratedDiagrams-A">

Not a good idea. Given below are three reasons each of which can be reported by evaluators as 'bugs' in your diagrams, costing you marks:

* They often don't follow the standard UML notation (e.g., they add extra icons).
* They tend to include _every_ little detail whereas we want to limit UML diagrams to important details only, to improve readability.
* Diagrams reverse-engineered by an IDE might not represent the actual design as some design concepts cannot be deterministically identified from the code %%e.g., differentiating between multiplicities `0..1` vs `1`, composition vs aggregation%%.
</div>
<!-- =============================================================== -->

<div id="faq-tpLowMidtermPeerEvaluations-Q">What if I don't agree with the tP peer evaluations I received for the midterm peer evaluation?</div>
<div id="faq-tpLowMidtermPeerEvaluations-A">

This round is for your info only (i.e., no direct impact on grades). After the final tP peer evaluation session (which is done at the end of the semester, and can affect the tP grading) results are published, you will get a chance to submit your objections if you don't agree with the evaluations you received.

{{ icon_tip }} Receiving ‘lower than expected’ feedback early is actually a good thing. It highlights the areas where your team members are less satisfied with your contribution or conduct, while there is still time to take corrective action. What is far worse is when team members give positive ratings for aspects they are unhappy about — just to avoid conflict — and hold back negative feedback until the project ends. In such cases, you may be caught off guard (“Hey! I thought everything was fine!”) with no time left to address the problem.
</div>
<!-- =============================================================== -->

<div id="faq-tpGuiTestAutomation-Q">Should we try to automate GUI testing as well?</div>
<div id="faq-tpGuiTestAutomation-A">

Automated GUI testing is hard, especially in Desktop apps, especially in CI (because the environment that CI runs doesn't have a display device to show the GUI).

A few years ago, we used [AB4](https://github.com/se-edu/addressbook-level4/) as the starting point of the tP.

* The main difference between AB4 and AB3? AB4 has automated GUI testing. It used the TestFX tool to do so, and ran the test in 'headless' mode in CI (i.e., simulate a display device without an actual display device).
* The main reason we changed tP to start with AB3 code was that some students found it too hard to maintain those GUI tests.

While we don't require you to automate GUI testing in your tP (i.e., it is fine to do only manual GUI testing), you are welcome to give it a try too, especially if you like a technical challenge.

* Even if you get it working in only some OS'es only, and only in local environment, it is still a useful way to test the GUI quickly.
* It is possible to run tests selectively, which means you can still run them in environments they work and skip them in other environments.

Feel free to reuse/refer AB4 code too. If you manage to make some headway in this direction, you are encouraged to share it with others via the forum.
</div>
<!-- =============================================================== -->

<div id="faq-tpWorksLocallyFailsCi-Q">All tests pass locally, but the same code fails CI in the PR. How come?</div>
<div id="faq-tpWorksLocallyFailsCi-A">

First, check which OS it is failing in. Some behaviors can be OS-dependent. For example, file paths are case-insensitive in Windows but not in Unix/Mac.

Second, note that PR CI does a temporary merge of `master` branch to the PR branch before running tests, to verify if the checks will pass _after_ you merge this PR. So, if the `master` branch has progressed after you started your PR branch, those new commits can affect the CI result. The remedy is to pull the `master` branch to your repo, merge it to your PR branch, and run tests again (which should fail as well, but you can now find the reason for the failure and fix it).
</div>

<div id="faq-tpPrPassCiButFailedAfterMerging-Q">PR passed CI before merging, but fails CI after merging. How come?</div>
<div id="faq-tpPrPassCiButFailedAfterMerging-A">

It is possible that the `master` branch has received new commits after your PR passed CI the last time. So, if GitHub indicates that your PR is not up-to-date with the latest `master` branch, synchronize your PR branch with the `master` branch (which will run the CI again) before merging it.
</div>
<!-- =============================================================== -->

<div id="faq-tpRenameAbReferences-Q">Do we need to change all class/package names that refer to AB3?</div>
<div id="faq-tpRenameAbReferences-A">

Given your product is supposed to be an address book variant, it is fine to keep using 'AddressBook' in class/package names.<br>
But remember to change any user-visible mention of AddressBook at places where the user _expects_ to see the name of your product, and will be confused by seeing a different name instead.

Caution: Mass renaming can disrupt authorship tracking. So, it is best to do any mass renaming at earlier stages of the tP (but you are still _allowed_ to rename them even at later stages).
</div>
<!-- =============================================================== -->

<div id="faq-peTooLong-Q">Isn't it unreasonable to expect us to spend so many hours for the PE/PE-D?</div>
<div id="faq-peTooLong-A">

The product testing part of the PE (and the PE-D) is expected to take no more than 2 hours. Typically, the bugs you can find within 2 hours should be enough to get full marks for the product testing component of the tP. The additional time is given as a buffer, and to reduce stress.

Note that you can send no more than 6 bugs to the dev team anyway, and the product testing is only a small component of tP marks (i.e., 3-4 marks). So, there is not much value spending too long on this.

</div>
<!-- =============================================================== -->

<div id="faq-peOtherCommitments-Q">Isn't it unfair to students who have other committments during the PE/PE-D period?</div>
<div id="faq-peOtherCommitments-A">

The product testing part of the PE (and the PE-D) is expected to take no more than 2 hours, and hence, can be done during the lecture slot of the course.
</div>
<!-- =============================================================== -->

<div id="faq-peMorePowerfulTools-Q">Will students using more powerful (e.g., paid) tools for testing will have an unfair advantage?</div>
<div id="faq-peMorePowerfulTools-A">

Given the nature of the product you are testing (small, simple), we expect that everyone will be able to find enough bugs to qualify for full marks for the product testing portion of the tP, even if you are not using any tools at all (i.e., manual testing only). At this scale, and at the current state of the art, we estimate the difference between using AI tools and manual testing to be negligible.
</div>
<!-- =============================================================== -->

<div id="faq-tpTestingLessBuggyProducts-Q">Some students will be testing less/more buggy products than others? Isn't that unfair?</div>
<div id="faq-tpTestingLessBuggyProducts-A">

As each product is tested by 4-5 testers, after all PE bugs have been finalized, we know how 'buggy' each product is. We then use that information for calculating your PE-related marks. So, the marks are calibrated to match the bugginess of the product you tested.
</div>
<!-- =============================================================== -->

<div id="faq-tpNoBugsInTestedProduct-Q">What if the product I tested has hardly any bugs?</div>
<div id="faq-tpNoBugsInTestedProduct-A">

If the total bugs found (by _all_ testers) in a product is below a certain level, we compensate those testers by increasing the weightage given to PE-D performance, and their dev-testing results.
</div>
<!-- =============================================================== -->

<div id="faq-tpNeedToFindAllBugs-Q">Am I expected to find the {{ tp_pe_bug_count }} highest severity bugs in the entire product, among _all_ bugs in the product?</div>
<div id="faq-tpNeedToFindAllBugs-A">

It is too much to expect you to first find _all_ bugs in the product (which could take a long time if the product is very buggy) and then choose the {{ tp_pe_bug_count }} most severe among them. To get full marks, you only need to have a certain percentage of those bugs among the {{ tp_pe_bug_count }} bugs you report. For example, suppose a product received 10 Medium/High severity bugs -- you could be given full marks if you have at least 3 of them among your {{ tp_pe_bug_count }} bugs. Even if you don't meet that bar, you still earn marks based on the bugs you've reported.
</div>
<!-- =============================================================== -->

<div id="faq-peCanTestersCombineBugs-Q">Can a tester combine multiple similar bugs into a single bug report?</div>
<div id="faq-peCanTestersCombineBugs-A">

**In the PE-D**, it is OK to do so.

**In the PE**, report each bug as a separate bug report. If you include multiple bugs in one bug report, the dev team is allowed to pick one bug out of them and discard the rest.

* Reasons:
  * It is hard to evaluate when multiple bugs are in the same report e.g., what if some of them are valid but others are not?
  * It can open the door for testers to define very high-level bugs %%(e.g., UG not well-formatted)%% and cramming more and more bugs into one bug report. It is hard to define what's acceptable in such cases.
  * Given these are lower-severity bugs, it is better to report them once and focus more on looking for higher-severity bugs.
* On the positive side, if similar bugs reported (even by multiple testers) are later combined into one bug report by the dev team (with our permission) and given a higher severity, all testers who reported instances of that bug will benefit from the higher severity.
</div>
<!-- =============================================================== -->

<div id="faq-peVaguePlannedEnhancements-Q">What if a 'Planned Enhancement' is written broadly so that it covers a variety of bugs?</div>
<div id="faq-peVaguePlannedEnhancements-A">

As per our instructions, each planned enhancement should be specific and detailed. If you feel a certain planned enhancement is too broad or not specific enough, you can 'reject' that planned enhancement and still report bugs as if it didn't exist. But in this case you should also justify why you 'reject' the corresponding planned enhancement.
</div>
<!-- =============================================================== -->

<div id="faq-tpJustifyBugsAcceptedAsIs-Q">Do we need to justify even if we accept the bug _as is_?</div>
<div id="faq-tpJustifyBugsAcceptedAsIs-A">

No need to provide a justification if you accept the bug without _any_ changes to it.
</div>
<!-- =============================================================== -->

<div id="faq-tpMoreCodeMeansHigherPenalty-Q">So, those who write more code will be hit with more bugs? How's that fair?</div>
<div id="faq-tpMoreCodeMeansHigherPenalty-A">

Penalty for bugs is applied based on bug _density_, not bug count. Here's an example:

* `n` bugs found in Ann's feature; it is a big feature consisting of a lot of code → marks for dev testing: 4
* `n` bugs found in Jim's feature; it is a small feature with a small amount of code → marks for dev testing: 1

Although both had the same number of bugs, as Ann's work has a lower bug density than Jim's, she earns more marks for the dev testing aspect.
</div>
<!-- =============================================================== -->

<div id="faq-tpRealBugWrongLabel-Q">What if the bug is real but the tester used the wrong label (e.g., used the wrong `type.*`). Can we reject that bug?</div>
<div id="faq-tpRealBugWrongLabel-A">

A bug is a bug irrespective of the label used. Instead of rejecting, rectify the label.
</div>
<!-- =============================================================== -->

<div id="faq-tpCorrectBugIncorrectSuggestion-Q">What if the bug the tester reported is legit but the expected behavior tester suggested is not correct?</div>
<div id="faq-tpCorrectBugIncorrectSuggestion-A">

You should accept the bug but state that you disagree with the expected/suggested behavior. Reason: the main job of the tester is to detect bugs; suggesting a solution is optional.
</div>
<!-- =============================================================== -->

<div id="faq-tpBugRejectedWithReason-Q">What if the team rejected my bug report without giving a reason?</div>
<div id="faq-tpBugRejectedWithReason-A">

You can disagree with the rejection, and the teaching team will likely rule in your favor in the next phase.
</div>
<!-- =============================================================== -->

<div id="faq-tpTesterAddingMoreInfoLater-Q">Can I (i.e., the tester) add more information about the bug when I object to a dev team's response?</div>
<div id="faq-tpTesterAddingMoreInfoLater-A">

Yes, you may. Given that the dev team did not get to see this additional info when they triaged the bug, the weight such additional info adds to your case is lower than if you had that info in the initial bug report. Nevertheless, it can still help your cause, especially if the dev team should have thought about that info on their own, even if they were missing in the initial bug report.
</div>
<!-- =============================================================== -->

<div id="faq-tpPeAccuracyForNotInScope-Q">If the bug I reported is `NotInScope`, how does it affect my accuracy bonus?</div>
<div id="faq-tpPeAccuracyForNotInScope-A">

A bug that is `type.Accepted` or `type.NotInScope` can boost your accuracy if the `severity.*` you chose matches the eventual `severity.*` of the bug. ~~Same for `type.*`~~ (the `type.*` will not be considered for accuracy).
</div>
<!-- =============================================================== -->

<div id="faq-tpPeNotInScopeSeverity-Q">If a bug is `NotInScope`, does the `severity.*` label still matter?</div>
<div id="faq-tpPeNotInScopeSeverity-A">

Yes. A higher severity means the enhancement you suggested is of higher value/importance; you earn more credit for doing so.
</div>
<!-- =============================================================== -->

<div id="faq-faqid-Q"></div>
<div id="faq-faqid-A">


</div>
<!-- =============================================================== -->


<!-- ===============================================================
  Exam FAQ
=============================================================== -->

<!-- =============================================================== -->
<div id="faq-examIsXyzInScope-Q">Is ____ in the scope of the exam?</div>
<div id="faq-examIsXyzInScope-A">

Aspect | Is in the scope?
-------|------------------
External pages hyperlinked from the [examinable version of the textbook]({{ url_course_website }}/se-book-adapted/print.html) e.g., eXtreme Programming website | No.
Content listed in _Resources_ panels | No.
Book titles and authors mentioned e.g., The Mythical Man-Month by Fred Brooks | No.
Refactoring and code 'smells' listed under the topic [Refactoring]({{ url_course_website }}/se-book-adapted/chapters/refactoring.html) | You should be able to cite examples of refactorings and code smells but their details will not be tested

</div>
<!-- =============================================================== -->
<div id="faq-examGradingFollowUpQuestion-Q">How is the follow-up question graded?</div>
<div id="faq-examGradingFollowUpQuestion-A">

In most cases the answer to the follow-up question is used to decide if you chose the right answer for the right reasons. Choosing the right answer for the wrong reasons will not earn you marks.

In rare cases the answer to the follow-up question can be used to give partial marks for choosing the wrong answer (e.g., the second-best answer), if it shows your reasoning was mostly correct, although you ended up choosing the wrong answer.
</div>
<!-- =============================================================== -->
<div id="faq-examMissedFollowUpQuestion-Q">What if I accidentally clicked `Next` before answering the follow-up question?</div>
<div id="faq-examMissedFollowUpQuestion-A">

In that case you will not be able to go back to type the answer, because our exam does not allow backward navigation.<br>
Not to worry. We realise that this can happen under exam pressure. Therefore, we will overlook up to two missing/incorrect answers to follow-up questions. This also means if the timer is running out, it may be OK to skip the follow-up question in the last two questions.
</div>
<!-- =============================================================== -->
<div id="faq-examPartialMarksForMsq-Q">Do I get partial marks for checkbox style questions?</div>
<div id="faq-examPartialMarksForMsq-A">

Yes, you get half the marks if your answer is only off-by-one.

For example, if the answer is [A,B],

* [A, B]: full marks
* [A] or [B]: half marks, because only one correct answer missing
* [A,B,C], [A,B,D] etc.: half marks, because only one incorrect option selected
* [A,C], [B,C], [A,D] etc.: half marks, because only one selected answer is incorrect
* [A,B,C,D]: no marks, because two incorrect options selected
* [A,C,D]: no marks, because one correct answer missing and one incorrect option selected
</div>
<!-- =============================================================== -->
<div id="faq-examSitNearChargingPoint-Q">My laptop battery is weak. Can I be put in a seat near a charging point?</div>
<div id="faq-examSitNearChargingPoint-A">

The standard operation procedure for digital exams: Some venues have charging points within reach of every seat. If that's not the case, you will be moved to another location with a charging point when your laptop power level reaches a low level. Pre-allocating you a seat with a charging point is not feasible, as the number of such requests can easily exceed the number of charging points in the venue.
</div>
<!-- =============================================================== -->
<div id="faq-examMorePastPapersAndAnswers-Q">Can we have more past year papers and model answers?</div>
<div id="faq-examMorePastPapersAndAnswers-A">

You are welcome to try past exam papers available in the library and post answers in the forum to discuss with others. The teaching team will contribute to those discussions as well, and ensure you reach a reasonable answer.

Caution: The scope of the course and the exam format evolve over time and some past questions may not be exactly in sync with the current semester. The format of the archived exam papers is different from the current format.
</div>
<!-- =============================================================== -->
<div id="faq-examWhyNoBackwardNavigation-Q">WHAT? Why aren't we allowed to go back to previous questions?</div>
<div id="faq-examWhyNoBackwardNavigation-A">

**Reasons:**

1. **To minimize opportunities for collusion or over-the-shoulder copying** from others (the risk of the latter is higher in this type of exam due to the upright exam device screens being easily visible to other exam takers).<br>
1. **Not unreasonable for the materials tested, nature of the questions, and the proficiency level expected** -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion, nor will you be able to 'answer the easy questions first and come back to harder questions later'.<br>
  Note that you are allowed to go back and modify diagrams you drew in part 1, just like in a real life project scenario.

Not to worry; we understand that this restriction can make the exam feel 'harder' than otherwise. We have the following **measures to compensate:**

* **There is a buffer of two extra questions**, to cushion the impact of making a mistake in question, realizing it later, and not being able to go back to fix it. {{ bullet_tick_green }}
* **There is a buffer of six extra minutes** (on top of the two extra questions), to cushion the impact of needing to spend extra time on a question to ensure the answer is correct before moving to the next question.
* **The question difficulty is calibrated to match this mode of testing** i.e., the questions are easy enough that can be done one shot in a short time.
* **Our tutorials prepare you for this mode of testing** (provided you do them sincerely), as our tutorials get you to answer a series of small MCQ-like questions and short-answer questions.
</div>

<!-- =============================================================== -->