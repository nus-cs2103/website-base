{% from "schedule/index.md" import show_week_topics_page with context %}
{% from "common/topics.njk" import panopto, topic_preamble with context %}

{{ show_week_topics_page(8) }}

<div id="notices" class="d-none">
<div tags="m--tic2002">

<box type="info">

Last week, you learned intermediate-level class diagram notation. But the quiz only focused on interpreting such diagrams. **This week, we cover the aspect of _drawing intermediate-level class diagrams to match code_**. Here are what you can do:<br>
1\. Do _Part 1_ of this week's quiz (which covers the same area).<br>
2\. Watch the worked examples in the following videos to learn the process of drawing intermediate-level class diagrams to match code.

{{ panopto("052aa055-c89f-4dbf-af24-ac4000f175e0", desc="Drawing class/object diagrams (intermediate) - `Action`, `Task`, `History`") }}
{{ panopto("f4f7e1f2-60a4-4d18-b70a-ac4000f17608", desc="Drawing class/object diagrams (intermediate) - `Person`, `Inbox`, `Message`") }}
{{ panopto("e05845ed-8c70-47d9-a4d0-ac6800d58224", desc="Drawing class/object diagrams (intermediate) - `Person`, `Project`, `Task`") }}

</box>
</div>
</div>
