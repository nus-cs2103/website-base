{% from "common/macros.njk" import get_week_start_date with context %}
{% from "common/admin.njk" import get_admin_menu_items with context %}

{% macro ip_dashboard_links() %}
<li><a href="{{ url_ip_progress_dashboard }}" target="_blank" class="dropdown-item text-success"><md>:fas-tasks: iP Progress Dashboard</md></a></li>
<li><a href="{{ url_course_gihub_io }}/dashboards/contents/ip-comments.html" target="_blank" class="dropdown-item"><md>:octicon-comment: iP Comments dashboard</md></a></li>
<li><a href="{{ url_ip_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: iP Code Dashboard</md></a></li>
{% endmacro %}

{% macro tp_dashboard_links() %}
<li><a href="{{url_tp_progress_dashboard}}" target="_blank" class="dropdown-item text-success"><md>:fas-tasks: tP Progress Dashboard</md></a></li>
<li><a href="{{ url_course_gihub_io }}/dashboards/contents/tp-comments.html" target="_blank" class="dropdown-item"><md>:octicon-comment: tP Comments Dashboard</md></a></li>
<li><a href="{{ url_tp_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: tP Code Dashboard</md></a></li>{% if show_feature_freeze_dashboards %}
<li><a href="{{ url_tp_dashboard_fc_only }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: tP Code Dashboard (Functional Code Only)</md></a></li>
<li><a href="{{ url_tp_feature_freeze_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: tP Code Dashboard (Feature Freeze Period Only)</md></a></li>{% endif %}
{% endmacro %}

