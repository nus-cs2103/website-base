{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Install Git {{ timing_badge("before the lecture") }}
1. Submit weekly exercises
1. Submit post-lecture quiz
{% endcall %}

{{ thumb(1) }} Get started with Git {{ timing_badge("before/during the lecture") }}

* See weekly topics (Git Learning Trail - Tour 1) for more info.

{{ thumb(2) }} Submit weekly exercises

* As usual, submit weekly programming exercise.

{{ thumb(3) }} Submit post-lecture quiz

* Submit the post-lecture quiz on Canvas.
