<frontmatter>
title: "Timeline"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 3
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics with context %}


# Summary of the Module Timeline

<box type="warning" dismissible>
<span id="warnings">

* Please try to **follow instructions closely**. If you deviate, our grading scripts will not be able to detect your work.
* The deadline to complete weekly project work is the **midnight before your tutorial day** %%e.g., if your tutorial is on Thursday, you should finish your project work by Wednesday 23.59%%. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
* You may have to **go through the weekly topics before attempting weekly project tasks** as the knowledge from those topics may be needed to complete the iP tasks.

</span>
</box>

{% for week_num in range(1, 14) %}

### <span class="badge badge-pill badge-dark"><small>**Week {{ week_num }}**</small></span>

<include src="week{{ week_num }}/notices-{{ module }}.md#summary" optional />
{% endfor %}



