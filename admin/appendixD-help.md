{% macro show_main_text() %}
<div id="main">

%%{{ icon_info }} This guide is mostly about getting tech help, but it also applies to getting clarifications on module topics too. e.g. what is the difference between _refactoring_ and _rewriting_?%%

<img src="{{baseUrl}}/admin/images/how to get help.png" width="200px"><br/>


**We want to move you away from 'hand holding' and make you learn how to solve problems on your own.** This is a vital survival skill in the industry and it needs practice.

Whether it is a technical problem %%(e.g. error when using the IDE)%% or a doubt about a concept %%(e.g. what is the difference between scripted testing and exploratory testing?)&nbsp;%% **the teaching team is happy to work _with_ you when you look for a solution/answer, but we do not do it _for_ you.** We discourage unconditional direct help from tutors because we want you to learn to help yourself. Yes, we believe in ‘tough love’:stuck_out_tongue_closed_eyes:.

The question you should always ask yourself is, 'how do I solve this problem if the lecturer/tutors are not around to help me?' 

<img src="{{baseUrl}}/admin/images/the good reasons to get home early.png" width="300"/><br>

<big>{{ icon_dislike }} **What not to do:**</big> 

* When faced with a technical problem or a doubt about a concept, don'f fire off an email lecturer/tutor immediately after you encounter a problem or a doubt, unless it is something only the lecturer/tutor is supposed to know.

<big>{{ icon_like }} **What to do:**</big>

* **Check what is given**: Check if the problem/concept has been discussed in the lectures, text book, or the list of resources given to you. Yes it is easier for you to write an email to the tutor/lecturer instead, but that shouldn't be your default behavior. We know that sometimes it is difficult to find stuff in the resources we have provided. But you should try first.

* **Search**: It is very likely the answer already exists somewhere in the cyberspace. Almost every programming-related question has been answered in places like [stackoverflow](http://stackoverflow.com/). Don't give an opportunity for someone to ask you to [STFW](http://www.jibble.org/stfw/).  
  Pay attention to the error message you encounter. Sometimes it also contains hints as to how to fix the problem. Even if not, a web search on the error message is a good starting point.    
  <img src="{{baseUrl}}/admin/images/how to google it.png" width="460" height="268"/>

* **Ask peers**:   

  Ask your team members.   

  Ask classmates using the module forum or the slack channel. Even if you figured out one way to solve a problem, discussing it on a public forum might lead you to better ways of solving it, and will help other classmates who are facing similar problems too. If you are really shy to ask questions in the forum, you may use [this form](https://docs.google.com/forms/d/1vf2TjVhASq_u1_kQEEyURE5fTeBg6iKwGQDJUxYiAmg/viewform) to submit your question anonymously which we will then post in the forum.

  <panel header="Rubber Duck Debugging">

  <img src="{{baseUrl}}/admin/images/Rubber_duck_assisting_with_debugging.jpg" width="220"/><br/>

  _Rubber duck debugging_ is an informal term used in software engineering to refer to a method of debugging code. The name is a reference to a story in the book The Pragmatic Programmer in which a programmer would carry around a rubber duck and debug his code by forcing himself to explain it, line-by-line, to the duck.

  [for more, see [wikipedia entry](https://en.wikipedia.org/wiki/Rubber_duck_debugging)]  

  </panel><p/>

* **Ask the world** using programming forums such as stackoverflow.   

  Here are some tips for posting help request:
  * PLEASE search for existing answers before you post your question in those public forums; You don't want to appear as a 'clueless' or 'too lazy to do your research' person in a public forum.
  * Learn to isolate the problem. "My code doesn't work" isn't going to help even if you post the whole code online. Others don't have time to go through all of your code. Isolate the part that doesn't work and strip it down to the bare minimum that is enough reproduce the error. Sometimes, this process actually helps you to figure out the problem yourself. If not, at least it increases the chance of someone else being able to help you.  
    
    <tip-box>
    
    :bulb: How to isolate problematic code? Delete code (one bit at a time) that is confirmed as not related to the problem. Do that until you can still reproduce the problem with the least amount of code remaining.
    
    </tip-box>

  * Generalize the problem. "How to write tasks to a text file using Java" is too specific to what you are working on. You are more likely to find help if you post a thread called (or search for) "How to write to a file using Java".
  * Explain well. Conversations via online forums take time. If you post everything that is relevant to your problem, your chances of getting an answer in the first try is higher. If others have to ask you more questions before they can help you, it will take longer. But this doesn't mean you dump too much information into the thread either.  
    
    <tip-box>
    
    :bulb: Know what these stand for: **RTFM**, **STFW**, **GIYF**
    
    </tip-box>
    
<span id="questions-for-tutros">

* **Raise your question during a tutorial**. Some questions can be discussed with the tutor and tutorial-mates.
  What kind of questions are suitable to discuss with the tutor? Consider these two questions you might want to ask a tutor:
  * :white_check_mark: *This is how I understood/applied coupling. Is that correct?* - Such questions are welcome. %%**Reason**:This question shows you have put in some effort to learn the topic and seeking further clarification from the tutor.%%
  * :no_entry_sign: *What is coupling?* - Such questions are discouraged. %%**Reason**: This question implies you haven’t done what you could to learn the topic in concern.%%
  
</span>

* **Talk to the lecturer** before or after the lecture. The lecturer will be at the lecture venue from 30 minutes before the start of the lecture.

* **Request our help**: Failing all above, you can always request for help by emailing the lecturer.

Resources

* [lifehacker article]  [Google Tips and Tricks Every Student Should Know](http://lifehacker.com/google-tips-and-tricks-every-student-should-know-1508121671)
* [Article] [How To Ask Questions The Smart Way](http://catb.org/esr/faqs/smart-questions.html) by Eric Steven Raymond

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("appendixD-help", show_main_text) }}