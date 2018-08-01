{% macro show_main_text() %}
<div id="main">

This module is organized primarily around a list of Learning Outcomes.

Each week has a suggested list of LOs. They are categorized using a star-rating system<span class="flat"> ([link](#starRatingSystem))</span>.

<panel  src="moduleExpectations.md#starRatingSystem" header="Admin {{ icon_embedding }} Module Expectations → Star Rating System" class="embedding" minimized />

</div>

{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("learningOutcomes", show_main_text) }}