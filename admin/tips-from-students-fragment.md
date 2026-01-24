{% set tips = {
  focus_on_process: {
    header: "Focus on the process",
    tags: ['AY2526S1', 'tP', 'workload'],
    body: "Don't stress too much about the product; it's more about the process of building it. Keep it simple."
  },
  follow_the_timeline: {
    header: "Follow the timeline",
    tags: ['AY2526S1', 'workload', 'schedule'],
    body: "It is better to follow the timeline of the course. Don't stack everything until the last minute."
  },
  plan_project_early: {
    header: "Do more early planning",
    tags: ['AY2526S1', 'tP'],
    body: "It would be ideal to properly plan out the project in the early stages so as to minimize the number of additional features/changes made along the way."
  },
  do_more_in_early_iterations: {
    header: "Do more work in earlier iterations",
    tags: ['AY2526S1', 'tP', 'workload'],
    body: "Plan more work for early iterations in TP instead of just meeting the requirements. Early iterations can be quite chill while mid-late iterations will be very busy"
  },
  keep_up_with_the_schedule: {
    header: "Keep the tempo with the weekly schedule",
    tags: ['AY2526S1', 'schedule', 'workload'],
    body: "keep tempo with the weekly schedule."
  },
  mod_demands_consistency: {
    header: "Mod demands consistency",
    tags: ['AY2526S1', 'schedule', 'workload'],
    body: "The mod really demands consistency, not something that can be pushed or done last minute."
  },
  take_notes_during_tutorials: {
    header: "Take notes during tutorials",
    tags: ['AY2526S1', 'tutorials', 'grade', 'exam', 'learning'],
    body: "Tutorials are likely to be undervalued but taking notes then will prob help for finals alot. Learning > grades"
  },
  watch_lecture_videos: {
    header: "Watch lecture videos",
    tags: ['AY2526S1', 'lectures', 'grade', 'exam', 'learning'],
    body: "Watch every lecture video so that you are familiar with the massive course content."
  },
  workload_is_what_you_make_it: {
    header: "Workload is what you make it to be",
    tags: ['AY2526S1', 'workload', 'tP'],
    body: "Workload is what u make it to be. As long as u meet around minimum functionality/lines of code, the course can be very manageable."
  },
  not_as_daunting: {
    header: "Not as daunting as it seems",
    tags: ['AY2526S1', 'workload'],
    body: "Put in sufficient effort for CS2103T and it shouldn't be as daunting as it seems."
  },
  consolidate_bugs_to_look_for_in_pe: {
    header: "Consolidate bugs to look for in PE",
    tags: ['AY2526S1', 'PE'],
    body: "It is good to consolidate some ideas of what kinds of bugs to test for beforehand to efficiently use the time"
  },
  have_a_good_communication_framework: {
    header: "Have a good communication framework with your team",
    tags: ['AY2526S1', 'tP'],
    body: "Have a good communication framework with ur team."
  },
  design_features_early: {
    header: "Design features early",
    tags: ['AY2526S1', 'tP', 'schedule'],
    body: "Design your feature with final version, do not delay it, thinking that you will improve it later on. you do not have time later on, and when you delay it, you will just forget about it which become a bug later on."
  },
  design_features_early: {
    header: "Double-check AI-generated code",
    tags: ['AY2526S1', 'iP', 'tP', 'AI', 'learning'],
    body: "If using AI, adopt the mindset of a software architect if you are proficient. Or if you are not strong in fundamentals, learn on the fly as you use AI to help with our already stressful schoolwork.<br>Please please please double check AI-generated code; it is super easy to introduce subtle bugs this way."
  },
  review_concepts: {
    header: "Review concepts",
    tags: ['AY2526S1', 'exam', 'learning'],
    body: "I think reviewing the concepts in the textbook (via quizzes or whatever) is important to score well in the exam."
  },
  dont_add_extra_features: {
    header: "Don't add extra features",
    tags: ['AY2425S2', 'iP', 'tP', 'workload'],
    body: "Don't add extra features for your IP or TP as you are better off spending that time focusing on other mods and it most likely won't add to your final marks too. Instead focus on just learning the core SWE concepts and do only what is necessary for the IP and TP."
  },
  kee_projet_scope_small: {
    header: "Keep project scope small",
    tags: ['AY2425S2', 'iP', 'tP', 'workload'],
    body: "Keep the project scope small and adjust according to your individual and team capabilities."
  },
  hold_teammates_accountable: {
    header: "Hold all teammates accountable",
    tags: ['AY2425S2', 'tP'],
    body: "Please ensure that all your teammates are accountable, and have a stipulated deadline set for individual tasks. You probably won't want to deal with 17 files during a merge conflict at 1am :)"
  },
  be_honest_with_team_members: {
    header: "Be honest with team members",
    tags: ['AY2425S2', 'tP'],
    body: "Set an expectation of your team early, make sure to be honest with each other! But still be ready in case anything happens."
  },
  have_a_project_leader: {
    header: "Have a project leader",
    tags: ['AY2425S2', 'tP'],
    body: "Have a leadership role early and be prepared to take over if needed"
  },
  learn_content_along_the_way: {
    header: "Learn content along the way",
    tags: ['AY2425S2', 'exam', 'schedule', 'learning'],
    body: "For finals, do them as the sem goes not at the end cuz theres a lot to remember."
  },
  start_early_or_die: {
    header: "Start early or die!",
    tags: ['AY2425S2', 'workload', 'schedule'],
    body: "Start early or die due to the workload."
  },
  put_effort_into_design_early: {
    header: "Put effort into design early",
    tags: ['AY2425S2', 'tP'],
    body: "At the beginning of a project, put effort into design. It will pay off later. Once you start debugging, you'll thank yourself."
  },
  set_a_suitable_meeting_time: {
    header: "Set a suitable meeting time",
    tags: ['AY2425S1', 'tP', 'schedule'],
    body: "Set a suitable meeting time for your tP, preferably one or two days after the weekly deadline on Thursday, 11:59 PM.<br>Reason: Delegating of tasks can be done earlier so you would have more time to complete them, rather than rushing everything at the last minute."
  },
  ask_in_forum: {
    header: "When in doubt, ask in the forum",
    tags: ['AY2425S1', 'misc'],
    body: "When in doubt, ask in the forum. Profs (or other students) would most likely answer your question promptly."
  },
  start_eary_everything: {
    header: "Start early, everthing!",
    tags: ['AY2425S1', 'schedule', 'learning'],
    body: "Start early in everything (lecture, ip, tp)."
  },
  stay_on_schedule: {
    header: "Stay on schedule",
    tags: ['AY2425S1', 'schedule', 'workload'],
    body: "Try your best to stay on track with the weekly tasks. Even though it might feel like you can catch up later, sometimes the work accumulates, and it seems even more difficult then."
  },
  get_to_think_on_how_to_work_in_projects: {
    header: "You get to think how to work on a project",
    tags: ['AY2425S1', 'tP', 'iP', 'learning'],
    body: "The course is quite useful in making you think about how to work on a project, especially in the second half with your project team, and initially it might seem as unnecessary (for eg user stories), but it really helps you narrow down what exactly you want from the app, and what exactly should you focus on."
  },
  tutorials_help: {
    header: "Tutorials do help",
    tags: ['AY2425S1', 'tutorials', 'learning'],
    body: "The tutorials are actually a great way to practically apply your weekly knowledge, and I have noticed some students tend to underestimate this."
  },
  be_wary_of_end_of_sem_crunch: {
    header: "Be wary of end-of-semester crunch",
    tags: ['AY2425S1', 'schedule', 'tP'],
    body: "Be wary of the crunch within the last few weeks of the semester when planning modules or allocating time for assignments."
  },
  read_pe_instructions_beforehand: {
    header: "Read PE grading instructions beforehand",
    tags: ['AY2425S1', 'PE', 'tP'],
    body: "For the PE, please read the bug grading instructions beforehand, and make sure you understand them."
  },
  dont_plan_to_game_grading: {
    header: "Read PE grading instructions beforehand",
    tags: ['AY2425S1', 'learning', 'grade'],
    body: "Don't come in with the expectation of gaming the grading components.<br>If you don't have SWE experience, what this course teaches is quite important. It is more important for you to understand the concept compared to scoring the grade."
  },
  beware_of_unforeseen_challenges: {
    header: "Beware of unforeseen challenges",
    tags: ['AY2425S1', 'scheduling', 'grade'],
    body: "Do not push your work to the deadline, and start work on the deliverables early. There are often a lot of unforeseen challenges and it can be really stressful trying to resolve them nearing deadlines."
  },
  do_weekly_readings: {
    header: "Do the weekly readings",
    tags: ['AY2425S1', 'learning', 'exam', 'schedule'],
    body: "Do the Weekly Readings."
  },
  follow_instructions_closely: {
    header: "Follow instructions closely",
    tags: ['AY2425S1', 'learning', 'tP', 'iP'],
    body: "Follow the instructions very closely."
  },
  note_down_deliverables: {
    header: "Note down deliverables",
    tags: ['AY2425S1', 'workload', 'schedule'],
    body: "If you are a type B, try to note down all the deliverables because it will quickly become overwhelming."
  },
  note_down_deliverables: {
    header: "Enjoy :-)",
    tags: ['AY2425S1', 'workload', 'grade'],
    body: "Just enjoy this mod and put as much effort as you have time for it/are willing to spend on it.<br> Most people seem to do well in this mod so don't stress."
  },
  pay_attention_to_grading_criteria: {
    header: "Pay attention to grading criteria",
    tags: ['AY2425S1', 'grade'],
    body: "Understand the requirements for the course' grades well, because if you put in effort but in the wrong aspect, you may not have reached your full potential for grades."
  },
  read_textbook_incrementally: {
    header: "Read textbook incrementally",
    tags: ['AY2425S1', 'grade', 'exam', 'learning', 'schedule'],
    body: "Read the textbook content bit by bit everyday before final exams. That way every knowledge can sink in."
  }
}%}

{% macro show_tip_card(tip) %}
  <card header="**{{ tip.header }}**" tag="{{ tip.tags  | join(', ') }}">
{{ tip.body }}
  </card>
{% endmacro %}


{% macro show_tips_list() %}
<cardstack searchable blocks="2">
  {% for tip_id, tip in tips %}
{{ show_tip_card(tip) }}
  {% endfor %}
</cardstack>
{% endmacro %}
