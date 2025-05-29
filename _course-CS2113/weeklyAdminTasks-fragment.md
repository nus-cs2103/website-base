{% from "common/macros.njk" import get_date with context %}

{% set weekly_admin_tasks = {
week1: [
  {id: 'set_up_tools', deadline: "before the lecture"},
  {id: 'submit_pre_course_survey', deadline: "by Friday 2359"},
  {id: 'learn_about_the_course'},
  {id: 'attend_the_first_lecture'}
],
week2: [
  {id: 'submit_first_coding_exercises', deadline: get_date(date_w2_start, 3)},
  {id: 'get_connect_with_comm_channels'}
],
week3: [
  {id: 'submit_coding_exercises', graded: true, deadline: "midnight before tutorial"},
  {id: 'form_teams'}
],
week4: [
  {id: 'accept_github_invitations', graded: true},
  {id: 'submit_coding_exercises', graded: true}
],
week5: [
  {id: 'submit_coding_exercises', graded: true},
  {id: 'practice_peer_evaluations_on_TEAMMATES', deadline: get_date(date_w5_start, 5)}
],
week6: [
  {id: 'submit_coding_exercises', graded: true},
  {id: 'submit_post_lecture_quiz', graded: true, deadline: "before the next lecture"},
  {id: 'submit_midterm_feedback_for_the_course', deadline: get_date(date_w6_start, 12), deadline_type: 'info'}
],
week7: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week8: [
  {id: 'submit_post_lecture_quiz', graded: true, deadline: "before the next lecture"}
],
week9: [
  {id: 'submit_post_lecture_quiz', graded: true, deadline: "before the next lecture"},
  {id: 'submit_midterm_peer_evaluations', graded: true, deadline: get_date(date_w9_start, 4)}
],
week10: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week11: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week12: [
  {id: 'submit_post_lecture_quiz', graded: true},
  {id: 'submit_final_peer_evaluations', graded: true, deadline: get_date(date_w12_start, 3)}
],
week13: [
  
]
} %}
