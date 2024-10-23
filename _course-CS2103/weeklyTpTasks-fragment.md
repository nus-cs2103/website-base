{% from "common/macros.njk" import get_date with context %}

{% set weekly_tp_tasks = {
week3: [
  {id: 'get_familiar_with_ab3', deadline: get_date(date_w3_start, 5, time="23:59")},
  {id: 'set_up_meeting_time', deadline: 'by the end of the tutorial'},
  {id: 'check_collective_ip_status', deadline: get_date(date_w4_start, 1, time="")}
],
week4: [
  {id: 'start_weekly_meetings'},
  {id: 'start_project_notes', deadline: 'before the tutorial'},
  {id: 'decide_project_direction', deadline: 'decide by tutorial, submit by Sat'}
],
week5: [
  {id: 'brainstorm_user_stories', deadline: 'before the tutorial'},
  {id: 'prioritize_user_stories', deadline: 'before/during the tutorial'}
],
week6: [
  {id: 'conceptualize_first_version'},
  {id: 'draft_the_ug', deadline: get_date(date_w6_start, 6, time="23:59")},
  {id: 'set_up_project_repo'},
  {id: 'get_familiar_with_the_code_base'}
],
week7: [
  {id: 'do_a_practice_iteration', deadline: get_date(date_w7_start, 3, time="23:59")},
  {id: 'update_website_aboutus_readme'},
  {id: 'update_dg_user_stories_etc'},
  {id: 'start_the_next_iteration'}
],
week8: [
  {id: 'divide_mvp_features'},
  {id: 'rename_packages'},
  {id: 'add_first_functionality_increment', deadline: get_date(date_w8_start, 3, time="23:59")}
],
week9: [
  {id: 'plan_the_first_product_release'},
  {id: 'deliver_first_version', deadline: get_date(date_w9_start, 3, time="23:59")}
],
week10: [
  {id: 'do_a_postmortem', deadline: 'before the tutorial'},
  {id: 'plan_the_alpha_version'},
  {id: 'deliver_the_alpha_version', deadline: get_date(date_w10_start, 3, time="23:59")},
  {id: 'smoke_test_catcher', deadline: '[COMPULSORY] ' + get_date(date_w10_start, 4, time="16:00"), graded: true},
  {id: 'start_updating_uml_diagrams'}
],
week11: [
  {id: 'alpha_test_product'},
  {id: 'fix_alpha_test_bugs'},
  {id: 'update_ug_dg'},
  {id: 'release_as_a_jar_file', deadline: get_date(date_w12_start, 3, time="23:59")}
],
week12: [
  {id: 'finish_remaining_tasks'},
  {id: 'attend_the_PED', deadline: get_date(date_w12_start, 4, time="1600-1800"), graded: true}
],
week13: [
  {id: 'start_fixing_PED_bugs'},
  {id: 'submit_final_deliverables', deadline: get_date(date_final_submission, time=time_final_submission)},
  {id: 'prepare_for_PE'},
  {id: 'make_code_reposense_compatible'},
  {id: 'attend_the_PE', deadline: get_date(date_w13_start, 4, format=format_normal, time="1600-1800"), deadline_type: 'warning'},
  {id: 'attend_the_makeup_PE', deadline: get_date(date_w13_start, 6, format=format_normal, time="1400-1600"), deadline_type: 'secondary'}
]
} %}

{% set weekly_tp_themes = {
  w3: {name: "Kickoff"},
  w4: {name: "Set direction"},
  w5: {name: "Gather requirements"},
  w6: {name: "Define the MVP"},
  w7: {name: "Practice iteration → " + version_practice, milestone: version_practice},
  w8: {name: "First feature increment → " + version_first, milestone: version_first},
  w9: {name: "MVP → " + version_mvp, milestone: version_mvp},
  w10: {name: "Alpha version → " + version_alpha, milestone: version_alpha},
  w11: {name: "Release candidate → " + version_penultimate, milestone: version_penultimate},
  w12: {name: "Extra week for " + version_penultimate},
  w13: {name: "Public release → " + version_final, milestone: version_final}
} %}
