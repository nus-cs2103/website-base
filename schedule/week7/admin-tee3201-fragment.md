{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import policies, show_admin_summary, topics with context %}

{% call show_admin_summary() %}
1. Submit weekly quiz
1. Submit weekly exercises
1. Submit weekly project increment `Level 8. Support Deadlines`
{% endcall %}


#### {{ thumb(1) }} Submit weekly quiz

* As usual


#### {{ thumb(2) }} Submit weekly exercises

* As usual


#### {{ thumb(3) }} Submit weekly project increments

<span id="week7-project">

<include src="montyFragment.md" boilerplate var-displacement="../.." var-header="**Level 8. Support Deadlines**" var-fragment="monty-fragment.md#monty8" />
</span>
