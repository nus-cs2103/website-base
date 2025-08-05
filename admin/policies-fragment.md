{% from "common/macros.njk" import embed_topic, show_faq with context %}
<div id="policy-adminQuestions" tags="m--cs2103" >

**All admin questions should be sent to the course email `{{ course | lower }}@comp.nus.edu.sg` or posted in the [forum]({{ url_forum }}).** This way, the person in charge of that admin detail will answer you.

==#r#Do not ask admin questions from tutors##== (in person or via other means) as **tutors are prohibited from answering admin questions**.

{{ show_faq("tutorialWhyTutorsCannotAnswerAdminQuestions") }}

Examples of admin questions:

* What happens if I don't submit by the deadline?
* How is this graded?
* Can I use X instead of Y for the project?
* Where can I find details about [some aspect of the course]?

</div>

<div id="policy-teamSize">

As most of the work is graded individually, team sizes of 4/5/6 are not expected to affect your grade. For example, while managing larger teams is harder, larger teams have more collective know-how, which can cancel each other. However, we give some special consideration when grading 3-person teams.

</div>

<div id="policy-followingInstructions">

When working with others, especially in a large class such as {{ course_pair }}, it is very important that you adhere to standards, policies, and instructions imposed on everyone. Not doing so creates unnecessary headaches for everyone and puts your work attitude in a negative light. That is why we penalize repeated non-compliance of instructions. On the other hand, we do understand that we all are liable to make mistakes. That is why we only penalize repeated or frequent mistakes.

</div>

<div id="policy-workDistribution">

As most of the work is graded individually, it is OK to do less or more than equal share in your project team.

{{ embed_topic("tp-expectations.md#individualExpectations", "Admin " + icon_embedding + " tP → Expectations: from each student", "3") }}
<p/>
</div>

<div id="policy-validAbsences">

* **An occasional absence or two will not affect your marks**, as the marking scheme already has built-in buffers to absorb such occasional absences/lapses. If you miss a {{ lecture_name_short }}/tutorial/task for a valid reason (e.g., MC, LOA, official university event, officially representing NUS in a competition), just do your best to catch up.{texts="['a)', 'b)', 'c)']"}
* **Let us know only if you failed to earn full marks for participation due to such a reason** (or if you feel you are at risk of not earning full marks), in which case we will consider giving an alternative avenue to earn marks missed due to the absences.<br>
 Detail of participation marks calculation is [here]({{ baseUrl }}/admin/participation.html).
* **Normally, there is no need to inform us** (e.g., the tutor) of such absences or the reason, although you are welcome to.<br>
  **No need to send us your MC** (it is best not to share your health information with others, unless necessary), but keep a copy  of it safely, in case we ask for it later, in relation to (b) given above.
</div>

<div id="policy-responseTime">

**Normally, the prof will respond within 24 hours** if it was an email sent to the prof or a forum post directed at the prof. If you don't get a response within that time, **please feel free to remind the prof**. It is likely that the prof did not notice your post or the email got stuck somewhere.

Similarly, we expect you to check email regularly and respond to emails written to you personally (not mass email) promptly.

<panel header="Email etiquette: ALWAYS respond to direct emails" expanded>

Not responding to a personal email is a major breach of professional etiquette (and general civility). Imagine how pissed off you would be if you met the prof along the corridor, said 'Hi prof, good morning' and the prof walked away without saying anything back. Not responding to a personal email is just as bad. Always take a few seconds to at least acknowledge such emails. It doesn't take long to type "Noted. Thanks" and hit 'send'.

The promptness of a reply is even more important when the email is requesting you for something that you cannot provide. Imagine you wrote to the prof requesting a reference letter and the prof did not respond at all because he/she did not want to give you one; You'll be quite frustrated because you wouldn't know whether to look for another prof or wait longer for a response. Saying 'No' is fine and in fact a necessary part of professional life; but saying nothing is not acceptable. If you didn't reply, the sender will not even know whether you received the email.

