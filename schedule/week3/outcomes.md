{% import "common/macros.md" as macros with context %}

{% set outcome_groups = [
  {
    name: "Refactoring", 
    outcomes: 
      [
        {heading: "Can refactor code at a basic level", priority: "2", file: "outcome-refactor.md"}
      ]
  },
  {
    name: "Code Quality", 
    outcomes: 
      [
        {heading: "Can follow a simple style guide", priority: "2", file: "outcome-ide.md"},
        {heading: "Can improve code readability", priority: "2", file: "outcome-readability.md"},
        {heading: "Can use good naming", priority: "2", file: "outcome-naming.md"},
        {heading: "Can avoid unsafe coding practices", priority: "2", file: "outcome-codingPractice.md"},
        {heading: "Can write good code comments", priority: "3", file: "outcome-comment.md"}
      ]
  },
  {
    name: "IDEs", 
    outcomes: 
      [
        {heading: "Can use intermediate level features of an IDE", priority: "3", file: "outcome-ide.md"}
      ]
  },
  {
    name: "Revision Control", 
    outcomes: 
      [
        {heading: "Can communicate with a remote repo", priority: "1", file: "outcome-remoteRepo.md"},
        {heading: "Can traverse Git history", priority: "3", file: "outcome-gitHistory.md"}
      ]
  },
  {
    name: "Other", 
    outcomes: 
      [
        {id: "W3.10", heading: "Can work with a 1KLoC code base ==[Compulsory]==", priority: "1", file: "outcome-1kloc.md"}
      ]
  }
  ] %}

{{ macros.show_outcome_groups("3", outcome_groups) }}

