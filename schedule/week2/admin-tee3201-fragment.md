{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import policies, show_admin_summary, topics with context %}

{% call show_admin_summary() %}
1. Submit weekly exercises
1. Submit weekly project increment `Monty Level 2. Recognize Known Commands`
{% endcall %}

#### {{ thumb(0) }} Finish previous week's tasks if you haven't done so already

#### {{ thumb(1) }} Submit weekly exercises

* As usual, submit on coursemology

#### {{ thumb(2) }} Submit quiz

* After learning the [SE topics](topics.md) allocated for this week, submit the quiz on Canvas.


#### {{ thumb(3) }} Submit weekly project increments

<span id="week2-project">

* Add the following increment to your project. As before (and also in future weeks), copy-paste-submit the updated code via the weekly exercise named `WeekN - Project Submission` where `N` is the week number %%e.g., submit this week's project code via the Coursemology exercise named `Week2 - Project Submission`%%.

<include src="montyFragment.md" boilerplate var-displacement="../.." var-header="**Level 2. Recognize Known Commands**" var-fragment="monty-fragment.md#monty2" />
</span>
