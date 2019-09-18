{% from "admin/ip-showcase.md" import tutorials, students with context %}

<frontmatter>
title: "Project List"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 2
</frontmatter>

# tP Showcase

{% macro get_team_start(team_id, team_org, team_repo, team_website) %}
<div class="container">
<div class="row">
<div class="col border">

### {{ team_id }} <small>[:fab-github:]({{ team_repo }}) [:fas-home:]({{ team_website }}) [:fas-code-branch:](https://github.com/nus-{{ module | lower }}-{{ semester }}/addressbook-level3/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aopen+{{ team_id }}) [:far-comment:]({{ team_repo }}/issues/new)</small> [<img src="https://travis-ci.org/{{ team_org }}/main.svg?branch=master" alt="Build Status">](https://travis-ci.org/{{ team_org }}/main)
<img src="{{ team_website }}/images/Ui.png" width="750" onerror="this.src='images/placeholder-large.png';" /><p/>
</div>
</div>
<div class="row">
{% endmacro %}


{% macro get_team_end(team_id) %}
</div>
</div>
<p/>
{% endmacro %}


{% macro get_student_content(name, username, team_repo, team_website) %}
<div class="col text-center border">

**{{ name }}**<br>
<img src="{{ team_website }}/images/{{ username | lower }}.png" width="120"  onerror="this.src='images/placeholder-small.png';"/><br>[:fas-file-powerpoint:]({{ team_website }}/team/{{ username | lower }}.html) [:fas-code:](https://nus-{{ module }}-{{ current_semester }}.github.io/tp-dashboard/#=undefined&search={{ username | lower }}) [:fas-code-branch:]({{ team_repo }}/pulls?q=is%3Apr+author%3A{{ username }})
</div>
{% endmacro %}


{% set current_semester = "AY1920S1" %}
{% set panel_contents = "" %}
{% set team_contents = "" %}
{% set current_team = "" %}

{% for tutorial in tutorials  %}
  {% for student in students  %}

    {% set student_team = student[1] %}
    {% set student_tutorial = student_team.slice(0, -2) %}
    {% set student_name = student[0] %}
    {% set student_username = student[2] %}
    {% set team_org = current_semester + '-' + student_team %}
    {% set team_website = "https://" + team_org + ".github.io/main" %}
    {% set team_repo = "https://github.com/" + team_org + "/main" %}

    {% if student_tutorial == tutorial %}
      {% if current_team != student_team %}
        {% if current_team != "" %}
        {% set team_end %} {{ get_team_end() }} {% endset %}
          {% set panel_contents = panel_contents + team_contents + team_end %}
        {% endif %}
        {% set current_team = student_team %}
        {% set team_contents %} {{ get_team_start(student_team, team_org, team_repo, team_website) }} {% endset %}
      {% endif %}
        {% set student_contents %}{{ get_student_content(student_name, student_username, team_repo, team_website) }}{% endset %}
        {% set team_contents = team_contents + student_contents %}
    {% endif %}

  {% endfor %}
  {% set team_end %} {{ get_team_end() }} {% endset %}
  {% set panel_contents = panel_contents + team_contents + team_end %}

<panel type="seamless" header="## {{ tutorial }}" no-close expanded>
{{ panel_contents }}
</panel>

  {% set panel_contents = "" %}
  {% set team_contents = "" %}
  {% set current_team = "" %}
{% endfor %}
