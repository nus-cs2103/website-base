<navbar placement="top" type="inverse">
  <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">CS2103/T-AY1718S2</a>
  <li><a href="{{baseUrl}}/index.html">Schedule</a></li>
  
  <dropdown text="Textbook">
    <li><a href="{{baseUrl}}/se-book-adapted/index.html" target="_blank">{{glyphicon_th_list}} Table of Contents</a></li>
    <li><a href="{{baseUrl}}/book/common/outcomes.html" target="_blank">{{glyphicon_th_list}} List of all LOs</a></li>
    <li><a href="{{baseUrl}}/book/common/all.html" target="_blank">{{glyphicon_file}} All as one page</a></li>
    <li><a href="{{baseUrl}}/book/common/print.html" target="_blank">{{glyphicon_print}} Printer-Friendly(ish)</a></li>
  </dropdown> 
  
  <li><a href="{{baseUrl}}/admin/index.html">Admin</a></li>
  <li><a href="{{instructors_page}}">Instructors</a></li>
  <dropdown text="IVLE">
    <li><a href="{{ivle_announcements}}" target="_blank">{{glyphicon_bullhorn}} Announcements</a></li>
    <li><a href="{{ivle_files}}" target="_blank">{{glyphicon_file}} Submissions</a></li>
  </dropdown>   
  <dropdown text="Discuss">
    <li><a href="{{slack_team}}" target="_blank">{{glyphicon_comment}} Slack</a></li>
    <li><a href="{{module_org}}/forum/issues" target="_blank">{{glyphicon_question_sign}} Forum</a></li>
  </dropdown>    
  <dropdown text="Links">
    <li><a href="{{module_org}}/website/issues" target="_blank"> {{glyphicon_thumbs_down}} Report Bugs</a></li>
    <li><a href="{{module_org}}/forum/issues" target="_blank">{{glyphicon_question_sign}} Forum</a></li>
    <li><a href="{{baseUrl}}/schedule/overview/tutorialSchedule.html" target="_blank">{{glyphicon_calendar}} Tutorial Schedule</a></li>
    <li><a href="{{team_IDs_page}}">{{glyphicon_list_alt}} Team IDs</a></li>
    <li><a href="{{java_coding_standard}}" target="_blank">{{glyphicon_file}} Java Coding Standard</a></li>
    <li><a href="{{module_org}}/samplerepo-things" target="_blank">{{glyphicon_compressed}} samplerepo-things</a></li>
    <li><a href="{{module_org}}/addressbook-level1" target="_blank">{{glyphicon_compressed}} Addressbook-level1</a></li>
    <li><a href="{{module_org}}/addressbook-level2" target="_blank">{{glyphicon_compressed}} Addressbook-level2</a></li>
    <li><a href="{{module_org}}/addressbook-level3" target="_blank">{{glyphicon_compressed}} Addressbook-level3</a></li>
    <li><a href="{{module_org}}/addressbook-level4" target="_blank">{{glyphicon_compressed}} Addressbook-level4</a></li>
    <li><a href="{{baseUrl}}/admin/projectList.html" target="_blank">{{glyphicon_folder_open}} Projects List</a></li>
  </dropdown>
  <li slot="right">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback"></searchbar>
    </form>
  </li>
</navbar>
