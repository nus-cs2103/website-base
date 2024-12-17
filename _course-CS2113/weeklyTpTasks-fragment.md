{% from "common/macros.njk" import get_date with context %}

{% set weekly_tp_tasks = {
week3: [
  {id: 'set_up_meeting_time', deadline: 'by the end of the tutorial'}
],
week4: [
  {id: 'start_weekly_meetings'},
  {id: 'start_project_notes', deadline: 'before the tutorial'},
  {id: 'decide_project_direction', deadline: 'before the tutorial'}
],
week5: [
  {id: 'brainstorm_user_stories', deadline: 'before the tutorial'},
  {id: 'prioritize_user_stories', deadline: 'during the tutorial', deadline_type: "info"}
],
week6: [
  {id: 'conceptualize_first_version'},
  {id: 'draft_the_ug', deadline: 'midnight before the tutorial'},
  {id: 'set_up_project_repo', deadline: 'during the tutorial', deadline_type: "info"}
],
week7: [
  {id: 'ensure_you_know_tp_expectations'},
  {id: 'plan_the_next_iteration'},
  {id: 'start_the_next_iteration'}
],
week8: [
  {id: 'start_implementing_first_version'},
  {id: 'add_junit_tests'}
],
week9: [
  {id: 'make_code_more_defensive'},
  {id: 'deliver_first_version', deadline: 'midnight before the tutorial'},
  {id: 'do_an_informal_demo', deadline: 'during the tutorial', deadline_type: "info"}
],
week10: [
  {id: 'start_on_the_penultimate_version'},
  {id: 'update_dg_with_design_details', deadline: 'IMPORTANT'},
  {id: 'smoke_test_catcher', deadline: 'IMPORTANT', graded: true},
  {id: 'make_code_reposense_compatible'}
],
week11: [
  {id: 'update_ug_dg'},
  {id: 'review_others_dg', deadline: 'during the tutorial', graded: true},
  {id: 'deliver_penultimate_version', deadline: get_date(date_w12_start, 3, time="23:59")},
  {id: 'draft_the_ppp'}
],
week12: [
{id: 'finish_remaining_tasks'},
  {id: 'attend_the_PED', deadline: 'During the lecture on ' + get_date(date_w12_start, 4, time=""), graded: true}
],
week13: [
  {id: 'start_fixing_PED_bugs'},
  {id: 'submit_final_deliverables', deadline: get_date(date_final_submission, time=time_final_submission)},
  {id: 'demo_the_product'},
  {id: 'prepare_for_PE'},
  {id: 'attend_the_PE', deadline: 'during the lecture on ' + get_date(date_w13_start, 4, time="")}
]
} %}

{% set weekly_tp_themes = {
  w3: {name: "Kickoff"},
  w4: {name: "Set direction"},
  w5: {name: "Gather requirements"},
  w6: {name: "Define MVP, set up repo"},
  w7: {name: "Plan the iteration"},
  w8: {name: "mid-" + version_mvp},
  w9: {name: version_mvp, milestone: version_mvp},
  w10: {name: "mid-" + version_penultimate},
  w11: {name: version_penultimate, milestone: version_penultimate},
  w12: {name: "Extra week for " + version_penultimate},
  w13: {name: version_final, milestone: version_final}
} %}