</panel>
<p/>

</div>

<div id="policy-techHelp">

**Do not expect your tutor to code or debug for you**. We strongly discourage tutors from giving technical help directly to their own teams because we want to train you in troubleshooting tech problems yourselves. Allowing direct tech help from tutors transfers the troubleshooting responsibility to tutors.

**It is ok to ask for help from classmates even for assignments**, even from other teams, as long as you don't copy from others and submit as your own. The preferred way for this is to ask in the [forum]({{ url_forum }}) rather than privately, as (1) it gives others an opportunity to benefit as well (2) the teaching team can confirm the accuracy of the help you are receiving.

**We encourage you to give tech help to each other**, but do it in a way that the other person learns from it.

<span class="flat">%%Related: [[Admin: Appendix D: Getting Help](#admin-appendixD-help-anchor)]%%</span>

{{ embed_topic(baseUrl+"/admin/appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: How to get Help in " + course_pair, "3") }}
<p/>
</div>

<div id="policy-publishingSubmissions">

The source code are publicly available and are available for reuse by others without any restrictions.
Is publishing submissions unfair to the author? We don't think so. If you were the first to think of something your peers are willing to adopt later, that means you are already ahead of them and they are unlikely to earn more marks by adopting your ideas.

</div>

<div id="policy-plagiarism">

**We encourage sharing, but you should share with everyone in the class**, not just a selected group. That is,

* You are not allowed to share individual assignments with classmates directly.
* You are not allowed to share project-related things with other teams directly.

If you submit code (or adopt ideas) taken from elsewhere (**you can even reuse each other's work**), you need to comply with our reuse policy.

Detection:

* Detecting plagiarism in code is quite easy. You are not fooling anyone by reordering code or renaming methods/variables.
* As all your work is publicly visible on GitHub, sooner or later somebody will notice the plagiarism.

Penalties: NUS policy dictates that all plagiarism cases are to be reported, and to be handled centrally (i.e., at school and university level) and not by course lecturers. Hence, the penalty will be determined by the personnel handling the investigation at faculty/university level.


</div>

<div id="policy-reuse">

**Scope:** The policies on reuse apply to all project deliverables that are normally expected to be your own work (i.e., code, code comments, documentation, diagrams, images, etc.) unless stated otherwise.

**Reuse is encouraged. However, note that reuse has its own costs** (such as the learning curve, additional complexity, usage restrictions, and unknown bugs). Furthermore, you will not be given credit for work done by others. Rather, you will be given credit for _reusing_ work done by others.

* You are allowed to reuse work from your classmates or past students, subject to following conditions:
  * The work has been shared publicly by us or the authors.
  * You clearly give credit to the original author(s).
* You are allowed to reuse code from external sources, subject to following conditions:
  * You clearly give credit to the original author/source.
  * You do not violate the license under which the work has been released. Please **do not use 3rd-party images/audio** in your software unless they have been specifically released to be used freely. Just because you found it in the Internet does not mean it is free for reuse.
* ==Always get permission from us before you reuse== third-party libraries. Please post your 'request to use 3rd party library' in our [forum]({{ url_forum }}). That way, the whole class get to see what libraries are being used by others.
  * Our approval is given based on compliance with the course. Compliance with the license of the reused software is entirely your responsibility. While we don't anticipate such a case, any liability from improper reuse of a third-party library is to be borne by the person who reused it (i.e., not NUS).
  * Once a 3rd party library has been approved for one student/team, it can be used freely by others without asking for approval again.

<div id="cite-reuse-immediately">
<box type="important" seamless icon=":fas-exclamation:">

**Keep track of code reuse**{.text-danger} If you reuse/adapt code from elsewhere, cite the source in code immediately. Otherwise you will not remember the source of code reuse later. Not citing the original source can land you in trouble for plagiarism.
</box>
</div>
<div id="using-tool-generated-code">
<box type="important" seamless icon=":fas-exclamation:">

<span class="text-danger">**FAQ: Can I use code generated by AI tools** (e.g., Copilot, ChatGPT)?</span><br>
**Answer:** We don't explicitly prohibit you from using those tools, but we strongly discourage you from using them in a way that hinders your learning. For example,
* {{ good }} Use a tool such as GitHub co-pilot to increase the productivity of writing code (e.g., auto-complete the next bit of code).
* {{ good }} Write the required code yourself, and then, use the tool to generate alternative implementations, compare, and use that experience to improve your own coding skills.
* {{ good }} When troubleshooting/debugging, use a tool to help you locate the problem.
* {{ bad }} Give the problem description to the tool and get it to generate the code for you, use it directly in your submission, and claim it as your own.

Other caveats:
* Using such tools can result in your code being same as others in the class. If such code was flagged for plagiarism, "It was generated by a tool" will not be a valid excuse. Therefore, if you use (possibly with minor changes) a non-trivial code snippet generated by a tool (e.g., an entire method), it is safer to acknowledge in the code as a case of code reuse.
* Those tools sometimes can confidently give you the wrong answer. So, have a healthy level of scepticism about the accuracy of the code generated by such tools.

</box>
</div>
<box type="important" seamless icon=":fas-exclamation:">

**Automated plagiarism checks ahead!**{.text-danger} We'll be using automated plagiarism checks to detect uncredited reuses of content from other {{ course }} tP's i.e., tP's done by other teams in this batch and ==_all_ previous batches==. These checks will be done _after_ the final submissions. The cases detected will be verified and reported to the university administration for disciplinary action. As you know, NUS enforces a penalty of `F` grade for the entire course (with no option to S/U or withdraw from the course) for plagiarism offenses.
</box>
<box>

#### Giving credit for reused work

Given below are how to give credit for things you reuse from elsewhere. These requirements are specific to this course %%i.e., not applicable outside the course (outside the course, you should follow the rules specified by your employer and the license of the reused work)%%


If you **used a third party library**:
* Individual project (iP): Mention in the `README` file (under the _Acknowledgements_ section)
* Team project (tP):
  * Mention in the Developer Guide (under the _Acknowledgements_ section)
  * Mention in <trigger trigger="click" for="modal:reusePolicy-ppp">Project Portfolio Page</trigger> if the library has a significant relevance to the features you implemented.


If you **reused code snippets found on the Internet** %%e.g., from StackOverflow answers%% or<br>
**referred code in another software** or<br>
**referred project code by current/past student**:
* If you read the code to understand the approach and implemented it yourself, mention it as a comment<br>
  {{ icon_example }} Example:
  ```java{highlight-lines="1['inspired']"}
  //Solution below inspired by https://stackoverflow.com/a/16252290
  {Your implementation of the reused solution here ...}
  ```
* If you copy-pasted code from elsewhere but modified it significantly, mention it as a comment<br>
  {{ icon_example }} Example:
  ```java{highlight-lines="1['adapted']"}
  //Solution below adapted from https://stackoverflow.com/a/16252290
  {Your implementation of the reused solution here ...}
  ```
* If you copy-pasted a non-trivial code block (possibly with minor modifications %%renaming, layout changes, changes to comments, etc.%%), also mark the code block as reused code (using <trigger trigger="click" for="modal:reusePolicy-authorTags">`@@author` tags</trigger> with the <mark><code>-reused</code></mark>suffix)<br>
  Format:
  ```java{highlight-lines="1['@@author'],6['@@author']"}
  //@@author {yourGithubUsername}-reused
  //{Info about the source...}

  {Reused code (possibly with minor modifications) here ...}

  //@@author
  ```
  {{ icon_example }} Example of reusing a code snippet (with minor modifications):
  ```java{highlight-lines="2['@@author'],11['@@author']"}
  persons = getList()
  //@@author johndoe-reused
  //Reused from https://stackoverflow.com/a/34646172
  // with minor modifications
  Collections.sort(persons, new Comparator<CustomData>() {
      @Override
      public int compare(CustomData lhs, CustomData rhs) {
          return lhs.customInt > rhs.customInt ? -1 : 0;
      }
  });
  //@@author
  return persons;
  ```
<div tags="m--cs2103">

**Giving credit for reused images** (and other media assets): Ideally, the source should be credited where the asset appears. For example, if you reused an image in your GUI, you can credit the source where a screenshot of the GUI showing that image appears first in your user guide. In addition, you can also acknowledge the sources in your GitHub project's landing page (e.g., `README.md`)

**Giving credit to AB3 code**: If your team project code follows a design similar to AB3, that doesn't mean you need to credit AB3 -- this is because a brownfield project is _expected_ to follow existing code/design where possible, in the interest of consistency. This type of reuse need not be acknowledged/credited specifically.

**Giving credit to AB4 code**: If you reused any code from [AB4](https://github.com/se-edu/addressbook-level4/), cite it as you would cite reuse from any other external source.
</div>

**Giving credit for reusing from course materials** (e.g., course textbook, tutorials, instructional resources from se-education.org) is not required, although you are welcome to do so. Reason: Those materials were created by the teaching team for you to use/reuse.

**Reuse within the team** %%(e.g., reusing code written by a team member)%% need not be mentioned explicitly. However, you should factor in such reuse when you estimate effort contributed by each team member.

**Reuse of documentation** %%(e.g., reusing a UG/DG section)%% is no different from code reuse. Such reuse should be credited as well.

**Citing the use of AI-generated/assisted work** %%(e.g., using GitHub Copilot for project work)%%:

* If the use of the tool was localized into a few places %%(e.g., used it to write a few methods/classes only)%%, cite its use in comments near where you used it.
* If the use was more widespread %%(e.g., used it as an auto-complete tool during most of your coding)%%, cite the usage (i.e., which tool, who used it, the extent of use) in the following location instead (i.e., no need to cite in code comments):
  * iP: in the README file
  * tP: in the DG, under the Acknowledgements section
</box>

<modal large header="Admin {{ icon_embedding }} Project mid-v1.3 (extract) →" id="modal:reusePolicy-authorTags">
  <include src="reposenseAuthorAnnotation.md"/>
</modal>

<modal large header="Admin {{ icon_embedding }} Project → Deliverables → Project Portfolio Page" id="modal:reusePolicy-ppp">
  <include src="tp-deliverables.md#tp-deliverables-ppp"/>
</modal>

</div>

<div id="policy-feedbackOnProjectWork">

**The teaching team will not give ad-hoc feedback on project work connected to a component yet to be graded.** For example, if you were to ask your tutor for feedback on your individual or team project feature design, the tutor is not allowed to give feedback. Similarly, if you are faced with a design decision in your project, a tutor will not make that decision for you.

{{ show_faq("tutorialWhyTutorsCannotGiveProjectFeedback") }}
{{ show_faq("tutorialHowToImproveProjectWithoutTutorFeedback") }}


**You can still use the {{ link_forum }} to seek feedback on a specific aspect of your project** where a professor can answer the question in a general way that's not unfair to other teams (and other teams can benefit from the answer as well).<br>
**Alternatively, you can send your question to `{{ course_email }}`.**

</div>

<div id="policy-outsiderHelp">

In general, you are **not allowed to involve outsiders** in your project except your team members and the teaching team. However, It is OK to give your product to others for the purpose of getting voluntary user feedback. It is also OK to learn from others as long as they don't do your project work themselves.

</div>

<div id="policy-deadlineExtensions">

The ability to meet deadlines is a learning outcome of this course. Therefore, **we do not normally extend course deadlines** to accommodate those who missed the deadline, unless there are some extraordinary circumstances.

{% if cs2103 %}However, weekly project deliverables without specific deadlines are flexible. You will not be penalized for missing them if you catch up within a few days.{% endif %}
</div>

