{% from "common/macros.njk" import  show_stars, show_faq2 with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("appendixC-faq") %}
<div id="main">

## FAQs on: General

{{ show_faq2("whereIsEverything", "y") }}
{{ show_faq2("tVsNonT", "y") if cs2103 }}
{{ show_faq2("aPlus", "y") }}
{{ show_faq2("beanCounting", "y") }}
{{ show_faq2("separateWebsite", "y") }}
{{ show_faq2("slideFormat", "y")  if cs2103 }}
{{ show_faq2("narrowProjectScope", "y") }}
{{ show_faq2("favoriteTool", "y") }}
{{ show_faq2("manySubmissions", "y") }}
{{ show_faq2("cs2101Difference", "y") if cs2103  }}

## FAQs on: Participation

{{ show_faq2("whenCanWeSeeQuizAnswers", "y") }}

</div>

{% endcall %}
