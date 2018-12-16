<frontmatter>
title: "Full Schedule of Module Activities"
footer: footer.md
head: scheduleHead.md
</frontmatter>

{% import "common/outcomes.njk" as outcomes with context %}

{% set weeks = [
    {num: "1", day:"Jan 14"},
    {num: "2", day:"Jan 21"},
    {num: "3", day:"Jan 28"},
    {num: "4", day:"Feb 4"},
    {num: "5", day: "Feb 11" },
    {num: "6", day: "Feb 18" },
    {num: "7", day: "Mar 4" },
    {num: "8", day: "Mar 11" },
    {num: "9", day: "Mar 18" },
    {num: "10", day: "Mar 25" },
    {num: "11", day: "Apr 1" },
    {num: "12", day: "Apr 8" },
    {num: "13", day: "Apr 12" }
] %}


{% set current_weeks = ["1", "2"] %}


{% set all_outcomes = [
{week: "2"},
  {name: "SE Intro"},
    {heading: "SE: Intro"},
      {location: ["softwareEngineering", "introduction", "prosAndCons"]},
  {name: "Implementation"},
    {heading: "IDEs: Basic Features"},
      {location: ["ides", "introduction", "what"]},
      {location: ["intellij", "projectSetup"]},
      {location: ["intellij", "codeNavigation"]},
    {heading: "Java: Collections"},
      {location: ["cppToJava", "collections", "what"]},
      {location: ["cppToJava", "collections", "arrayListClass"], omit_evidence: true},
      {location: ["cppToJava", "collections", "hashMapClass"], omit_evidence: true},
    {heading: "Java: varargs"},
      {location: ["javaTools", "varargs"]},
  {name: "Testing"},
    {heading: "Automated Testing of Text UIs"},
      {location: ["testing", "introduction", "what"]},
      {location: ["testing", "testingTypes", "regressionTesting", "what"]},
      {location: ["testing", "testAutomation", "what"], omit_evidence: true},
      {location: ["testing", "testAutomation", "testingTextUis"]},
  {name: "Revision Control"},
    {heading: "RCS: Revision History"},
      {location: ["revisionControl", "what"]},
      {location: ["revisionControl", "repositories"]},
      {location: ["gitAndGithub", "init"]},
      {location: ["revisionControl", "savingHistory"]},
      {location: ["gitAndGithub", "commit"], omit_evidence: true},
      {location: ["gitAndGithub", "ignore"]},
      {location: ["revisionControl", "usingHistory"], omit_evidence: true},
      {location: ["gitAndGithub", "checkout"]},
      {location: ["gitAndGithub", "tag"]},
      {location: ["gitAndGithub", "stash"]},
{week: "3"},
  {name: "Implementation"},
    {heading: "Refactoring: Basics"},
      {location: ["refactoring", "what"]},
      {location: ["intellij", "refactoring"]},
      {location: ["refactoring", "how"]},
      {location: ["refactoring", "when"]},
    {heading: "IDEs: Intermediate Features"},
      {location: ["ides", "debugging", "what"], omit_evidence: true},
      {location: ["intellij", "debuggingBasic"]},
      {location: ["intellij", "productivityShortcuts"]},
    {heading: "Coding Standards"},
      {location: ["codeQuality", "introduction", "basic"], omit_evidence: true},
      {location: ["codeQuality", "followStandard", "introduction"]},
      {location: ["codeQuality", "followStandard", "basic"]},
      {location: ["codeQuality", "followStandard", "intermediate"]},
  {name: "Revision Control"},
    {heading: "RCS: Remote Repos"},
      {location: ["revisionControl", "remoteRepositories"], omit_evidence: true},
      {location: ["gitAndGithub", "clone"]},
      {location: ["gitAndGithub", "pull"]},
      {location: ["gitAndGithub", "push"]},
  {name: "Documentation"},
    {heading: "Documentation Tools"},
      {subheading: "Javadoc"},
        {location: ["documentation", "tools", "javaDoc", "what"], omit_evidence: true},
        {location: ["documentation", "tools", "javaDoc", "how"], omit_evidence: true},
      {subheading: "Markdown"},
        {location: ["documentation", "tools", "markdown", "what"], omit_evidence: true},
        {location: ["documentation", "tools", "markdown", "how"], omit_evidence: true},
      {subheading: "AsciiDoc"},
        {location: ["documentation", "tools", "asciiDoc", "what"], omit_evidence: true},
{week: "4"},
  {name: "Project Management"},
    {heading: "RCS: Pull Requests"},
      {location: ["revisionControl", "branching"]},
      {location: ["gitAndGithub", "branch"]},
      {location: ["gitAndGithub", "createPRs"]},
  {name: "Requirements"},
    {heading: "Requirements: Intro"},
      {location: ["requirements", "introduction"], omit_evidence: true},
      {location: ["requirements", "nonFunctionalRequirements"], omit_evidence: true},
      {location: ["requirements", "prioritizing"], omit_evidence: true},
      {location: ["requirements", "quality"], omit_evidence: true},
    {heading: "Gathering Requirements"},
      {location: ["gatheringRequirements", "brainstorming"], omit_evidence: true},
      {location: ["gatheringRequirements", "productSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "observation"], omit_evidence: true},
      {location: ["gatheringRequirements", "userSurveys"], omit_evidence: true},
      {location: ["gatheringRequirements", "interviews"], omit_evidence: true},
      {location: ["gatheringRequirements", "focusGroups"], omit_evidence: true},
      {location: ["gatheringRequirements", "prototyping"], omit_evidence: true},
    {heading: "Specifying Requirements"},
      {subheading: "Prose"},
        {location: ["specifyingRequirements", "prose", "what"], omit_evidence: true},
      {subheading: "Feature Lists"},
        {location: ["specifyingRequirements", "featureList", "what"], omit_evidence: true},
      {subheading: "User Stories"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"], omit_evidence: true},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Use Cases"},
        {location: ["specifyingRequirements", "useCases", "introduction"], omit_evidence: true},
        {location: ["specifyingRequirements", "useCases", "identifying"], omit_evidence: true},
        {location: ["specifyingRequirements", "useCases", "details"]},
        {location: ["specifyingRequirements", "useCases", "usage"], omit_evidence: true},
      {subheading: "Glossary"},
        {location: ["specifyingRequirements", "glossary", "what"], omit_evidence: true},
      {subheading: "Supplementary Requirements"},
        {location: ["specifyingRequirements", "supplementaryRequirements", "what"], omit_evidence: true},
  {name: "OOP"},
    {heading: "OOP: Classes & Objects"},
      {location: ["oop", "introduction", "what"], omit_evidence: true},
      {location: ["oop", "objects", "what"], omit_evidence: true},
      {location: ["oop", "classes", "what"], omit_evidence: true},
      {location: ["oop", "objects", "abstraction"], omit_evidence: true},
      {location: ["oop", "objects", "encapsulation"], omit_evidence: true},
      {location: ["cppToJava", "classes", "definingClasses"]},
      {location: ["cppToJava", "classes", "gettersAndSetters"]},
      {location: ["oop", "classes", "classLevelMembers"], omit_evidence: true},
      {location: ["cppToJava", "classes", "classLevelMembers"], omit_evidence: true},
      {location: ["oop", "classes", "enumerations"]},
    {heading: "Java: enumerations"},
      {location: ["cppToJava", "misc", "enums"]},
    {heading: "OOP: Inheritance"},
      {location: ["oop", "inheritance", "what"], omit_evidence: true},
      {location: ["oop", "inheritance", "overloading"], omit_evidence: true},
      {location: ["oop", "inheritance", "overriding"], omit_evidence: true},
      {location: ["cppToJava", "inheritance", "basic"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Exception Handling"},
      {location: ["errorHandling", "introduction", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "what"], omit_evidence: true},
      {location: ["cppToJava", "exceptions", "what"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "how"]},
      {location: ["cppToJava", "exceptions", "how"], omit_evidence: true},
      {location: ["errorHandling", "exceptions", "when"], omit_evidence: true},
  {name: "Quality Assurance"},
    {heading: "Developer Testing: Basics"},
      {location: ["testing", "testingTypes", "developerTesting", "what"], omit_evidence: true},
      {location: ["testing", "testingTypes", "developerTesting", "why"]},
      {location: ["testing", "testAutomation", "usingTestDrivers"], omit_evidence: true},
      {location: ["testing", "testAutomation", "tools"], omit_evidence: true},
      {location: ["junit", "basic"]},
{week: "5"},
  {name: "Requirements"},
    {heading: "Can apply basic product design guidelines", priority: "3", file: "project.md#product_design"},
  {name: "Design"},
    {heading: "Design: Models"},
      {location: ["modeling", "introduction", "what"], omit_evidence: true},
      {location: ["modeling", "introduction", "how"]},
    {heading: "Class/Ojbect Diagrams: Basics"},
      {location: ["modeling", "modelingStructures", "ooStructures"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
      {location: ["modeling", "modelingStructures", "objectDiagrams"]},
      {location: ["uml", "miscellaneous", "objectVsClassDiagrams"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "OOP: Polymorphism"},
      {subheading: "Polymorphism"},
        {location: ["oop", "polymorphism", "what"], omit_evidence: true},
        {location: ["cppToJava", "inheritance", "polymorphism"], omit_evidence: true},
      {subheading: "Abstract Classes"},
        {location: ["oop", "inheritance", "abstractClasses"], omit_evidence: true},
        {location: ["cppToJava", "inheritance", "abstractClassesAndMethods"], omit_evidence: true},
      {subheading: "Interfaces"},
        {location: ["oop", "inheritance", "interfaces"], omit_evidence: true},
        {location: ["cppToJava", "inheritance", "interfaces"], omit_evidence: true},
  {name: "Project Management"},
    {heading: "RCS: Workflows"},
      {location: ["gitAndGithub", "mergeConflicts"]},
      {location: ["gitAndGithub", "managePRs"]},
      {location: ["revisionControl", "forkingWorkflow"], omit_evidence: true},
      {location: ["gitAndGithub", "forkingWorkflow"]},
      {location: ["revisionControl", "drcsVsCrcs"], omit_evidence: true},
      {location: ["revisionControl", "featureBranchFlow"], omit_evidence: true},
      {location: ["revisionControl", "centralizedFlow"], omit_evidence: true},
{week: "6"},
  {name: "Design"},
    {heading: "Class Diagrams: Intermediate-Level"},
      {location: ["uml", "notes", "notes"], omit_evidence: true},
      {location: ["uml", "notes", "constraints"], omit_evidence: true},
      {location: ["uml", "classDiagrams", "associationsAsAttributes", "what"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "classDiagramsIntermediate"], omit_evidence: true},
    {heading: "Sequence Diagrams: Basics"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsBasic"]},
    {heading: "Architecture Diagrams"},
      {location: ["design", "introduction", "what"], omit_evidence: true},
      {location: ["architecture", "architectureDiagrams", "reading"], omit_evidence: true},
      {location: ["designApproaches", "multilevelDesign", "what"]},
  {name: "Implementation"},
    {heading: "Logging"},
      {location: ["errorHandling", "logging", "what"], omit_evidence: true},
      {location: ["errorHandling", "logging", "how"]},
    {heading: "Assertions"},
      {location: ["errorHandling", "assertions", "what"], omit_evidence: true},
      {location: ["errorHandling", "assertions", "how"]},
      {location: ["errorHandling", "assertions", "when"]},
    {heading: "Java: streams"},
      {location: ["javaTools", "streamsBasic"]},
    {heading: "Java: JavaFX"},
      {location: ["javaTools", "javaFXBasic"]},
  {name: "Project Management"},
    {heading: "Continuous Integration/Deployment"},
      {location: ["integration", "introduction", "what"], omit_evidence: true},
      {location: ["integration", "buildAutomation", "what"]},
      {location: ["integration", "buildAutomation", "continuousIntegrationDeployment"]},
{week: "7"},
  {name: "Design"},
    {heading: "Architectural Styles"},
      {location: ["architecture", "architecturalStyles", "introduction", "what"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "nTier", "what"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "clientServer", "what"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "eventDriven", "what"]},
      {location: ["architecture", "architecturalStyles", "transactionProcessing", "what"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "serviceOriented", "what"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "more", "moreStyles"], omit_evidence: true},
      {location: ["architecture", "architecturalStyles", "more", "usingStyles"]},
    {heading: "APIs"},
      {location: ["reuse", "apis", "what"]},
    {heading: "Sequence Diagrams: Intermediate-Level"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsIntermediate"]},
      {location: ["uml", "sequenceDiagrams", "referenceFrames"], omit_evidence: true},
      {location: ["uml", "sequenceDiagrams", "parallelPaths"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "CodeQuality: Readability"},
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
      {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"], omit_evidence: true},
    {heading: "CodeQuality: Naming"},
      {location: ["codeQuality", "nameWell", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "basic", "useStandardWords"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"], omit_evidence: true},
      {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"], omit_evidence: true},
    {heading: "CodeQuality: Unsafe Practices"},
      {location: ["codeQuality", "avoidShortcuts", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "useDefaultBranch"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "dontRecycleVarsOrParams"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "avoidEmptyCatchBlocks"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "basic", "deleteDeadCode"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseVariableScope"], omit_evidence: true},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseCodeDuplication"], omit_evidence: true},
    {heading: "CodeQuality: Code Comments"},
      {location: ["codeQuality", "commentMinimally", "introduction"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"], omit_evidence: true},
      {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"], omit_evidence: true},
{week: "8"},
  {name: "Design"},
    {heading: "Design Principles: Basics"},
      {subheading: "Abstraction"},
        {location: ["designFundamentals", "abstraction", "what"], omit_evidence: true},
      {subheading: "Coupling"},
        {location: ["designFundamentals", "coupling", "what"]},
        {location: ["designFundamentals", "coupling", "how"]},
        {location: ["designFundamentals", "coupling", "types"]},
      {subheading: "Cohesion"},
        {location: ["designFundamentals", "cohesion", "what"]},
        {location: ["designFundamentals", "cohesion", "how"]},
      {subheading: "Some other principles"},
        {location: ["principles", "singleResponsibilityPrinciple"]},
        {location: ["principles", "openClosedPrinciple"]},
        {location: ["principles", "separationOfConcernsPrinciple"]},
  {name: "Implementation"},
    {heading: "Integration Approaches"},
      {location: ["integration", "approaches", "lateVsEarly"], omit_evidence: true},
      {location: ["integration", "approaches", "bigBangVsIncremental"], omit_evidence: true},
      {location: ["integration", "approaches", "topDownVsBottomUp"], omit_evidence: true},
    {heading: "Association Classes"},
      {location: ["oop", "associations", "associationClasses"]},
  {name: "Quality Assurance"},
    {heading: "Types of Testing"},
      {subheading: "Unit Testing"},
        {location: ["testing", "testingTypes", "unitTesting", "what"]},
        {location: ["testing", "testingTypes", "unitTesting", "stubs"]},
        {location: ["testing", "dependencyInjection", "what"], omit_evidence: true},
        {location: ["testing", "dependencyInjection", "how"], omit_evidence: true},
      {subheading: "Integration Testing"},
        {location: ["testing", "testingTypes", "integrationTesting", "what"]},
        {location: ["testing", "testingTypes", "integrationTesting", "how"]},
      {subheading: "System Testing"},
        {location: ["testing", "testingTypes", "systemTesting", "what"]},
        {location: ["testing", "testAutomation", "testingGuis"]},
      {subheading: "Acceptance Testing"},
        {location: ["testing", "testingTypes", "acceptanceTesting", "what"]},
        {location: ["testing", "testingTypes", "acceptanceTesting", "acceptanceVsSystemTesting"]},
      {subheading: "Alpha/Beta Testing"},
        {location: ["testing", "testingTypes", "alphaBetaTesting", "what"]},
    {heading: "Testing: Intermediate Techniques"},
      {location: ["testing", "introduction", "testability"], omit_evidence: true},
      {location: ["testing", "testCoverage", "what"]},
      {location: ["testing", "testCoverage", "how"]},
      {location: ["junit", "intermediate"]},
      {location: ["testing", "tdd", "what"], omit_evidence: true},
  {name: "Project Management"},
    {heading: "Project Mgt: Scheduling and Tracking"},
      {location: ["projectPlanning", "milestones"]},
      {location: ["projectPlanning", "buffers"]},
      {location: ["projectPlanning", "issueTrackers"]},
      {location: ["projectPlanning", "workBreakdownStructure"]},
      {location: ["projectPlanning", "ganttCharts"], omit_evidence: true},
      {location: ["projectPlanning", "pertCharts"], omit_evidence: true},
      {location: ["teamwork", "teamStructures"]},
{week: "9"},
  {name: "Design"},
    {heading: "Conceptualize OO Solution"},
      {location: ["modeling", "modelingASolution", "introduction"], omit_evidence: true},
      {location: ["modeling", "modelingASolution", "basic"]},
      {location: ["modeling", "modelingASolution", "intermediate"]},
    {heading: "Basic Design Approaches"},
      {location: ["designApproaches", "topDownBottomUp", "what"], omit_evidence: true},
      {location: ["designApproaches", "agileDesign", "what"], omit_evidence: true},
    {heading: "Design Principles: Intermediate-Level"},
      {subheading: "How Polymorphism Works"},
        {location: ["oop", "inheritance", "substitutability"], omit_evidence: true},
        {location: ["oop", "inheritance", "dynamicAndStaticBinding"], omit_evidence: true},
        {location: ["oop", "polymorphism", "how"]},
      {subheading: "More Design Principles"},
        {location: ["principles", "liskovSubstitutionPrinciple"]},
        {location: ["principles", "lawOfDemeter"]},
        {location: ["principles", "interfaceSegregationPrinciple"], omit_evidence: true},
        {location: ["principles", "dependencyInversionPrinciple"], omit_evidence: true},
        {location: ["principles", "solidPrinciples"], omit_evidence: true},
        {location: ["principles", "yagniPrinciple"], omit_evidence: true},
        {location: ["principles", "dryPrinciple"], omit_evidence: true},
        {location: ["principles", "brooksLaw"], omit_evidence: true},
    {heading: "Activity Diagrams"},
        {location: ["modeling", "modelingBehaviors", "activityDiagrams"]},
        {location: ["modeling", "modelingBehaviors", "activityDiagramsIntermediate"], omit_evidence: true},
  {name: "Implementation"},
    {heading: "Defensive Programming"},
      {location: ["errorHandling", "defensiveProgramming", "what"], omit_evidence: true},
      {location: ["errorHandling", "defensiveProgramming", "compulsoryAssociations"], omit_evidence: true},
      {location: ["errorHandling", "defensiveProgramming", "1to1Associations"], omit_evidence: true},
      {location: ["errorHandling", "defensiveProgramming", "referentialIntegrity"], omit_evidence: true},
      {location: ["errorHandling", "defensiveProgramming", "when"], omit_evidence: true},
      {location: ["errorHandling", "designByContract", "what"], omit_evidence: true},
  {name: "Quality Assurance"},
    {heading: "Other QA Techniques"},
      {location: ["qualityAssurance", "introduction", "what"], omit_evidence: true},
      {location: ["qualityAssurance", "introduction", "validationVsVerification"]},
      {location: ["qualityAssurance", "codeReviews", "what"]},
      {location: ["qualityAssurance", "staticAnalysis", "what"]},
      {location: ["qualityAssurance", "formalVerification", "what"], omit_evidence: true},
  {name: "Documentation"},
    {heading: "Writing Developer Documents"},
      {subheading: "Type of Developer Docs"},
        {location: ["documentation", "introduction", "what"]},
      {subheading: "Guideline: Aim for Comprehensibility"},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "how"]},
      {subheading: "Guideline: Describe Top-Down"},
        {location: ["documentation", "guidelines", "goTopDown", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "goTopDown", "why"]},
        {location: ["documentation", "guidelines", "goTopDown", "how"]},
      {subheading: "Guideline: Minimal but Sufficient"},
        {location: ["documentation", "guidelines", "documentMinimally", "what"], omit_evidence: true},
        {location: ["documentation", "guidelines", "documentMinimally", "how"], omit_evidence: true},
      {subheading: "Drawing Architecture Diagrams"},
        {location: ["architecture", "architectureDiagrams", "drawing"], omit_evidence: true},
{week: "10"},
  {name: "Requirements"},
    {heading: "OO Domain Models"},
      {location: ["modeling", "modelingStructures", "objectOrientedDomainModels"], omit_evidence: true},
  {name: "Design"},
    {heading: "Design Patterns: Basics"},
      {subheading: "Introduction"},
        {location: ["designPatterns", "introduction", "what"], omit_evidence: true},
        {location: ["designPatterns", "introduction", "format"], omit_evidence: true},
      {subheading: "Singleton pattern"},
        {location: ["designPatterns", "singleton", "what"]},
        {location: ["designPatterns", "singleton", "implementation"]},
        {location: ["designPatterns", "singleton", "evaluation"]},
      {subheading: "Facade pattern"},
        {location: ["designPatterns", "facade", "what"]},
      {subheading: "Command pattern"},
        {location: ["designPatterns", "command", "what"]},
      {subheading: "Abstraction Occurrence pattern"},
        {location: ["designPatterns", "abstractionOccurrence", "what"]},
  {name: "Quality Assurance"},
    {heading: "Test Case Design"},
      {location: ["testCaseDesign", "introduction", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "what"]},
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "when"], omit_evidence: true},
      {location: ["testCaseDesign", "introduction", "positiveVsNegative"]},
      {location: ["testCaseDesign", "introduction", "blackVsGlass"]},
      {location: ["testCaseDesign", "more", "testingUseCases"]},
    {heading: "Equivalence Partitioning"},
      {location: ["testCaseDesign", "equivalencePartitions", "what"], omit_evidence: true},
      {location: ["testCaseDesign", "equivalencePartitions", "basic"], omit_evidence: true},
      {location: ["testCaseDesign", "equivalencePartitions", "intermediate"]},
    {heading: "Boundary Value Analysis"},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "what"], omit_evidence: true},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "how"], omit_evidence: true},
{week: "11"},
  {name: "Design"},
    {heading: "Design Patterns: Intermediate-Level"},
      {location: ["designPatterns", "modelViewController", "what"]},
      {location: ["designPatterns", "observer", "what"]},
      {location: ["designPatterns", "more", "otherDesignPatterns"]},
      {location: ["designPatterns", "more", "combiningDesignPatterns"]},
      {location: ["designPatterns", "more", "usingDesignPatterns"]},
      {location: ["designPatterns", "more", "vsPrinciples"], omit_evidence: true},
      {location: ["designPatterns", "more", "otherTypesOfPatterns"]},
    {heading: "Other UML Models"},
      {location: ["modeling", "modelingStructures", "deploymentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "componentDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "packageDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingStructures", "compositeStructureDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "timingDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "interactionOverviewDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "communicationDiagrams"], omit_evidence: true},
      {location: ["modeling", "modelingBehaviors", "stateMachineDiagrams"], omit_evidence: true},
  {name: "Quality Assurance"},
    {heading: "Combining Multiple Test Inputs"},
      {location: ["testCaseDesign", "combiningTestInputs", "why"], omit_evidence: true},
      {location: ["testCaseDesign", "combiningTestInputs", "combinationStrategies"], omit_evidence: true},
      {location: ["testCaseDesign", "combiningTestInputs", "heuristicValid"], omit_evidence: true},
      {location: ["testCaseDesign", "combiningTestInputs", "heuristicInvalid"], omit_evidence: true},
      {location: ["testCaseDesign", "combiningTestInputs", "mix"]},
  {name: "Project Management"},
    {heading: "SDLC Process Models"},
      {location: ["processModels", "introduction", "what"], omit_evidence: true},
      {location: ["processModels", "introduction", "sequentialModels"]},
      {location: ["processModels", "introduction", "iterativeModels"]},
      {location: ["processModels", "introduction", "agileModels"]},
      {location: ["processModels", "exampleProcessModels", "scrum"], evidence: "project.md#relate_process"},
      {location: ["processModels", "exampleProcessModels", "xp"], evidence: "project.md#relate_process"},
      {location: ["processModels", "exampleProcessModels", "unifiedProcess"], evidence: "project.md#relate_process"},
      {location: ["processModels", "more", "cmmi"], omit_evidence: true},
      {location: ["processModels", "summary", "recap"], omit_evidence: true},
{week: "12"},
  {name: "Implementation"},
    {heading: "Reuse: Frameworks, Libraries, Platforms"},
      {subheading: "Reuse"},
        {location: ["reuse", "introduction", "what"], omit_evidence: true},
        {location: ["reuse", "introduction", "when"]},
      {subheading: "Libraries"},
        {location: ["reuse", "libraries", "what"]},
        {location: ["reuse", "libraries", "how"]},
      {subheading: "Frameworks"},
        {location: ["reuse", "frameworks", "what"]},
        {location: ["reuse", "frameworks", "frameworksVsLibraries"]},
      {subheading: "Platforms"},
        {location: ["reuse", "platforms", "what"]},
    {heading: "Cloud Computing"},
      {location: ["reuse", "cloudComputing", "what"], omit_evidence: true},
      {location: ["reuse", "cloudComputing", "services"], omit_evidence: true},
{week: "13"}
]%}


{% macro show_week_outcomes(week_num, path="") %}
<panel type="seamless" popup-url="{{baseUrl}}/schedule/week{{ week_num }}/outcomes.html" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_outcome }} Outcomes</span>
  <div class="indented">
  {{ outcomes.show_week_schedule_main(week_num, all_outcomes, path) }}
  </div>
</panel>
{% endmacro %}


{% macro show_week_todos(week_num, path="") %}
<panel type="seamless" expanded no-close>
  <span slot="header" class="card-title activity-type">{{ icon_todo }} Todo</span>
  <div class="indented">
  <include src="{{ path }}todo.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_tutorial(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_tutorial }} Tutorial {{ week_num }}</span>
   <div class="indented">
   <include src="{{ path }}tutorial.md" />
   </div>
</panel>
{% endmacro %}


{% macro show_week_lecture(week_num, path="") %}
<panel type="seamless" expanded no-close>
<span slot="header" class="card-title activity-type">{{ icon_lecture }} Lecture {{ week_num }}</span>
  <div class="indented">
  <include src="{{ path }}lecture.md" />
  </div>
</panel>
{% endmacro %}


{% macro show_week_schedule(week_num_string, path="") %}

{% set week_num_int = week_num_string | int %}
{% set week = weeks[week_num_int - 1] %}

<include src="../../common/header.md" />

<div class="website-content" id="main">

{{ show_nav_buttons(week.num) }}

{{ show_week_schedule_body(week, path) }}

</div>

{% endmacro %}


{% macro show_nav_buttons(week_num) %}
{% set week_num = week_num | int %}
{% if week_num != 1 %}<span style="float:left"><md>[{{ glyphicon_chevron_left }} Previous Week]({{ baseUrl }}/schedule/week{{ (week_num - 1) }}/)</md></span>{% endif %}{% if week_num != 13 %}<span style="float:right"><md>[Next Week {{ glyphicon_chevron_right }}]({{ baseUrl }}/schedule/week{{ (week_num + 1) }}/)</md></span>{% endif %}<br>

{% endmacro %}


{% macro show_week_schedule_body(week, path="") %}

# Week {{ week.num }} <small><small>%%[{{ week.day }}]%%</small></small>

<tabs>
  <tab header="{{ icon_announcement }} Notices">
    <include src="{{ path }}notices-{{ module | lower }}.md" optional />
  </tab>
  <tab header="{{ icon_outcome }} Topics">
    <include src="{{ path }}outcomes.md" />
  </tab>
  <tab header="{{ icon_project }} Project">
    <include src="{{ path }}project.md" optional />
  </tab>
  <tab header="{{ icon_tutorial }} Tutorial">
    <include src="{{ path }}tutorial.md" />
  </tab>
  <tab header="{{ icon_info }} Admin Info">
    <include src="{{ path }}todo.md" />
  </tab>
</tabs>

{% endmacro %}




<!-- ============================= page content ============================================ -->

<include src="../common/header.md" />

<div class="website-content" id="main">

{{ show_nav_buttons(current_weeks[0]) }}

{% for week in weeks %}
{% set week_num = week.num | int %}
{% if week.num in current_weeks %}
  {{ show_week_schedule_body(week, "week" + week_num + "/") }}
<br>
<br>
{% endif %}
{% endfor %}

</div>