{% if current_week == "-1" %}
<div class="w-100 p-1 bg-warning text-center d-print-none"><md>**This is a draft version of the website! The final version will be available near the start of the semester.**</md></div>
{% endif %}{% if current_week in ["-1", "0", "1"] %}
<div class="w-100 p-1 bg-success text-white text-center d-print-none"><md>{% if cs2113 %}All the course activities are scheduled to be _in-person_ activities this semester.{% else %}This course will be delivered in _blended learning_ mode (i.e., a mix of online and F2F activities) this semester.{% endif %}</md></div>
{% elseif current_week == "15" %}
<div class="w-100 p-1 bg-warning text-center"><md>**This site is from a past semester! The current version will be [here](http://www.comp.nus.edu.sg/~{{ course | lower }}) when the new semester starts.**</md></div>
</div>
{% endif %}
<header sticky>
<navbar placement="top" type="dark">
<a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand"><span class="badge rounded-pill bg-{{ course_color }}">{{ course_pair }} <small>{{ period }}</small></span></a>
  <dropdown header="**Schedule**" class="nav-link">
  <li><a href="{{baseUrl}}/schedule/timeline.html" class="dropdown-item"><md>**Full Timeline**</md></a></li>
{% for week in range(1, 14) %}
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/index.html" class="dropdown-item"> <md>**Week {{ week }}** [{{ get_week_start_date(week | int, format_normal) }}] {% if current_week == week %} :fas-arrow-circle-left:{% endif %}</md></a></li>
{% if current_week == week %}
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/admin.html" class="dropdown-item">&nbsp;&nbsp;├ Week {{ week }}: {{ icon_tab_admin_info }} <md> **Admin**</md></a></li>
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/topics.html" class="dropdown-item">&nbsp;&nbsp;├ Week {{ week }}: {{ icon_tab_topics }} <md> **Topics**</md></a></li>
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/project.html" class="dropdown-item">&nbsp;&nbsp;├ Week {{ week }}: {{ icon_project }} <md> **Project**</md></a></li>
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/tutorial.html" class="dropdown-item">&nbsp;&nbsp;└ Week {{ week }}: {{ icon_tab_tutorial }} <md> **Tutorial**</md></a></li>
{% endif %}
{% endfor %}
  </dropdown>
<<<<<<< HEAD
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="nav-link"><md>**Textbook**</md></a></li>
{% if tic2002 %}
  <li><a href="{{baseUrl}}/admin/index.html" class="nav-link"><md>**Admin Info**</md></a></li>
{% else %}
  <dropdown header="**Admin Info**" class="nav-link">
{{ get_admin_menu_items() }}
  </dropdown>
{% endif %}
  <dropdown tags="m--cs2103 m--cs2113" header="**Dashboards**" class="nav-link">
  <li><a href="{{ url_participation_dashboard }}" class="dropdown-item text-success" target="_blank"><md>:fas-trophy: **Participation** dashboard</md></a></li>
  <li><a href="{{ url_course_gihub_io }}/dashboards/contents/forum-activities.html" class="dropdown-item" target="_blank"><md>:octicon-comment: **Forum** Dashboard</md></a></li>
  <hr>
  <md>**&nbsp;iP dashboards:**</md>
  {{ ip_dashboard_links() }}
  <hr>
  <md>**&nbsp;tP dashboards:**</md>
  {{ tp_dashboard_links() }}
  <dropdown header="**Textbook**" class="nav-link">
    <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="dropdown-item">SE Textbook</a></li>
    <li><a href="{{baseUrl}}/programming/index.html" class="dropdown-item">Programming Textbook</a></li>
  </dropdown>
  <li><a href="{{baseUrl}}/admin/index.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <li tags="m--cs2103 m--cs2113"><a href="{{ url_dashboards }}" target="_blank" class="nav-link" highlight-on="none"><md>**Dashboards**</md></a></li>
  <dropdown tags="m--cs2103 m--cs2113" header="**Project Links**" class="nav-link">
    <md>**&nbsp;Individual Project (iP):**</md>
    <li><a href="{{baseUrl}}/admin/ip-overview.html" class="dropdown-item"><md>{{ icon_project }} Individual Project Info</md></a></li>
    <li><a href="{{url_course_org}}/{{ ip_repo_name }}" target="_blank" class="dropdown-item"><md>{{ icon_repo }} iP Upstream Repo</md></a></li>{% if (current_week | int) > 1 %}
    <li tags="m--cs2103"><a href="{{baseUrl}}/admin/ip-showcase.html" class="dropdown-item"><md>:glyphicon-list-alt: iP Showcase</md></a></li>{% endif %}
  {{ ip_dashboard_links() }}
  <hr>
    <md>**&nbsp;Team Project (tP):**</md>
    <li><a href="{{baseUrl}}/admin/tp-overview.html" class="dropdown-item"><md>{{ icon_project }} Team Project Info</md></a></li>
    <li tags="m--cs2103 m--cs2113"><a href="{{url_course_org}}/{{ tp_repo_name }}" target="_blank" class="dropdown-item"><md>{{ icon_repo }} tP Upstream Repo {% if not cs2113 %}(AB3){% endif %}</md></a></li>
    <li><a href="{{ url_team_list }}" class="dropdown-item"><md>:glyphicon-list-alt: Team List</md></a></li>
  {{ tp_dashboard_links() }}
  <li tags="m--cs2113"><a href="https://github.com/se-edu/addressbook-level3" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Reference AB3</md></a></li>
  </dropdown>
  <li tags="m--cs2103 m--cs2113"><a href="{{url_forum}}" class="nav-link"><md>**Forum**</md></a></li>
  <dropdown header="**{{ "Other " if not tic2002 or tee3201 else ""}}Links**" class="nav-link">
    <li tags="m--cs2103 m--cs2113"><a href="{{url_bugs}}" target="_blank" class="dropdown-item"><md>:fas-bug: Report Bugs</md></a></li>
    <li><a href="{{url_forum}}" target="_blank" class="dropdown-item"><md>:fas-comment: Forum</md></a></li>
    <li><a href="{{ baseUrl }}/admin/{{ "index.html#instructors" if tic2002 or tee3201 else "instructors.html" }}" class="dropdown-item"><md>:fas-user-tie: Instructors</md></a></li>
    <li><a href="{{url_announcements}}" target="_blank" class="dropdown-item"><md>:glyphicon-bullhorn: Announcements</md></a></li>
    <li><a href="{{url_files}}" target="_blank" class="dropdown-item"><md>:fas-file-upload: Files (handouts, submissions etc.)</md></a></li>
    <li tags="m--cs2113 m--cs2103"><a href="{{baseUrl}}/admin/tutorials.html" class="dropdown-item"><md>:glyphicon-calendar: Tutorial Schedule</md></a></li>
    <li tags="m--tic2002 m--tee3201"><a href="{{baseUrl}}/admin/index.html#project" class="dropdown-item"><md>{{ icon_project }} Project Info</md></a></li>
    <li tags="m--cs2113 m--tic2002 m--tee3201"><a href="{{url_coursemology_classroom}}" target="_blank" class="dropdown-item"><md>{{ icon_exercise }} Coursemology link</md></a></li>
    {% if not cs2113 %}<li><a href="{{url_ms_teams_class}}" target="_blank" class="dropdown-item"><md>:fas-users-cog: MS Teams link</md></a></li>
    {% endif %}{% if cs2103 %}<li><a href="{{ baseUrl }}/se-book-adapted/git-trail/index.html" class="dropdown-item"><md>:fas-route: Git Learning Trail</md></a></li>
    {% endif %}<li tags="m--tic2002"><a href="{{ url_participation_dashboard }}" class="dropdown-item text-success" target="_blank"><md>:fas-trophy: **Participation** dashboard</md></a></li>
    <li tags="m--cs2103 m--cs2113 m--tic2002"><a href="{{url_java_coding_standard}}" target="_blank" class="dropdown-item"><md>:fas-code: Java Coding Standard</md></a></li>
    <li tags="m--cs2103 m--cs2113"><a href="{{url_git_conventions}}" target="_blank" class="dropdown-item"><md>:fab-git-square: Git Conventions</md></a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      {% if algolia == "no" %}<searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>{% else %}<searchbar placeholder="Search" algolia menu-align-right></searchbar>{% endif %}
    </form>
  </li>
</navbar>
</header>
