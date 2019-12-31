{% from "schedule/index.md" import weeks, current_week with context %}
<header>
{% if current_week == "-1" %}
<div class="w-100 p-1 bg-warning text-center"><md>**This site is not ready yet! The updated version will be available soon.**</md></div >
{% elif current_week == "14" %}
<div class="w-100 p-1 bg-warning text-center"><md>**This site is from a past semester! The current version is [here](http://www.comp.nus.edu.sg/~{{ module | lower }}).**</md></div>
{% endif %}
<navbar placement="top" type="dark">
<a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand"><span class="badge badge-pill badge-{{ module_color }}">{{ module_pair }} <small>{{ period }}</small></span></a>
  <dropdown text="Schedule" class="nav-link">
  <li><a href="{{baseUrl}}/schedule/timeline.html" class="dropdown-item"><md>**Full Timeline**</md></a></li>
{% for week in weeks %}
<li><a href="{{ baseUrl }}/schedule/week{{ week.num }}/index.html" class="dropdown-item"> <md>**Week {{ week.num }}** [{{ week.day }}] {% if current_week == week.num %} :fas-arrow-circle-left:{% endif %}</md></a></li>
{% endfor %}
  </dropdown>
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="nav-link"><md>**Textbook**</md></a></li>
  <li><a href="{{baseUrl}}/admin/index.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown text="Links" class="nav-link">
    <li><a href="{{bugs_link}}" target="_blank" class="dropdown-item"><md>:fas-bug: Report Bugs</md></a></li>
    <li><a href="{{forum_link}}" target="_blank" class="dropdown-item"><md>:fas-comment: Forum</md></a></li>
    <li><a href="{{ baseUrl }}/admin/instructors.html" class="dropdown-item"><md>:fas-user-tie: Instructors</md></a></li>
    <li><a href="{{announcements_link}}" target="_blank" class="dropdown-item"><md>:glyphicon-bullhorn: Announcements</md></a></li>
    <li><a href="{{files_link}}" target="_blank" class="dropdown-item"><md>:fas-file-upload: File Submissions</md></a></li>
    <li><a href="{{baseUrl}}/admin/tutorials.html" target="_blank" class="dropdown-item"><md>:glyphicon-calendar: Tutorial Schedule</md></a></li>
    <li><a href="{{java_coding_standard}}" target="_blank" class="dropdown-item"><md>:fas-code: Java Coding Standard</md></a></li>
    <li><a href="{{participation_marks_page}}" target="_blank" class="dropdown-item"><md>:fas-trophy: Participation Marks List</md></a></li>
    <hr>
    <md>**&nbsp;Individual Project (iP):**</md>
    <li><a href="{{baseUrl}}/admin/ip-overview.html" class="dropdown-item"><md>{{ icon_project }} Individual Project Info</md></a></li>
    <li><a href="{{module_org}}/duke" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Duke Upstream Repo</md></a></li>
    <li><a href="{{ ip_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: iP Code Dashboard</md></a></li>
    <li><a href="{{baseUrl}}/admin/ip-showcase.html" class="dropdown-item"><md>:fas-th-list: iP Showcase</md></a></li>
    <hr>
    <md>**&nbsp;Team Project (tP):**</md>
    <li><a href="{{baseUrl}}/admin/project-expectations.html" class="dropdown-item"><md>{{ icon_project }} Team Project Info</md></a></li>
    <li><a href="{{team_IDs_page}}" target="_blank" class="dropdown-item"><md>:glyphicon-list-alt: Team IDs</md></a></li>
    <li><a href="{{module_org}}/addressbook-level3" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level3</md></a></li>
    <li><a href="https://se-education.org" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level 1,2,4</md></a></li>
    <li><a href="{{ tp_dashboard }}" target="_blank" class="dropdown-item"><md>:fas-chart-area: tP Code Dashboard</md></a></li>
    <li><a href="{{baseUrl}}/admin/projectList.html" class="dropdown-item"><md>:fas-th-list: tP Showcase</md></a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>
    </form>
  </li>
</navbar>
</header>
