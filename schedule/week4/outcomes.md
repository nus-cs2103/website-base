{% import "common/macros.njk" as macros with context %}

{% set outcome_groups = [
  {
    name: "Design", 
    outcomes: [
      {heading: "Can explain models", priority: "3", units: [ 
        {location: ["modeling", "introduction", "what"], omit_evidence: true},
        {location: ["modeling", "introduction", "how"]}]
      },
      {heading: "Can explain OOP", priority: "1", units: [ 
        {location: ["oopDesign", "introduction", "what"], omit_evidence: true},
        {location: ["oopDesign", "objects", "basic"]},
        {location: ["oopDesign", "classes", "basic"]},
        {location: ["oopDesign", "objects", "abstraction"], omit_evidence: true},
        {location: ["oopDesign", "objects", "encapsulation"], omit_evidence: true}]
      },
      {heading: "Can explain basic object/class structures", priority: "1", units: [ 
        {location: ["modeling", "modelingStructures", "ooStructures"], omit_evidence: true},
        {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
        {location: ["uml", "miscellaneous", "objectVsClassDiagrams"], omit_evidence: true}]
      }]
  },
  {
    name: "Implementation", 
    outcomes: [
      {heading: "Can implement classes", priority: "1",  units: [ 
        {location: ["oopImplementation", "classes"]},
        {location: ["oopImplementation", "associations"]}]
      },
      {heading: "Can do exception handling in code", priority: "2", units: [ 
        {location: ["errorHandling", "introduction", "what"], omit_evidence: true},
        {location: ["errorHandling", "exceptions", "what"], omit_evidence: true},
        {location: ["errorHandling", "exceptions", "how"]},
        {location: ["errorHandling", "exceptions", "when"], omit_evidence: true}]
      },
      {heading: "Can use Java enumerations", priority: "3", units: [ 
        {location: ["oopDesign", "classes", "enumerations"]},
        {location: ["javaTools", "enums"]}]
      }]
  },
  {
    name: "Project Management", 
    outcomes: [
        {heading: "Can create PRs on GitHub", priority: "1", units: [ 
        {location: ["revisionControl", "branching"]},
        {location: ["gitAndGithub", "branch"]},
        {location: ["gitAndGithub", "createPRs"]},
        {location: ["gitAndGithub", "mergeConflicts"]},
        {location: ["gitAndGithub", "managePRs"]}]
      }]
  }] 
%}

{{ macros.show_outcome_groups("4", outcome_groups) }}
