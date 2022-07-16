{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{% call topic_preamble("Revision Control", reuse=false) %}
Revision control is an essential aspect of software projects. Unfortunately, this module doesn't have room to go deep into it but at least you should know what it is. **The video in the content below (look for the tab marked <span class="text-primary">:fas-video:</span>) is recommended viewing.**
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Writing Developer Documents", reuse=false) %}
In this module you learned some UML diagrams that can be useful in software documentation. The module project however is too small to require serious documentation. Nevertheless, given below are **some almost common-sense guidelines that you can use when documenting a software project, or any other technical thing**.
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("revisionControl-repositories", reuse=false) %}
Two tools related to revision control to keep in mind (as they come up in conversation often):
* **[Git](https://git-scm.com/) is the most popular tool used for revision control.**
* **[GitHub](https://github.com) is one of the popular online platform that provides project management facilities centered around Git**.
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
