{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_faq with context %}

{% call show_admin_page("appendixD-help") %}
<div id="main">

{% set negative_icon = '{icon="fas-thumbs-down" i-class="text-white badge rounded-pill bg-danger" i-size="12px"}' %}
{% set positive_icon = '{icon="fas-thumbs-up" i-class="text-white badge rounded-pill bg-success" i-size="12px"}' %}

%%{{ icon_info }} This guide is mostly about getting tech help, but it also applies to getting clarifications on course topics too. e.g., what is the difference between_refactoring_and_rewriting_?%%

<span class="float-end">

<pic eager src="{{baseUrl}}/admin/images/the good reasons to get home early.png" width="300"></pic><br>
</span>

**Keep in mind that instructors don't have ready solutions to all technical problems**. Unlike tutorial questions for which instructors have model solutions, given the complexity of industry tools we use (Gradle, GitHub, Git, ...) and the rapid pace they are updated, instructors don't have ready solutions to most technical problems you face in this course. The only realistic way to solve those problems at a large scale is crowdsourcing i.e., someone else who faced a similar problem might know how to fix it.


### <span class="text-danger"><span class="text-white badge rounded-pill bg-danger">{{ icon_dislike }}</span> **What not to do:**</span>

* **Send a help request to an instructor**: When faced with a technical problem or a doubt about a concept, don't fire off an email lecturer/tutor immediately, unless it is something only the lecturer/tutor is supposed to know.{{ negative_icon }}

* **Request to meet the instructor to solve the problem**: That can only work if the person is supposed to know how to solve _all_ technical problems, which is often not the case.

{{ show_faq("tutorialWhyTutorCannotGiveTechHelp") }}

### <span class="text-success"><span class="text-white badge rounded-pill bg-success">{{ icon_like }}</span> **What to do:**</span>

* **Double-check the given instructions**: Often, technical problems arise due to deviations in how you perform a step or a difference in your environment.{{ positive_icon }}

* **Get your team to meet for a weekly work-together session**. When you do course tasks together, it is easy to compare with each other and figure out what deviation is causing the problem. That is, crowd-source your team first.

