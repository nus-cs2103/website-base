{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(2, "tutorial") }}

{% import "common/macros.njk" as macros with context %}

<big>**Tutorial selection and seating arrangement**</big>

* **{{ module }}** students: As you don't have a confirmed tutorial yet, attend the slot you chose in the 'Temporary Tutorial Registration' Doodle poll (to be done early in Mon-Tue of week 2). Team forming will be done in the following week. You are free to sit with anyone this week.
* **{{ module }}T** students:
  * Those in Wednesday tutorials: As Wednesday is a holiday, follow instructions for {{ module }} students given above to choose another slot for this week. You can attend your normal tutorial from week 3. Sit with your team members for Tutorial 3 onwards.
  * Those in Thursday and Friday tutorials: Attend the tutorial pre-allocated to you. Sit together with your team members.


<br/>

<big>****Show evidence of learning the topics assigned for the week****</big>

* Starting with topics at {{ macros.show_stars("1") }} level, share/discuss/demo evidence of (as directed by the tutor) weekly topics.

* Suggested minimal achievements for the tutorial:
  * Set up AddressBook-level1 in Intellij
  * Use the IDE to navigate code efficiently
  * Use use file I/O method to automate regression testing
  * Set up a local repo and do some commits