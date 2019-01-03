{% macro show_main_text() %}
<div id="main">

This module is organized primarily around a list of Learning Outcomes.

Each week has a suggested list of topics. They are categorized using a star-rating system.

{{ embed_topic("moduleExpectations.md#starRatingSystem", "Admin " + icon_embedding + " Module Expectations → Star Rating System", "learningOutcomes-starRatingSystem") }}

</div>

{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("learningOutcomes", show_main_text) }}