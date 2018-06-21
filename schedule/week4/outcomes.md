{% import "common/macros.md" as macros with context %}

{% set outcome_groups = [
  {
    name: "Design", 
    outcomes: 
      [
        {heading: "Can explain models", priority: "3", file: "outcome-model.md"},
        {heading: "Can explain OOP", priority: "1", file: "outcome-oop.md"},
        {heading: "Can explain basic object/class structures", priority: "1", file: "outcome-classStructure.md"}
      ]
  },
  {
    name: "Implementation", 
    outcomes: 
      [
        {heading: "Can implement classes", priority: "1", file: "outcome-implementClassStructures.md"},
        {heading: "Can do exception handling in code", priority: "2", file: "outcome-exceptionHandling.md"},
        {heading: "Can use Java enumerations", priority: "3", file: "outcome-enumeration.md"}
      ]
  },
  {
    name: "Project Management", 
    outcomes: 
      [
        {heading: "Can create PRs on GitHub", priority: "1", file: "outcome-pr.md"}
      ]
  }
  ] %}

{{ macros.show_outcome_groups("4", outcome_groups) }}
