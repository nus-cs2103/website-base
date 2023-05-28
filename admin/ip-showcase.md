<frontmatter>
title: "iP Showcase"
</frontmatter>

# iP Showcase

{% from "_course-" + course + "/studentData-fragment.md" import students, tutorials with context %}

{% set current_team = "" %}
{% for tutorial in tutorials %}
<panel header="## {{ tutorial }}" {{ "expanded" if tic4001 or tic4002 else "" }} no-close>
{% for student in students %}
{% set student_team = student[1] %}
{% set student_tutorial = 'TIC4001-F18' if tic4001 else student_team.slice(0, -2) %}
{% if student_tutorial == tutorial %}
{% if current_team != student_team %}
  {% set current_team = student_team %}
### <span class="badge bg-secondary">{{ student_team }}</span>
{% endif %}
{% set student_name = student[0] %}
{% set username = student[2] %}
{% set duke_website = "https://" + username + ".github.io/" + ip_repo_name %}
{% set duke_repo = "https://github.com/" + username + "/" + ip_repo_name %}
#### {{ student_name }} ([<span class="text-monospace">@{{ username }}</span>](https://github.com/{{ username }})) <small>[:fas-home:]({{ duke_website }}) [:fab-github:]({{ duke_repo }}) [:fas-download:]({{ duke_repo }}/releases) [:fas-code:](https://nus-{{ course | lower }}-{{ semester | lower }}.github.io/ip-dashboard/?search=&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=false&tabOpen=true&tabType=authorship&tabAuthor={{ username }}&tabRepo={{ username }}%2Fip%5Bmaster%5D&authorshipIsMergeGroup=false&authorshipFileTypes=java~md~fxml~gradle~txt&authorshipIsBinaryFileTypeChecked=false) [:fas-code-branch:](https://github.com/nus-{{ course | lower }}-{{ semester }}/{{ ip_repo_name }}/pulls/{{ username }}) [:fas-comment:](https://github.com/{{ username }}/{{ ip_repo_name }}/issues/new) </small>
<pic tags="m--cs2103 m--tic4002" src="{{ duke_website }}/Ui.png" height="750" style="max-width: 100%"  onerror="this.src='images/placeholder-small.png';"></pic><p/>

<hr>
{% endif %}
{% endfor %}

</panel>
{% endfor %}
