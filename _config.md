{% set m = "cs2103" %}

{% from "_module-" + m + "/weeklyTextbookTopics.md" import weekly_textbook_topics as _weekly_textbook_topics %}
{% set weekly_textbook_topics = _weekly_textbook_topics %}
{% from "_module-" + m + "/weeklyAdminTasks.md" import weekly_admin_tasks as _weekly_admin_tasks %}
{% set weekly_admin_tasks = _weekly_admin_tasks %}
{% from "_module-" + m + "/weeklyAdminTopics.md" import weekly_admin_topics as _weekly_admin_topics %}
{% set weekly_admin_topics = _weekly_admin_topics %}
{% from "_module-" + m + "/weeklyIpTasks.md" import weekly_ip_tasks as _weekly_ip_tasks %}
{% set weekly_ip_tasks = _weekly_ip_tasks %}
{% from "_module-" + m + "/weeklyTpTasks.md" import weekly_tp_tasks as _weekly_tp_tasks %}
{% set weekly_tp_tasks = _weekly_tp_tasks %}
