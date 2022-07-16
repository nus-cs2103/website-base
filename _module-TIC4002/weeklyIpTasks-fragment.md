{% from "common/macros.njk" import get_date with context %}

{% set weekly_ip_tasks = {
week2: [
  {id: 'learn_about_the_project'},
  {id: 'set_up_project_tic4002'},
  {id: 'create_pr_to_upstream'},
  {id: 'ensure_tic4001_increments'},
  {id: 'add_increments', increments:  [
    {id: 'A-Gradle', title: 'Use Gradle'}
  ]},
  {id: 'stricter_coding_standard'}
],
week3: [
  {id: 'add_increments', increments:  [
    {id: 'Level-10', title: 'Add a GUI'}
  ]},
  {id: 'generate_new_jar'}
],
week4: [
  {id: 'add_increments', increments:  [
    {id: 'A-CI', title: 'Set up CI'}
  ]},
  {id: 'add_an_extension'}
],
week5: [
  {id: 'more_code_quality'},
  {id: 'start_next_week_tasks'}
],
week6: [
  {id: 'update_website'},
  {id: 'submit_the_final_version', deadline: get_date(date_w6_start, 9)}
]
} %}
