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
  {id: 'refine_product_design'}
],
week7: [
  {id: 'set_up_project_repo', deadline: 'during the tutorial', deadline_type: "info"},
  {id: 'plan_the_next_iteration'}
],
week8: [
  {id: 'ensure_you_know_tp_expectations'},
  {id: 'start_implementing_first_version'},
  {id: 'use_github_to_manage_milestones'},
  {id: 'add_junit_tests'}
],
week9: [
  {id: 'make_code_more_defensive'},
  {id: 'deliver_first_version', deadline: 'midnight before the tutorial'},
  {id: 'do_an_informal_demo', deadline: 'before the tutorial', deadline_type: "info"}
],
week10: [
  {id: 'start_on_the_penultimate_version'},
  {id: 'update_dg_with_design_details', deadline: 'IMPORTANT'},
  {id: 'smoke_test_catcher', deadline: 'IMPORTANT', graded: true},
  {id: 'make_code_reposense_compatible'}
],
week11: [
  {id: 'update_user_docs'},
  {id: 'add_sd_to_dg', deadline: 'recommended: before ' + day_first_tutorial, deadline_type: 'info'},
  {id: 'deliver_penultimate_version', deadline: 'midnight before the tutorial'},
  {id: 'review_others_dg', deadline: 'during the tutorial', graded: true}
],
week12: [
  {id: 'attend_the_PED', deadline: 'During the lecture on ' + get_date(date_w12_start, time=""), graded: true},
  {id: 'start_fixing_PED_bugs', deadline: 'Before the tutorial'},
  {id: 'tweak_product_as_per_PED'},
  {id: 'draft_the_ppp'},
  {id: 'double_check_reposense_compatibility'}
],
week13: [
  {id: 'submit_final_deliverables', deadline: get_date(date_w13_start, 3)},
  {id: 'demo_the_product', deadline: get_date(date_w13_start, 5)},
  {id: 'prepare_for_PE'},
  {id: 'attend_the_PE', deadline: 'during the lecture on ' + get_date(date_w13_start, 7, time="")}
]
} %}

{% set weekly_tp_themes = {
  w3: {name: "Kickoff"},
  w4: {name: "Set direction"},
  w5: {name: "Gather requirements"},
  w6: {name: "Conceptualize the product"},
  w7: {name: "Get ready for iterations"},
  w8: {name: "mid-" + version_first},
  w9: {name: version_first, milestone: version_first},
  w10: {name: "mid-" + version_penultimate},
  w11: {name: version_penultimate, milestone: version_penultimate},
  w12: {name: "mid-" + version_final},
  w13: {name: version_final, milestone: version_final}
} %}
