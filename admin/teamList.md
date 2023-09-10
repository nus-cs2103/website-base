{% from "_course-" + course + "/studentData-fragment.md" import students, tutorials, teams, products, users, values with context %}

<frontmatter>
title: "tP Teams List"
pageNav: 2
</frontmatter>

# tP Teams


{% if not teams | length %}

<p>
This page will be populated later in the semester ...

{% endif %}


{% macro get_team_start(team_id, team_org, team_repo, team_website) %}
<div class="container">
<div class="row">
<div class="col border">

### {{ team_id }} <small>[:fab-github:]({{ team_repo }}) [:fas-home:]({{ team_website }}) [:fas-code-branch:](https://github.com/nus-{{ course | lower }}-{{ semester }}/{{ tp_repo_name }}/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aopen+{{ team_id }}) [:far-comment:]({{ team_repo }}/issues/new)</small> {% if (current_week | int) > 6 %}[<pic eager src="{{ team_repo }}/workflows/Java%20CI/badge.svg"></pic>]({{ team_repo }}/actions){% endif %} {{ "[**" + products[team_id] + "]**" if team_id in products else ""}}

<span tags="m--cs2103 m--tic4002">

<img src="{{ team_website }}/images/Ui.png" width="750" onerror="this.src='images/placeholder-large.png';"></img><p/>
</span>
<span tags="m--cs2103 m--tic4001 m--tic4002">
**Target user:**
<div class="indented">
<blockquote>
{{ users[team_id] if team_id in users else "[not available yet]" }}
</blockquote>
</div>

**Value proposition:**
<div class="indented">
<blockquote>
{{ values[team_id] if team_id in values else "[not available yet]" }}
</blockquote>
</div>

**Project notes** (internal): {% if teams[team_id] != '' %}see [here]({{ teams[team_id] }}){% else %}N/A{% endif %}
</span>
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
<sup>[`{{ username }}`](https://github.com/{{ username }})</sup><br>
{% if not cs2113 %}<img style="border-radius: 8px;" src="{{ team_website }}/images/{{ username | lower }}.png" width="120"  onerror="this.src='images/placeholder-small.png';"></img><br>{% endif %}[:fas-file-powerpoint:]({{ team_website }}/team/{{ username | lower }}.html) [:fas-code:](https://nus-{{ course }}-{{ semester }}.github.io/tp-dashboard/?search={{ username | lower }}&breakdown=true) [:fas-code-branch:]({{ team_repo }}/pulls?q=is%3Apr+author%3A{{ username }})
</div>
{% endmacro %}

{% set panel_contents = "" %}
{% set team_contents = "" %}
{% set current_team = "" %}

{% if teams | length %}
{% for tutorial in tutorials %}
  {% for student in students %}

    {% set student_team = student[1] %}
    {% set student_tutorial = 'TIC4001-F18' if tic4001 else student_team.slice(0, -2) %}
    {% set student_name = student[0] %}
    {% set student_username = student[2] %}
    {% set team_org = semester + '-' + student_team %}
    {% set team_website = "https://" + team_org + ".github.io/" + tp_repo_name %}
    {% set team_repo = "https://github.com/" + team_org + "/" + tp_repo_name %}

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

<panel type="seamless" header="## {{ tutorial }}" {{ "expanded" if tic4001 or tic4002 else ""}} no-close>
{{ panel_contents }}
</panel>

  {% set panel_contents = "" %}
  {% set team_contents = "" %}
  {% set current_team = "" %}
{% endfor %}
{% endif %}
