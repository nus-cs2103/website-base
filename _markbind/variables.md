<!-- ===========================  primary module configuration ============================================= -->

<span id="module">CS2103</span>
<span id="module_pair">CS2103/T</span>
<span id="module_name">Software Engineering</span>
<span id="module_color">success</span>

<span id="S">1</span>
<span id="semester">AY2021S{{ S }}</span>
<span id="period">2020 Aug-Dec</span>

<span id="instructors_page">https://docs.google.com/document/d/e/2PACX-1vQe3k_8EDv73v8PmGf0vjoJWVh1eixYQ31_sNHz1eKfRjVciSwZJ9UDu6H1H4ZxVmqKy9CY4vRAq7cv/pub?embedded=true</span>
<span id="team_IDs_page">https://docs.google.com/spreadsheets/d/e/2PACX-1vRuJ9gGqFSvZci_uqivCoBipX5AOjJa7DgxRIDQ60xFnH-KEqPyEINmo4M0BJYENj7sS4dcMgRcnnMN/pubhtml?gid=0&single=true</span>
<span id="pr_review_mapping">https://docs.google.com/spreadsheets/d/e/2PACX-1vRWi6lYGxlvJF-O--ndWa5PU7LKREcoKLAUJ8QRNtBy-9TYkg2MnNPy_KrdO7zH9fbaVZ455nDnNpPd/pubhtml?gid=0&single=true</span>
<span id="files_link">https://luminus.nus.edu.sg/modules/852a7711-54a0-4103-a2f7-3d877f33a454/files</span>
<span id="announcements_link">https://luminus.nus.edu.sg/modules/852a7711-54a0-4103-a2f7-3d877f33a454/announcements/active</span>
<span id="java_coding_standard">{{ baseUrl }}/coding-standards/java/intermediate.html</span>
<span id="first_version">v1.2</span>
<span id="penultimate_version">v1.3</span>
<span id="final_version">v1.4</span>
<span id="future_version">v2.0</span>

<variable name="date_semester_start">2020-08-10</variable>
<variable name="date_first_lecture">2020-08-14</variable>
<variable name="day_lecture">{{ date_first_lecture | date("dddd") }}</variable>
<variable name="date_final_submission">2020-11-09</variable>
<variable name="format_normal">ddd, MMM Do</variable>

<variable name="marks_ip">20</variable>
<variable name="marks_tp">45</variable>
<variable name="marks_tp_design">5</variable>
<variable name="marks_tp_documentation">10</variable>
<variable name="marks_tp_implementation">10</variable>
<variable name="marks_tp_pm">10</variable>
<variable name="marks_tp_pm_individual">5</variable>
<variable name="marks_tp_pm_team">5</variable>
<variable name="marks_tp_qa">10</variable>
<variable name="marks_participation">5</variable>
<variable name="marks_exam">30</variable>
<variable name="marks_exam_essay">0</variable>
<variable name="marks_exam_mcq">30</variable>
<variable name="mcq_count">100</variable>

<variable name="ug_pages_per_person">1</variable>
<variable name="dg_pages_per_person">3</variable>
<variable name="uml_diagrams_per_person">2 types of</variable>


<!-- ===========================  secondary module configuration =========================================== -->

<span id="edition_badge"><small><small><small><span class='badge badge-pill badge-{{ module_color }}'>{{ module_pair }} edition - {{ period }}</span></small></small></small></span>

<span name="M"><span class="badge badge-info">&nbsp;{{ module }}&nbsp;</span></span>
<span name="MT"><span class="badge badge-warning">{{ module }}T</span></span>

<span id="module_org">https://github.com/nus-{{ module | lower }}-{{ semester }}</span>
<span id="module_gh_pages">https://nus-{{ module | lower }}-{{ semester }}.github.io</span>
<span id="module_website">{{ module_gh_pages }}/website</span>
<span id="ab3_website">https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/tp</span>
<span id="participation_marks_page">www.comp.nus.edu.sg/~cs2103</span>
<span id="bugs_link">{{ module_org | safe }}/forum/issues</span>
<span id="forum_link">{{ module_org | safe }}/forum/issues</span>
<span id="admin_link"><md>[Admin Info page]({{baseUrl}}/admin/index.html)</md></span>
<span id="schedule_link"><md>[Schedule page]({{baseUrl}}/schedule/index.html)</md></span>
<span id="ip_dashboard">https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/ip-dashboard/#sort=groupTitle&groupSelect=groupByAuthors</span>
<span id="tp_dashboard">https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/tp-dashboard</span>

<!-- ===========================  icons ================================================= -->

