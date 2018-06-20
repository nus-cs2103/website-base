<frontmatter>
title: "Full Schedule of Module Activities"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<include src="../common/header.md" />

<div class="website-content">

# Full Schedule of Module Activities

<panel header="### <small>**{{glyphicon_calendar}} Tutorial Timetable**</small>" no-close>
  <include src="overview/tutorialSchedule.md"/>
</panel>
<include src="overview/index.md" name=":exclamation: **Info relevant to all weeks**" dynamic />
<p/>


{% set past_weeks = [
    {num: "1", day:"Jan 15"}
] %}

{% for week in past_weeks %}
<panel type="seamless" src="week{{ week.num }}/index.md" dynamic no-close>
<span slot="header" class="panel-title week-past"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endfor %}

<panel type="seamless" expanded no-close>
<span slot="header" class="panel-title week"> Week 2 [Jan 22]</span>
  <include src="week2/index.md"/>
</panel>

{% set future_weeks = [
    {num: "3", day:"Jan 29"}, 
    {num:"4", day:"Jan 29"},
    {num:"5", day: "Feb 12" },
    {num:"6", day: "Feb 19" },
    {num:"7", day: "Mar 5" },
    {num:"8", day: "Mar 12" },
    {num:"9", day: "Mar 19" },
    {num:"10", day: "Mar 26" },
    {num:"11", day: "Apr 2" },
    {num:"12", day: "Apr 9" },
    {num:"13", day: "Apr 16" }
] %}

{% for week in future_weeks %}
<panel type="seamless" src="week{{ week.num }}/index.md" dynamic no-close>
<span slot="header" class="panel-title week-future"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endfor %}




</div>