{% from "common/macros.njk" import get_date with context %}

{% set weekly_admin_tasks = {
week1: [
  {id: 'set_up_tools', deadline: "before the lecture"},
  {id: 'learn_about_the_course'},
  {id: 'attend_the_first_lecture'}
],
week2: [
  {id: 'get_connect_with_comm_channels'}
],
week3: [],
week4: [],
week5: [
  {id: 'practice_peer_evaluations_on_TEAMMATES', deadline: get_date(date_w5_start, 6), graded: true}
],
week6: [],
week7: [],
week8: [
  {id: 'submit_midterm_peer_evaluations', deadline: get_date(date_w8_start, 9), graded: true}
],
week9: [],
week10: [],
week11: [],
week12: [],
week13: [
  {id: 'submit_final_peer_evaluations', deadline: get_date(date_w13_start, 6), graded: true}
]
} %}
