{% import "common/macros.md" as macros with context %}

{% set outcome_groups = [
  {name: "SE Intro", outcomes: [
    {heading: "Can explain pros and cons of software engineering", priority: "4", file: "outcome-se.md"}]
  },
  {name: "Implementation", outcomes: [
     {heading: "Can use basic features of an IDE", priority: "1", file: "outcome-ide.md"},
     {heading: "Can use Java Collections", priority: "2", file: "outcome-collections.md"},
     {heading: "Can use Java varargs feature", priority: "3", file: "outcome-varargs.md"}]
  },
  {name: "Testing", outcomes: [
      {heading: "Can automate simple regression testing of text UIs", priority: "2", file: "outcome-testing.md"}]
  },
  {name: "Revision Control", outcomes: [
     {heading: "Can use Git to save history", priority: "1", file: "outcome-git.md", units: [
       {location: ["revisionControl", "what"], priority: "1"},
       {location: ["revisionControl", "repositories"], priority: "1"},
       {location: ["gitAndGithub", "init"], priority: "1"},
       {location: ["revisionControl", "savingHistory"], priority: "1"},
       {location: ["gitAndGithub", "commit"], priority: "1", omit_evidence: true},
       {location: ["gitAndGithub", "ignore"], priority: "2"}]
     }]
  }] 
%}

{{ macros.show_outcome_groups("2", outcome_groups) }}


