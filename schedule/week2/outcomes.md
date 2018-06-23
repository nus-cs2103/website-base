{% import "common/macros.njk" as macros with context %}

{% set outcome_groups = [
  {name: "SE Intro", outcomes: [
    {heading: "Can explain pros and cons of software engineering", priority: "4", units: [
      {location: ["softwareEngineering", "introduction", "prosAndCons"]}]
    }]
  },
  {name: "Implementation", outcomes: [
    {heading: "Can use basic features of an IDE", priority: "1", units: [
      {location: ["ides", "introduction", "what"]},
      {location: ["intellij", "projectSetup"]},
      {location: ["intellij", "codeNavigation"]}]
    },
    {heading: "Can use Java Collections", priority: "2", units: [
      {location: ["javaTools", "collections"]}]
    },
    {heading: "Can use Java varargs feature", priority: "3", units: [
      {location: ["javaTools", "varargs"]}]
    }]
  },
  {name: "Testing", outcomes: [
    {heading: "Can automate simple regression testing of text UIs", priority: "2", units: [
      {location: ["testing", "introduction", "what"]},
      {location: ["testing", "testingTypes", "regressionTesting", "what"]},
      {location: ["testing", "testAutomation", "what"], priority: "2", omit_evidence: true},
      {location: ["testing", "testAutomation", "testingTextUis"]}]
    }]
  },
  {name: "Revision Control", outcomes: [
    {heading: "Can use Git to save history", priority: "1", units: [
      {location: ["revisionControl", "what"]},
      {location: ["revisionControl", "repositories"]},
      {location: ["gitAndGithub", "init"]},
      {location: ["revisionControl", "savingHistory"]},
      {location: ["gitAndGithub", "commit"], priority: "1", omit_evidence: true},
      {location: ["gitAndGithub", "ignore"]}]
    }]
  }] 
%}

{{ macros.show_outcome_groups("2", outcome_groups) }}


