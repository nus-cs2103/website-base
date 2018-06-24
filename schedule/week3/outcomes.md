{% import "common/macros.njk" as macros with context %}

{% set outcome_groups = [
  {name: "Refactoring", 
    outcomes: [
      {heading: "Can refactor code at a basic level", priority: "2", units: [
        {location: ["refactoring", "what"]},
        {location: ["intellij", "refactoring"]},
        {location: ["refactoring", "how"]},
        {location: ["refactoring", "when"]}]
      }]
  },
  {name: "Code Quality", 
    outcomes: [
      {heading: "Can follow a simple style guide", priority: "2", units: [
        {location: ["codeQuality", "introduction", "basic"], omit_evidence: true},
        {location: ["codeQuality", "followStandard", "introduction"]},
        {location: ["codeQuality", "followStandard", "basic"]},
        {location: ["codeQuality", "followStandard", "intermediate"]}]
      },
      {heading: "Can improve code readability", priority: "2", units: [
        {location: ["codeQuality", "maximiseReadability", "introduction"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "basic", "avoidLongMethods"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "basic", "avoidDeepNesting"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "basic", "avoidComplicatedExpressions"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "basic", "avoidMagicNumbers"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "basic", "makeCodeObvious"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "intermediate", "structureCodeLogically"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "intermediate", "dontTripReader"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "intermediate", "practiceKISSing"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "intermediate", "avoidPrematureOptimizations"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "intermediate", "slapHard"], omit_evidence: true},
        {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"], omit_evidence: true}]
      },
      {heading: "Can use good naming", priority: "2", units: [
        {location: ["codeQuality", "nameWell", "introduction"], omit_evidence: true},
        {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"], omit_evidence: true},
        {location: ["codeQuality", "nameWell", "basic", "useStandardWords"], omit_evidence: true},
        {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"], omit_evidence: true},
        {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"], omit_evidence: true},
        {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"], omit_evidence: true}]
      },
      {heading: "Can avoid unsafe coding practices", priority: "2", units: [
        {location: ["codeQuality", "avoidShortcuts", "introduction"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "basic", "useDefaultBranch"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "basic", "dontRecycleVarsOrParams"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "basic", "avoidEmptyCatchBlocks"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "basic", "deleteDeadCode"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseVariableScope"], omit_evidence: true},
        {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseCodeDuplication"], omit_evidence: true}]
      },
      {heading: "Can write good code comments", priority: "3", units: [
        {location: ["codeQuality", "commentMinimally", "introduction"], omit_evidence: true},
        {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"], omit_evidence: true},
        {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"], omit_evidence: true},
        {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"], omit_evidence: true}]
      }]
  },
  {name: "IDEs", 
    outcomes: [
      {heading: "Can use intermediate level features of an IDE", priority: "3", units: [
        {location: ["ides", "debugging", "what"], omit_evidence: true},
        {location: ["intellij", "debuggingBasic"]},
        {location: ["intellij", "productivityShortcuts"]}]
      }]
  },
  {name: "Revision Control", 
    outcomes: [
      {heading: "Can communicate with a remote repo", priority: "1", units: [
        {location: ["revisionControl", "remoteRepositories"], omit_evidence: true},
        {location: ["gitAndGithub", "clone"]},
        {location: ["gitAndGithub", "pull"]},
        {location: ["gitAndGithub", "push"]}]
      },
      {heading: "Can traverse Git history", priority: "3", units: [
        {location: ["revisionControl", "usingHistory"], omit_evidence: true},
        {location: ["gitAndGithub", "checkout"]},
        {location: ["gitAndGithub", "tag"]},
        {location: ["gitAndGithub", "stash"]}]
      }]
  },
  {name: "Other", 
    outcomes: [
      {heading: "Can work with a 1KLoC code base ==[Compulsory]==", priority: "1", file: "outcome-1kloc.md"}]
  }] 
%}

{{ macros.show_outcome_groups("3", outcome_groups) }}

