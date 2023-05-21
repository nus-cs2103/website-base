{% from "common/macros.njk" import get_date with context %}

{% set weekly_admin_tasks = {
week1: [
  {id: 'set_up_tools', deadline: "before the lecture"},
  {id: 'learn_about_the_course'},
  {id: 'attend_the_first_lecture'}
],
week2: [
  {id: 'submit_post_lecture_quiz', deadline: "before the next lecture", graded: true},
  {id: 'get_connect_with_comm_channels'}
],
week3: [
  {id: 'submit_post_lecture_quiz', deadline: "before the next lecture", graded: true}
],
week4: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week5: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week6: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week7: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week8: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week9: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week10: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week11: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week12: [
  {id: 'submit_post_lecture_quiz', graded: true}
],
week13: [
]
} %}
