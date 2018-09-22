<navbar placement="top" type="inverse">
  <a slot="brand" href="{{baseUrl}}/index-flat.html" title="Home" class="navbar-brand">{{ module_pair }} <small>{{ period }}</small></a>
  <dropdown text="Flat" class="nav-link">
    <li><a href="{{baseUrl}}/index-flat.html" class="dropdown-item"> {{ icon_tick }} Flat (current format)</a></li>
    <li><a href="{{baseUrl}}/index.html" class="dropdown-item">&nbsp;&nbsp;&nbsp;&nbsp;Nested</a></li>
  </dropdown>
  <li><a href="{{baseUrl}}/index-flat.html" class="nav-link"><md>**Schedule**</md></a></li>
  <li><a href="{{baseUrl}}/se-book-adapted/index.html" target="_blank" class="nav-link"><md>**Textbook**</md></a></li>

  <li><a href="{{baseUrl}}/admin/index-flat.html" class="nav-link"><md>**Admin Info**</md></a></li>
  <dropdown text="Links" class="nav-link">
    <li><a href="{{bugs_link}}" target="_blank" class="dropdown-item"> {{ fas_bug }} Report Bugs</a></li>
    <li><a href="{{slack_team}}" target="_blank" class="dropdown-item">{{ fab_slack_hash }} Slack</a></li>
    <li><a href="{{forum_link}}" target="_blank" class="dropdown-item">{{ fas_comment }} Forum</a></li>
    <li><a href="{{ instructors_page }}" target="_blank" class="dropdown-item">{{ fas_user_tie }} Instructors</a></li>
    <li><a href="{{ivle_announcements}}" target="_blank" class="dropdown-item">{{ glyphicon_bullhorn }} Announcements</a></li>
        <li><a href="{{ivle_files}}" target="_blank" class="dropdown-item">{{ fas_file_upload }} File Submissions</a></li>
    <li><a href="{{baseUrl}}/admin/tutorials.html" target="_blank" class="dropdown-item">{{ glyphicon_calendar }} Tutorial Schedule</a></li>
    <li><a href="{{team_IDs_page}}" target="_blank" class="dropdown-item">{{ glyphicon_list_alt }} Team IDs</a></li>
    <li><a href="{{java_coding_standard}}" target="_blank" class="dropdown-item">{{ fas_code }} Java Coding Standard</a></li>
    <li><a href="{{module_org}}/samplerepo-things" target="_blank" class="dropdown-item">{{ icon_repo }} samplerepo-things</a></li>
    <li><a href="{{module_org}}/addressbook-level1" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level1</a></li>
    <li><a href="{{module_org}}/addressbook-level2" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level2</a></li>
    <li><a href="{{module_org}}/addressbook-level3" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level3</a></li>
    <li><a href="{{module_org}}/addressbook-level4" target="_blank" class="dropdown-item">{{ icon_repo }} Addressbook-level4</a></li>
    <li><a href="{{baseUrl}}/admin/projectList.html" class="dropdown-item">{{ fas_th_list }} Projects List</a></li>
    <li><a href="https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/{{ module | lower }}-dashboard" target="_blank" class="dropdown-item">{{ fas_chart_area }} Project Code Dashboard (BETA)</a></li>
  </dropdown>
</navbar>