* **Search**: It is very likely the answer already exists somewhere in the cyberspace. Almost every programming-related question has been answered in places like [stackoverflow](http://stackoverflow.com/). Don't give an opportunity for someone to ask you to [STFW](http://www.jibble.org/stfw/).
  Pay attention to the error message you encounter. Sometimes it also contains hints as to how to fix the problem. Even if not, a web search on the error message is a good starting point.<br>
  <pic eager src="{{baseUrl}}/admin/images/how to google it.png" width="600"/>

* **Ask AI** tools such as ChatGPT. If the question is not too specific to the course, AI tools such as ChatGPT might be able to give you a solution. It will help you hone your prompt engineering skills, and also, keep abreast with the current capabilities of such tools.

* **Ask in the [course forum]({{ url_forum }})**:
  <box type="tip" seamless>

  **Some technical problems can take a long time to resolve.** Therefore, plan ahead and schedule your work much earlier than the deadline.

  **Some problems might not get resolved at all**; while waiting for a solution, explore alternatives and workarounds.

  **==If your problem remains unsolved 24 hours after posting in the forum==**, please alert `{{ course | lower }}@comp.nus.edu.sg` so that the teaching team can look into it.
  </box>

  * **Give full details of the problem** Conversations via online forums take time. If you post everything that is relevant to your problem, your chances of getting an answer in the first try is higher. If others have to ask you more questions before they can help you, it will take longer. But this doesn't mean you dump too much information into the thread either.
    * Give a meaningful title to the post. Be as specific as you can.<br>
      {{ bad }} `testing problem`<br>
      {{ good }} `runtest.bat fails with ClassNotFound error`
    * Include full error message, screenshots, screen recordings, code snippets, stack traces, etc.<br>
      {{ icon_tip }} Use [GFMD (GitHub-Flavored Markdown)](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) syntax writing a post in the GitHub issue tracker (which we use for the forum) to format the text appropriately.
    * If the problem is code-related, share the full code if possible (e.g., push the current state of the code to a branch in your fork and give the link to the branch). That gives a chance for someone to reproduce the state of your project in their computer. Sharing just a snippet of your choosing might not be enough as the problem may not be where you think it is.
  * **Avoid showing text as screenshots**: If you want to show some text in your post %%(e.g., a code snippet, an error message)%%, it is better to copy-paste the actual text rather than a _screenshot_ of the text<br>
    Reason: so that others can easily quote/copy/modify the code in their answers.<br>
    Remember to use [_fenced code blocks_ feature](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks) so that the code is syntax-highlighted as well.<br>
    * **not preferred**{.text-danger} (it's a screenshot)<br>
      <pic eager src="images/code-screenshot.png"/>
    * **OK**
      ```{.no-line-numbers}
      @Override
      public void start(Stage primaryStage) {
          logger.info("Starting AddressBook " + MainApp.VERSION);
          ui.start(primaryStage);
      }
      ```
    * **better**{.text-success} (it has syntax highlighting too!)
      ```java{.no-line-numbers}
      @Override
      public void start(Stage primaryStage) {
          logger.info("Starting AddressBook " + MainApp.VERSION);
          ui.start(primaryStage);
      }
      ```
  * **Avoid directing the question to one person** (e.g., the prof), unless really necessary. Doing so will discourage others from answering that question.
  * **Isolate the problem.** "My code doesn't work" isn't going to help even if you post the whole code. Others don't have time to go through all of your code. Isolate the part that doesn't work and strip it down to the bare minimum that is enough to reproduce the error. Sometimes, this process actually helps you to figure out the problem yourself (have you heard about <trigger trigger="click" for="modal:appendixHelp-rubberDuckDebugging">Rubber Duck Debugging</trigger>?).

    <box>

    {{ icon_tip }} How to isolate problematic code? Delete code (one bit at a time) that is confirmed as not related to the problem. Do that until you can still reproduce the problem with the least amount of code remaining.
    </box>

  * **Generalize the problem.** "How to write tasks to a text file using Java" is too specific to what you are working on. You are more likely to find help if you post a thread called (or search for) "How to write to a file using Java".
  * **Remember to thank those who try to help, and close the issue** after the issue has been resolved.
  * **Share the solution**. If you eventually managed to solve the problem on your own, share the solution in the thread for the benefit of others, and give closure to those who tried to help you. Don't leave the thread hanging or close it with something like `Never mind. I figured it out`.
  * **Don't _hijack_ other threads**: It is OK to chime in if you have the same problem as the <tooltip content="Original Poster">OP</tooltip> but don't ask a different (even if somewhat related) question in someone else's thread. That prevents the OP from closing the thread after the original question has been resolved. Instead, post your question as a separate thread.

<modal large header="Rubber Duck Debugging" id="modal:appendixHelp-rubberDuckDebugging">

<pic eager src="{{baseUrl}}/admin/images/Rubber_duck_assisting_with_debugging.jpg" width="220"></pic><br/>

_Rubber duck debugging_ is an informal term used in software engineering to refer to a method of debugging code. The name is a reference to a story in the book _The Pragmatic Programmer_ in which a programmer would carry around a rubber duck and debug his code by forcing himself to explain it, line-by-line, to the duck.

[for more, see [wikipedia entry](https://en.wikipedia.org/wiki/Rubber_duck_debugging)]
</modal>


* **Ask the world** using programming forums such as stackoverflow.{{ positive_icon }}
  * PLEASE search for existing answers before you post your question in those public forums; You don't want to appear as a 'clueless' or 'too lazy to do your research' person in a public forum.
    <box>

    {{ icon_tip }} Know what these stand for: **RTFM**, **STFW**, **GIYF**, **LMGTFY**

    </box>

  <div id="questions-for-tutors">

* **Raise your question during a tutorial**. Some questions can be discussed with the tutor and tutorial-mates.

{{ show_faq("tutorialWhatTutorsCanAnswer", status="expanded") }}

  </div>

* **Ask the lecturer**: If your question/situation does not fit the above options, you can talk to the lecturer before/after the {{ lecture_name }}, or email the lecturer.{{ positive_icon }}


<box>

{{ icon_resource }} Resources

* [lifehacker article] [Google Tips and Tricks Every Student Should Know](http://lifehacker.com/google-tips-and-tricks-every-student-should-know-1508121671)
* [Article] [How To Ask Questions The Smart Way](http://catb.org/esr/faqs/smart-questions.html) by Eric Steven Raymond
</box>

</div>

{% endcall %}
