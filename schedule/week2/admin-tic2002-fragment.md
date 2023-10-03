{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Install Sourcetree {{ timing_badge("before the lecture") }}
1. Submit weekly exercises
1. Submit post-lecture quiz
{% endcall %}

{{ thumb(1) }} Install Sourcetree {{ timing_badge("before the lecture", "secondary") }}

* See the panel below:

{{ embed_topic("../../admin/index-tic2002-fragment.md#git-info", "Admin " + icon_embedding + " Tools → Git, Sourcetree", "week2Admin-git", "1") }}

{{ thumb(2) }} Submit weekly exercises

* As usual, submit weekly programming exercise.

{{ thumb(3) }} Submit post-lecture quiz

* Submit the post-lecture quiz on Canvas.
