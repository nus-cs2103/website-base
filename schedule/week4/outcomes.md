{% import "common/macros.md" as macros with context %}

{% set outcome_groups = [
  {
    name: "Design", 
    outcomes: 
      [
        {id: "W4.1", heading: "Can explain models", priority: "3", file: "outcome-model.md"},
        {id: "W4.2", heading: "Can explain OOP", priority: "1", file: "outcome-oop.md"},
        {id: "W4.3", heading: "Can explain basic object/class structures", priority: "1", file: "outcome-classStructure.md"}
      ]
  },
  {
    name: "Implementation", 
    outcomes: 
      [
        {id: "W4.4", heading: "Can implement classes", priority: "1", file: "outcome-implementClassStructures.md"},
        {id: "W4.5", heading: "Can do exception handling in code", priority: "2", file: "outcome-exceptionHandling.md"},
        {id: "W4.6", heading: "Can use Java enumerations", priority: "3", file: "outcome-enumeration.md"}
      ]
  },
  {
    name: "Project Management", 
    outcomes: 
      [
        {id: "W4.7", heading: "Can create PRs on GitHub", priority: "1", file: "outcome-pr.md"}
      ]
  }
  ] %}

{{ macros.show_outcome_groups("4", outcome_groups) }}
