{% set m = "cs2103" %}

{% from "_module-" + m + "/weeklyTextbookTopics.md" import weekly_textbook_topics as _weekly_textbook_topics %}
{% set weekly_textbook_topics = _weekly_textbook_topics %}
{% from "_module-" + m + "/weeklyAdminTasks.md" import weekly_admin_tasks as _weekly_admin_tasks %}
{% set weekly_admin_tasks = _weekly_admin_tasks %}
