{% import "common/macros.md" as macros with context %}

<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<div class="website-content">

## Week 2 - Outcomes 

<div id="main">

{% set outcome_groups = [
  {
    name: "SE Intro", 
    outcomes: 
      [
        {id: "W2.1", heading: "Can explain pros and cons of software engineering", priority: "4", file: "outcome-se.md"}
      ]
  },
  {
    name: "Implementation", 
    outcomes: 
      [
        {id: "W2.2", heading: "Can use basic features of an IDE", priority: "1", file: "outcome-ide.md"},
        {id: "W2.3", heading: "Can use Java Collections", priority: "2", file: "outcome-collections.md"},
        {id: "W2.4", heading: "Can use Java varargs feature", priority: "3", file: "outcome-varargs.md"}
      ]
  },
  {
    name: "Quality Assurance", 
    outcomes: 
    [
      {id: "W2.5", heading: "Can automate simple regression testing of text UIs", priority: "2", file: "outcome-testing.md"}
    ]
   },
  {
    name: "Project Management", 
    outcomes: 
    [
      {id: "W2.6", heading: "Can use Git to save history", priority: "1", file: "outcome-git.md"}
    ]
   }
  ] %}

{{ macros.show_outcome_groups(outcome_groups) }}

</div>
</div>
