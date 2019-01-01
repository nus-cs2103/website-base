<div id="additional">

%%Given below are some module _admin info_ to read around this time:%%

</div>

{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read with context %}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week1, is_flat=false ) }}

