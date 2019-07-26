{% from "schedule/index.md" import weeks, current_weeks with context %}
<header>
<navbar placement="top" type="dark">
  <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">{{ module_pair }} <small>{{ period }}</small></a>
  <dropdown text="Schedule" class="nav-link">
  <li><a href="{{baseUrl}}/schedule/timeline.html" class="dropdown-item"><md>**Full Timeline**</md></a></li>
{% for week in weeks %}
<li><a href="{{ baseUrl }}/schedule/week{{ week.num }}/index.html" class="dropdown-item"> <md>**Week {{ week.num }}** [{{ week.day }}] {% if current_weeks[0] == week.num %} :fas-arrow-circle-left:{% endif %}</md></a></li>
{% endfor %}
  </dropdown>
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" class="nav-link"><md>**Textbook**</md></a></li>
  <li><a href="{{baseUrl}}/admin/index.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown text="Links" class="nav-link">
    <li><a href="{{bugs_link}}" target="_blank" class="dropdown-item"><md>:fas-bug: Report Bugs</md></a></li>
    <li><a href="{{slack_team}}" target="_blank" class="dropdown-item"><md>:fab-slack-hash: Slack</md></a></li>
    <li><a href="{{forum_link}}" target="_blank" class="dropdown-item"><md>:fas-comment: Forum</md></a></li>
    <li><a href="{{baseUrl}}/admin/project-overview.html" class="dropdown-item"><md>{{ icon_project }} Project Info</md></a></li>
    <li><a href="{{ baseUrl }}/admin/instructors.html" class="dropdown-item"><md>:fas-user-tie: Instructors</md></a></li>
    <li><a href="{{ivle_announcements}}" target="_blank" class="dropdown-item"><md>:glyphicon-bullhorn: Announcements</md></a></li>
    <li><a href="{{ivle_files}}" target="_blank" class="dropdown-item"><md>:fas-file-upload: File Submissions</md></a></li>
    <li><a href="{{baseUrl}}/admin/tutorials.html" target="_blank" class="dropdown-item"><md>:glyphicon-calendar: Tutorial Schedule</md></a></li>
    <li><a href="{{team_IDs_page}}" target="_blank" class="dropdown-item"><md>:glyphicon-list-alt: Team IDs</md></a></li>
    <li><a href="{{java_coding_standard}}" target="_blank" class="dropdown-item"><md>:fas-code: Java Coding Standard</md></a></li>
    <li><a href="{{module_org}}/samplerepo-things" target="_blank" class="dropdown-item"><md>{{ icon_repo }} samplerepo-things</md></a></li>
    <li><a href="{{module_org}}/addressbook-level1" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level1</md></a></li>
    <li><a href="{{module_org}}/addressbook-level2" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level2</md></a></li>
    <li><a href="{{module_org}}/addressbook-level3" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level3</md></a></li>
    <li><a href="{{module_org}}/addressbook-level4" target="_blank" class="dropdown-item"><md>{{ icon_repo }} Addressbook-level4</md></a></li>
    <li><a href="{{baseUrl}}/admin/projectList.html" class="dropdown-item"><md>:fas-th-list: Projects List</md></a></li>
    <li><a href="{{baseUrl}}/admin/reposenseConfigTemplates.html" class="dropdown-item"><md>:fas-th-list:</md> config.json templates for Reposense</a></li>
    <li><a href="https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/{{ module | lower }}-dashboard" target="_blank" class="dropdown-item"><md>:fas-chart-area: Project Code Dashboard (BETA)</md></a></li>
  </dropdown>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>
    </form>
  </li>
</navbar>
</header>
