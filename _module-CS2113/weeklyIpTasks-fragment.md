{% from "common/macros.njk" import get_date with context %}

{% set weekly_ip_tasks = {
week2: [
  {id: 'learn_about_the_project'},
  {id: 'set_up_prerequisites'},
  {id: 'set_up_project'},
  {id: 'add_increments', suffix: '', increments: [
    {id: 'Level-0', title: 'Greet'}
  ]}
],
week3: [
  {id: 'finish_leftover_tasks'},
  {id: 'add_increments', suffix: ' (+ commit, tag, push)', increments: [
    {id: 'Level-1', title: 'Greet, Echo, Exit'},
    {id: 'Level-2', title: 'Add, List'},
    {id: 'Level-3', title: 'Mark as Done'},
    {id: 'A-CodingStandard', title: 'Follow the Coding Standard'}
  ]}
],
week4: [
  {id: 'create_pr_to_upstream', deadline: get_date(date_w4_start, 3)},
  {id: 'add_increments', suffix: '', increments: [
    {id: 'Level-4', title: 'ToDo, Event, Deadline'},
    {id: 'A-TextUiTesting', title: 'Automated Text UI Testing', tag: 'optional'},
    {id: 'A-CodeQuality', title: 'Improve Code Quality'}
  ]},
  {id: 'prepare_for_pr_reviews', deadline: 'before the tutorial'},
  {id: 'review_two_prs', deadline: 'during the tutorial', graded: true}
],
week5: [
  {id: 'learn_from_others'},
  {id: 'add_increments', suffix: ' as a branch', increments:  [
    {id: 'Level-5', title: 'Handle Errors'}
  ]},
  {id: 'add_increments', suffix: '', increments:  [
    {id: 'A-Packages', title: 'Organize into Packages', tag: 'optional'}
  ]}
],
week6: [
  {id: 'add_increments', suffix: ' as parallel branches', increments:  [
    {id: 'Level-6', title: 'Delete'},
    {id: 'Level-7', title: 'Save'}
  ]},
  {id: 'add_increments', suffix: '', increments:  [
    {id: 'A-Jar', title: 'Create a JAR File'}
  ]}
],
week7: [
  {id: 'add_increments', suffix: '', increments:  [
    {id: 'A-MoreOOP', title: 'Use More OOP'}
  ]},
    {id: 'add_increments', suffix: ' as PRs', increments:  [
    {id: 'Level-8', title: 'Dates and Times', tag: 'optional'},
    {id: 'Level-9', title: 'Find'},
    {id: 'A-JavaDoc', title: 'JavaDoc'}
  ]},
  {id: 'set_up_website'},
  {id: 'submit_the_final_version', deadline:  get_date(date_w7_start, 14)}
],
week8: [
  {id: 'evaluate_peer_ips', deadline: 'before next week lecture', graded: true}
]
} %}
