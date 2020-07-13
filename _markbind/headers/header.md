{% from "common/macros.njk" import get_week_start_date with context %}

<header fixed>
{% if current_week == "-1" %}
<div class="w-100 p-1 bg-warning text-center"><md>**This site is not ready yet! The updated version will be available soon.**</md></div >
{% elseif current_week in ["0", "1"] %}
<div class="w-100 p-1 bg-success text-center text-white"><md>This module will be **fully online** this semester. There is no need for on-campus presence.</md></div>
{% elseif current_week == "15" %}
<div class="w-100 p-1 bg-warning text-center"><md>**This site is from a past semester! The current version will be [here](http://www.comp.nus.edu.sg/~{{ module | lower }}) when the new semester starts.**</md></div>
{% endif %}
<navbar placement="top" type="dark">
<a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand"><span class="badge badge-pill badge-{{ module_color }}">{{ module_pair }} <small>{{ period }}</small></span></a>
  <dropdown header="**Schedule**" class="nav-link">
  <li><a href="{{baseUrl}}/schedule/timeline.html" class="dropdown-item"><md>**Full Timeline**</md></a></li>
{% for week in range(1, 14) %}
<li><a href="{{ baseUrl }}/schedule/week{{ week }}/index.html" class="dropdown-item"> <md>**Week {{ week }}** [{{ get_week_start_date(week | int, format_normal) }}] {% if current_week == week.num %} :fas-arrow-circle-left:{% endif %}</md></a></li>
{% endfor %}
  </dropdown>
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="nav-link"><md>**Textbook**</md></a></li>
  <li><a href="{{baseUrl}}/admin/index.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown header="**Links**" class="nav-link">
    <li tags="m--cs2103 m--cs2113 m--tic4001"><a href="{{url_bugs}}" target="_blank" class="dropdown-item"><md>:fas-bug: Report Bugs</md></a></li>
    <li><a href="{{url_forum}}" target="_blank" class="dropdown-item"><md>:fas-comment: Forum</md></a></li>
    <li tags="m--cs2113 m--cs2103 m--tic4001"><a href="{{url_gitter}}" target="_blank" class="dropdown-item"><md>:fab-gitter: Gitter (Chat)</md></a></li>
    <li><a href="{{ baseUrl }}/admin/{{ "index.html#instructors" if tic2002 or te3201 else "instructors.html" }}" class="dropdown-item"><md>:fas-user-tie: Instructors</md></a></li>
    <li><a href="{{url_announcements}}" target="_blank" class="dropdown-item"><md>:glyphicon-bullhorn: Announcements</md></a></li>
    <li><a href="{{url_files}}" target="_blank" class="dropdown-item"><md>:fas-file-upload: Files</md></a></li>
    <li tags="m--cs2113 m--cs2103"><a href="{{baseUrl}}/admin/tutorials.html" class="dropdown-item"><md>:glyphicon-calendar: Tutorial Schedule</md></a></li>
    <li tags="m--cs2113 m--tic2002 m--te3201"><a href="{{url_repl_classroom}}" target="_blank" class="dropdown-item"><md>{{ icon_exercise }} `repl.it` link</md></a></li>
    <li tags="m--cs2103 m--cs2113 m--tic2002 m--tic4001"><a href="{{url_java_coding_standard}}" target="_blank" class="dropdown-item"><md>:fas-code: Java Coding Standard</md></a></li>
    <li tags="m--cs2103 m--cs2113 m--tic4001"><a href="{{url_git_conventions}}" target="_blank" class="dropdown-item"><md>:fab-git-square: Git Conventions</md></a></li>
    <li tags="m--cs2103 m--cs2113"><a href="{{ url_forum_activities_dashboard }}" class="dropdown-item"><md>:fas-trophy: Forum Activities Dashboard</md></a></li>
    <li><a href="{{url_participation_dashboard}}" target="_blank" class="dropdown-item text-success"><md>:fas-trophy: Participation Dashboard</md></a></li>
    <hr>
    <md>**&nbsp;Individual Project (iP):**</md>
    <li><a href="{{baseUrl}}/admin/ip-overview.html" class="dropdown-item"><md>{{ icon_project }} Individual Project Info</md></a></li>
    <li><a href="{{ baseUrl }}/admin/ip-showcase.html" class="dropdown-item"><md>:glyphicon-list-alt: iP List</md></a></li>
    <li><a href="{{url_module_org}}/{{ ip_repo_name }}" target="_blank" class="dropdown-item"><md>{{ icon_repo }} iP Upstream Repo</md></a></li>
    <li><a href="{{ url_ip_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: iP Code Dashboard</md></a></li>
    <li><a href="{{ url_ip_progress_dashboard }}" target="_blank" class="dropdown-item text-success"><md>:fas-trophy: iP Progress Dashboard</md></a></li>
    <hr>
    <md>**&nbsp;Team Project (tP):**</md>
    <li><a href="{{baseUrl}}/admin/tp-expectations.html" class="dropdown-item"><md>{{ icon_project }} Team Project Info</md></a></li>
    <li tags="m--cs2103"><a href="{{url_module_org}}/addressbook-level3" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level3</md></a></li>
    <li><a href="{{ url_team_list }}" class="dropdown-item"><md>:glyphicon-list-alt: Team List</md></a></li>
    <li><a href="{{ url_tp_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: tP Code Dashboard</md></a></li>
    <li><a href="{{url_tp_progress_dashboard}}" target="_blank" class="dropdown-item text-success"><md>:fas-trophy: tP Progress Dashboard</md></a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      {% if current_week == "15" or alogolia == "no" %}<searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>{% else %}<searchbar placeholder="Search" algolia menu-align-right></searchbar>{% endif %}
    </form>
  </li>
</navbar>
</header>