<span id="icon_announcement"><md>:fas-bell:</md></span>
<span id="icon_book"><md>:fas-book:</md></span>
<span id="icon_calendar"><md>:fas-calendar-alt:</md></span>
<span id="icon_deadline"><md>:fas-clock:</md></span>
<span id="icon_dislike"><md>:fas-thumbs-down:</md></span>
<span id="icon_example"><md>:fas-cube:</md></span>
<span id="icon_embedding"><md>:glyphicon-log-in:</md></span>
<span id="icon_exercise"><md>:fas-dumbbell:</md></span>
<span id="icon_extra"><span class='badge badge-pill badge-secondary'><md>:fas-plus: extra</md></span></span>
<span id="icon_evidence"><md>:fas-briefcase:</md></span>
<span id="icon_info"><md>:fas-info-circle:</md></span>
<span id="icon_individual"><md>:fas-user:</md></span>
<span id="icon_lecture"><md>:glyphicon-blackboard:</md></span>
<span id="icon_like"><md>:fas-thumbs-up:</md></span>
<span id="icon_linux"><md>:fab-linux:</md></span>
<span id="icon_important_big_red"><font color="red"><big>:glyphicon-exclamation-sign:</big></font></span>
<span id="icon_important"><md>:glyphicon-exclamation-sign:</md></span>
<span id="icon_new_window"><md>:glyphicon-new-window:</md></span>
<span id="icon_outcome"><md>:fas-trophy:</md></span>
<span id="icon_output"><md>:fas-arrow-down:</md></span>
<span id="icon_output_right"><md>:fas-arrow-right:</md></span>
<span id="icon_print"><md>:glyphicon-print:</md></span>
<span id="icon_prereq"><md>:glyphicon-education:</md></span>
<span id="icon_preview"><md>:glyphicon-eye-open:</md></span>
<span id="icon_pro_tip"><span class="badge badge-pill badge-warning">:fas-lightbulb: PRO TIP</span></span>
<span id="icon_project"><md>:fas-drafting-compass:</md></span>
<span id="icon_Q"><md>:glyphicon-question-sign:</md></span>
<span id="icon_Q_A">{{ icon_Q | safe }}:glyphicon-ok-sign:</span>
<span id="icon_resource"><md>:fas-paperclip:</md></span>
<span id="icon_team"><md>:fas-users:</md></span>
<span id="icon_terminal"><smal><span class="badge badge-secondary">&gt;_</span></smal></span>
<span id="icon_text"><md>:far-file-alt:</md></span>
<span id="icon_tick"><md>:fas-check:</md></span>
<span id="icon_tip"><span class="badge badge-pill badge-warning">:fas-lightbulb:</span></span>
<span id="icon_tick_green"><span style="color:green">{{ icon_tick | safe }}</span></span>
<span id="icon_todo"><md>:glyphicon-check:</md></span>
<span id="icon_tutorial"><md>:fas-chalkboard-teacher:</md></span>
<span id="icon_slides"><md>:far-images:</md></span>
<span id="icon_video"><md>:glyphicon-facetime-video:</md></span>
<span id="icon_windows"><md>:fab-windows:</md></span>
<span id="icon_x"><md>:fas-times:</md></span>
<span id="icon_x_red"><span style="color:red">{{ icon_x | safe }}</span></span>
<span id="bad"><font color="red"><md>**{{ icon_dislike | safe }} Bad**</md></font></span>
<span id="good"><font color="green"><md>**{{ icon_like | safe }} Good**</md></font></span>
<variable name="pros"><span class="text-success">**pros:**</span></variable>
<variable name="cons"><span class="text-danger">**cons:**</span></variable>
<span id="icon_repo"><md>:fas-code-branch:</md></span>

<span id="s"><md>:glyphicon-star:</md></span>
<span id="star"><span class='glyphicon glyphicon-star' aria-hidden='true'></span></span>
<span id="one_star"><span class='badge badge-pill badge-light text-danger'>{{ star | safe }} </span></span>
<span id="prereq_no_stars"><span class='badge badge-pill badge-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }}</span></span>
<span id="prereq_one_star"><span class='badge badge-pill badge-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }} </span></span>
<span id="two_stars"><span class='badge badge-pill badge-light text-warning'>{{ star | safe }}{{ star | safe }} </span></span>
<span id="prereq_two_stars"><span class='badge badge-pill badge-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }} </span></span>
<span id="three_stars"><span class='badge badge-pill badge-light text-primary'>{{ star | safe }}{{ star | safe }}{{ star | safe }} </span></span>
<span id="prereq_three_stars"><span class='badge badge-pill badge-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }}{{ star | safe }} </span></span>
<span id="four_stars"><span class='badge badge-pill badge-success'>{{ star | safe }}{{ star | safe }}{{ star | safe }}{{ star | safe }}: OPTIONAL</span></span>
<span id="prereq_four_stars"><span class='badge badge-pill badge-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }}{{ star | safe }}{{ star | safe }} </span></span>
<span id="hr_double"><hr style="border-top: 3px double #c5c5c5;"></span>

<!-- ===========================  misc aliases =========================================== -->

<span id="pagebreak"><p style="page-break-after: always;">&nbsp;</p></span>
<span id="dashed_line"><hr style="border-top: dashed 1px; border-color:grey" /></span>
<span id="dotted_line"><hr style="border-width: 1px; border-color: #f3ccff; border-style: dotted"></span>
<span id="evidence"><big>{{ icon_evidence | safe }} Evidence:</big></span>
