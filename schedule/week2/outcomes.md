{% import "common/macros.md" as macros with context %}

{% set outcome_groups = [
  {
    name: "SE Intro", 
    outcomes: 
      [
        {heading: "Can explain pros and cons of software engineering", priority: "4", file: "outcome-se.md"}
      ]
  },
  {
    name: "Implementation", 
    outcomes: 
      [
        {heading: "Can use basic features of an IDE", priority: "1", file: "outcome-ide.md"},
        {heading: "Can use Java Collections", priority: "2", file: "outcome-collections.md"},
        {heading: "Can use Java varargs feature", priority: "3", file: "outcome-varargs.md"}
      ]
  },
  {
    name: "Testing", 
    outcomes: 
    [
      {heading: "Can automate simple regression testing of text UIs", priority: "2", file: "outcome-testing.md"}
    ]
   },
  {
    name: "Revision Control", 
    outcomes: 
    [
      {heading: "Can use Git to save history", priority: "1", file: "outcome-git.md"}
    ]
   }
  ] %}

{{ macros.show_outcome_groups("2", outcome_groups) }}


