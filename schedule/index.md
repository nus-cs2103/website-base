<frontmatter>
title: "Full Schedule of Module Activities"
header: header.md
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
      {location: ["cppToJava", "collections", "arrayListClass"]},
      {location: ["cppToJava", "collections", "hashMapClass"]},
    {heading: "Java: varargs"},
      {location: ["javaTools", "varargs"]},
  {name: "Testing"},
    {heading: "Automated Testing of Text UIs"},
      {location: ["testing", "introduction", "what"]},
      {location: ["testing", "testingTypes", "regressionTesting", "what"]},
      {location: ["testing", "testAutomation", "what"]},
      {location: ["testing", "testAutomation", "testingTextUis"]},
  {name: "Revision Control"},
    {heading: "RCS: Revision History"},
      {location: ["revisionControl", "what"]},
      {location: ["revisionControl", "repositories"]},
      {location: ["gitAndGithub", "init"]},
      {location: ["revisionControl", "savingHistory"]},
      {location: ["gitAndGithub", "commit"]},
      {location: ["gitAndGithub", "ignore"]},
      {location: ["revisionControl", "usingHistory"]},
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
      {location: ["ides", "debugging", "what"]},
      {location: ["intellij", "debuggingBasic"]},
      {location: ["intellij", "productivityShortcuts"]},
    {heading: "Coding Standards"},
      {location: ["codeQuality", "introduction", "basic"]},
      {location: ["codeQuality", "followStandard", "introduction"]},
      {location: ["codeQuality", "followStandard", "basic"]},
      {location: ["codeQuality", "followStandard", "intermediate"]},
  {name: "Revision Control"},
    {heading: "RCS: Remote Repos"},
      {location: ["revisionControl", "remoteRepositories"]},
      {location: ["gitAndGithub", "clone"]},
      {location: ["gitAndGithub", "pull"]},
      {location: ["gitAndGithub", "push"]},
  {name: "Documentation"},
    {heading: "Documentation Tools"},
      {subheading: "Javadoc"},
        {location: ["documentation", "tools", "javaDoc", "what"]},
        {location: ["documentation", "tools", "javaDoc", "how"]},
      {subheading: "Markdown"},
        {location: ["documentation", "tools", "markdown", "what"]},
        {location: ["documentation", "tools", "markdown", "how"]},
      {subheading: "AsciiDoc"},
        {location: ["documentation", "tools", "asciiDoc", "what"]},
{week: "4"},
  {name: "Project Management"},
    {heading: "RCS: Pull Requests"},
      {location: ["revisionControl", "branching"]},
      {location: ["gitAndGithub", "branch"]},
      {location: ["gitAndGithub", "createPRs"]},
  {name: "Requirements"},
    {heading: "Requirements: Intro"},
      {location: ["requirements", "introduction"]},
      {location: ["requirements", "nonFunctionalRequirements"]},
      {location: ["requirements", "prioritizing"]},
      {location: ["requirements", "quality"]},
    {heading: "Gathering Requirements"},
      {location: ["gatheringRequirements", "brainstorming"]},
      {location: ["gatheringRequirements", "productSurveys"]},
      {location: ["gatheringRequirements", "observation"]},
      {location: ["gatheringRequirements", "userSurveys"]},
      {location: ["gatheringRequirements", "interviews"]},
      {location: ["gatheringRequirements", "focusGroups"]},
      {location: ["gatheringRequirements", "prototyping"]},
    {heading: "Specifying Requirements"},
      {subheading: "Prose"},
        {location: ["specifyingRequirements", "prose", "what"]},
      {subheading: "Feature Lists"},
        {location: ["specifyingRequirements", "featureList", "what"]},
      {subheading: "User Stories"},
        {location: ["specifyingRequirements", "userStories", "introduction"]},
        {location: ["specifyingRequirements", "userStories", "details"]},
        {location: ["specifyingRequirements", "userStories", "usage"]},
      {subheading: "Use Cases"},
        {location: ["specifyingRequirements", "useCases", "introduction"]},
        {location: ["specifyingRequirements", "useCases", "identifying"]},
        {location: ["specifyingRequirements", "useCases", "details"]},
        {location: ["specifyingRequirements", "useCases", "usage"]},
      {subheading: "Glossary"},
        {location: ["specifyingRequirements", "glossary", "what"]},
      {subheading: "Supplementary Requirements"},
        {location: ["specifyingRequirements", "supplementaryRequirements", "what"]},
  {name: "OOP"},
    {heading: "OOP: Classes & Objects"},
      {location: ["oop", "introduction", "what"]},
      {location: ["oop", "objects", "what"]},
      {location: ["oop", "classes", "what"]},
      {location: ["oop", "objects", "abstraction"]},
      {location: ["oop", "objects", "encapsulation"]},
      {location: ["cppToJava", "classes", "definingClasses"]},
      {location: ["cppToJava", "classes", "gettersAndSetters"]},
      {location: ["oop", "classes", "classLevelMembers"]},
      {location: ["cppToJava", "classes", "classLevelMembers"]},
      {location: ["oop", "classes", "enumerations"]},
    {heading: "Java: enumerations"},
      {location: ["cppToJava", "misc", "enums"]},
    {heading: "OOP: Inheritance"},
      {location: ["oop", "inheritance", "what"]},
      {location: ["oop", "inheritance", "overloading"]},
      {location: ["oop", "inheritance", "overriding"]},
      {location: ["cppToJava", "inheritance", "basic"]},
  {name: "Implementation"},
    {heading: "Exception Handling"},
      {location: ["errorHandling", "introduction", "what"]},
      {location: ["errorHandling", "exceptions", "what"]},
      {location: ["cppToJava", "exceptions", "what"]},
      {location: ["errorHandling", "exceptions", "how"]},
      {location: ["cppToJava", "exceptions", "how"]},
      {location: ["errorHandling", "exceptions", "when"]},
  {name: "Quality Assurance"},
    {heading: "Developer Testing: Basics"},
      {location: ["testing", "testingTypes", "developerTesting", "what"]},
      {location: ["testing", "testingTypes", "developerTesting", "why"]},
      {location: ["testing", "testAutomation", "usingTestDrivers"]},
      {location: ["testing", "testAutomation", "tools"]},
      {location: ["junit", "basic"]},
{week: "5"},
  {name: "Design"},
    {heading: "Design: Models"},
      {location: ["modeling", "introduction", "what"]},
      {location: ["modeling", "introduction", "how"]},
    {heading: "Class/Ojbect Diagrams: Basics"},
      {location: ["modeling", "modelingStructures", "ooStructures"]},
      {location: ["modeling", "modelingStructures", "classDiagramsBasic"]},
      {location: ["modeling", "modelingStructures", "objectDiagrams"]},
      {location: ["uml", "miscellaneous", "objectVsClassDiagrams"]},
  {name: "Implementation"},
    {heading: "OOP: Polymorphism"},
      {subheading: "Polymorphism"},
        {location: ["oop", "polymorphism", "what"]},
        {location: ["cppToJava", "inheritance", "polymorphism"]},
      {subheading: "Abstract Classes"},
        {location: ["oop", "inheritance", "abstractClasses"]},
        {location: ["cppToJava", "inheritance", "abstractClassesAndMethods"]},
      {subheading: "Interfaces"},
        {location: ["oop", "inheritance", "interfaces"]},
        {location: ["cppToJava", "inheritance", "interfaces"]},
  {name: "Project Management"},
    {heading: "RCS: Workflows"},
      {location: ["gitAndGithub", "mergeConflicts"]},
      {location: ["gitAndGithub", "managePRs"]},
      {location: ["revisionControl", "forkingWorkflow"]},
      {location: ["gitAndGithub", "forkingWorkflow"]},
      {location: ["revisionControl", "drcsVsCrcs"]},
      {location: ["revisionControl", "featureBranchFlow"]},
      {location: ["revisionControl", "centralizedFlow"]},
{week: "6"},
  {name: "Design"},
    {heading: "Class Diagrams: Intermediate-Level"},
      {location: ["uml", "notes", "notes"]},
      {location: ["uml", "notes", "constraints"]},
      {location: ["uml", "classDiagrams", "associationsAsAttributes", "what"]},
      {location: ["modeling", "modelingStructures", "classDiagramsIntermediate"]},
    {heading: "Sequence Diagrams: Basics"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsBasic"]},
    {heading: "Architecture Diagrams"},
      {location: ["design", "introduction", "what"]},
      {location: ["architecture", "architectureDiagrams", "reading"]},
      {location: ["designApproaches", "multilevelDesign", "what"]},
  {name: "Implementation"},
    {heading: "Logging"},
      {location: ["errorHandling", "logging", "what"]},
      {location: ["errorHandling", "logging", "how"]},
    {heading: "Assertions"},
      {location: ["errorHandling", "assertions", "what"]},
      {location: ["errorHandling", "assertions", "how"]},
      {location: ["errorHandling", "assertions", "when"]},
    {heading: "Java: streams"},
      {location: ["javaTools", "streamsBasic"]},
    {heading: "Java: JavaFX"},
      {location: ["javaTools", "javaFXBasic"]},
  {name: "Project Management"},
    {heading: "Continuous Integration/Deployment"},
      {location: ["integration", "introduction", "what"]},
      {location: ["integration", "buildAutomation", "what"]},
      {location: ["integration", "buildAutomation", "continuousIntegrationDeployment"]},
{week: "7"},
  {name: "Design"},
    {heading: "Architectural Styles"},
      {location: ["architecture", "architecturalStyles", "introduction", "what"]},
      {location: ["architecture", "architecturalStyles", "nTier", "what"]},
      {location: ["architecture", "architecturalStyles", "clientServer", "what"]},
      {location: ["architecture", "architecturalStyles", "eventDriven", "what"]},
      {location: ["architecture", "architecturalStyles", "transactionProcessing", "what"]},
      {location: ["architecture", "architecturalStyles", "serviceOriented", "what"]},
      {location: ["architecture", "architecturalStyles", "more", "moreStyles"]},
      {location: ["architecture", "architecturalStyles", "more", "usingStyles"]},
    {heading: "APIs"},
      {location: ["reuse", "apis", "what"]},
    {heading: "Sequence Diagrams: Intermediate-Level"},
      {location: ["modeling", "modelingBehaviors", "sequenceDiagramsIntermediate"]},
      {location: ["uml", "sequenceDiagrams", "referenceFrames"]},
      {location: ["uml", "sequenceDiagrams", "parallelPaths"]},
  {name: "Implementation"},
    {heading: "CodeQuality: Readability"},
      {location: ["codeQuality", "maximiseReadability", "introduction"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidLongMethods"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidDeepNesting"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidComplicatedExpressions"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "avoidMagicNumbers"]},
      {location: ["codeQuality", "maximiseReadability", "basic", "makeCodeObvious"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "structureCodeLogically"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "dontTripReader"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "practiceKISSing"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "avoidPrematureOptimizations"]},
      {location: ["codeQuality", "maximiseReadability", "intermediate", "slapHard"]},
      {location: ["codeQuality", "maximiseReadability", "advanced", "makeHappyPathProminent"]},
    {heading: "CodeQuality: Naming"},
      {location: ["codeQuality", "nameWell", "introduction"]},
      {location: ["codeQuality", "nameWell", "basic", "nounsAndVerbsAsNames"]},
      {location: ["codeQuality", "nameWell", "basic", "useStandardWords"]},
      {location: ["codeQuality", "nameWell", "intermediate", "useNameExplain"]},
      {location: ["codeQuality", "nameWell", "intermediate", "notTooLongNorShort"]},
      {location: ["codeQuality", "nameWell", "intermediate", "avoidMisleadingNames"]},
    {heading: "CodeQuality: Unsafe Practices"},
      {location: ["codeQuality", "avoidShortcuts", "introduction"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "useDefaultBranch"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "dontRecycleVarsOrParams"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "avoidEmptyCatchBlocks"]},
      {location: ["codeQuality", "avoidShortcuts", "basic", "deleteDeadCode"]},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseVariableScope"]},
      {location: ["codeQuality", "avoidShortcuts", "intermediate", "minimiseCodeDuplication"]},
    {heading: "CodeQuality: Code Comments"},
      {location: ["codeQuality", "commentMinimally", "introduction"]},
      {location: ["codeQuality", "commentMinimally", "basic", "dontRepeatObvious"]},
      {location: ["codeQuality", "commentMinimally", "basic", "writeToReader"]},
      {location: ["codeQuality", "commentMinimally", "intermediate", "explainWhatWhyNotHow"]},
{week: "8"},
  {name: "Design"},
    {heading: "Design Principles: Basics"},
      {subheading: "Abstraction"},
        {location: ["designFundamentals", "abstraction", "what"]},
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
      {location: ["integration", "approaches", "lateVsEarly"]},
      {location: ["integration", "approaches", "bigBangVsIncremental"]},
      {location: ["integration", "approaches", "topDownVsBottomUp"]},
    {heading: "Association Classes"},
      {location: ["oop", "associations", "associationClasses"]},
  {name: "Quality Assurance"},
    {heading: "Types of Testing"},
      {subheading: "Unit Testing"},
        {location: ["testing", "testingTypes", "unitTesting", "what"]},
        {location: ["testing", "testingTypes", "unitTesting", "stubs"]},
        {location: ["testing", "dependencyInjection", "what"]},
        {location: ["testing", "dependencyInjection", "how"]},
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
      {location: ["testing", "introduction", "testability"]},
      {location: ["testing", "testCoverage", "what"]},
      {location: ["testing", "testCoverage", "how"]},
      {location: ["junit", "intermediate"]},
      {location: ["testing", "tdd", "what"]},
  {name: "Project Management"},
    {heading: "Project Mgt: Scheduling and Tracking"},
      {location: ["projectPlanning", "milestones"]},
      {location: ["projectPlanning", "buffers"]},
      {location: ["projectPlanning", "issueTrackers"]},
      {location: ["projectPlanning", "workBreakdownStructure"]},
      {location: ["projectPlanning", "ganttCharts"]},
      {location: ["projectPlanning", "pertCharts"]},
      {location: ["teamwork", "teamStructures"]},
{week: "9"},
  {name: "Design"},
    {heading: "Conceptualize OO Solution"},
      {location: ["modeling", "modelingASolution", "introduction"]},
      {location: ["modeling", "modelingASolution", "basic"]},
      {location: ["modeling", "modelingASolution", "intermediate"]},
    {heading: "Basic Design Approaches"},
      {location: ["designApproaches", "topDownBottomUp", "what"]},
      {location: ["designApproaches", "agileDesign", "what"]},
    {heading: "Design Principles: Intermediate-Level"},
      {subheading: "How Polymorphism Works"},
        {location: ["oop", "inheritance", "substitutability"]},
        {location: ["oop", "inheritance", "dynamicAndStaticBinding"]},
        {location: ["oop", "polymorphism", "how"]},
      {subheading: "More Design Principles"},
        {location: ["principles", "liskovSubstitutionPrinciple"]},
        {location: ["principles", "lawOfDemeter"]},
        {location: ["principles", "interfaceSegregationPrinciple"]},
        {location: ["principles", "dependencyInversionPrinciple"]},
        {location: ["principles", "solidPrinciples"]},
        {location: ["principles", "yagniPrinciple"]},
        {location: ["principles", "dryPrinciple"]},
        {location: ["principles", "brooksLaw"]},
    {heading: "Activity Diagrams"},
        {location: ["modeling", "modelingBehaviors", "activityDiagrams"]},
        {location: ["modeling", "modelingBehaviors", "activityDiagramsIntermediate"]},
  {name: "Implementation"},
    {heading: "Defensive Programming"},
      {location: ["errorHandling", "defensiveProgramming", "what"]},
      {location: ["errorHandling", "defensiveProgramming", "compulsoryAssociations"]},
      {location: ["errorHandling", "defensiveProgramming", "1to1Associations"]},
      {location: ["errorHandling", "defensiveProgramming", "referentialIntegrity"]},
      {location: ["errorHandling", "defensiveProgramming", "when"]},
      {location: ["errorHandling", "designByContract", "what"]},
  {name: "Quality Assurance"},
    {heading: "Other QA Techniques"},
      {location: ["qualityAssurance", "introduction", "what"]},
      {location: ["qualityAssurance", "introduction", "validationVsVerification"]},
      {location: ["qualityAssurance", "codeReviews", "what"]},
      {location: ["qualityAssurance", "staticAnalysis", "what"]},
      {location: ["qualityAssurance", "formalVerification", "what"]},
  {name: "Documentation"},
    {heading: "Writing Developer Documents"},
      {subheading: "Type of Developer Docs"},
        {location: ["documentation", "introduction", "what"]},
      {subheading: "Guideline: Aim for Comprehensibility"},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "what"]},
        {location: ["documentation", "guidelines", "aimForComprehensibility", "how"]},
      {subheading: "Guideline: Describe Top-Down"},
        {location: ["documentation", "guidelines", "goTopDown", "what"]},
        {location: ["documentation", "guidelines", "goTopDown", "why"]},
        {location: ["documentation", "guidelines", "goTopDown", "how"]},
      {subheading: "Guideline: Minimal but Sufficient"},
        {location: ["documentation", "guidelines", "documentMinimally", "what"]},
        {location: ["documentation", "guidelines", "documentMinimally", "how"]},
      {subheading: "Drawing Architecture Diagrams"},
        {location: ["architecture", "architectureDiagrams", "drawing"]},
{week: "10"},
  {name: "Requirements"},
    {heading: "OO Domain Models"},
      {location: ["modeling", "modelingStructures", "objectOrientedDomainModels"]},
  {name: "Design"},
    {heading: "Design Patterns: Basics"},
      {subheading: "Introduction"},
        {location: ["designPatterns", "introduction", "what"]},
        {location: ["designPatterns", "introduction", "format"]},
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
      {location: ["testing", "testingTypes", "exploratoryVsScriptedTesting", "when"]},
      {location: ["testCaseDesign", "introduction", "positiveVsNegative"]},
      {location: ["testCaseDesign", "introduction", "blackVsGlass"]},
      {location: ["testCaseDesign", "more", "testingUseCases"]},
    {heading: "Equivalence Partitioning"},
      {location: ["testCaseDesign", "equivalencePartitions", "what"]},
      {location: ["testCaseDesign", "equivalencePartitions", "basic"]},
      {location: ["testCaseDesign", "equivalencePartitions", "intermediate"]},
    {heading: "Boundary Value Analysis"},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "what"]},
      {location: ["testCaseDesign", "boundaryValueAnalysis", "how"]},
{week: "11"},
  {name: "Design"},
    {heading: "Design Patterns: Intermediate-Level"},
      {location: ["designPatterns", "modelViewController", "what"]},
      {location: ["designPatterns", "observer", "what"]},
      {location: ["designPatterns", "more", "otherDesignPatterns"]},
      {location: ["designPatterns", "more", "combiningDesignPatterns"]},
      {location: ["designPatterns", "more", "usingDesignPatterns"]},
      {location: ["designPatterns", "more", "vsPrinciples"]},
      {location: ["designPatterns", "more", "otherTypesOfPatterns"]},
    {heading: "Other UML Models"},
      {location: ["modeling", "modelingStructures", "deploymentDiagrams"]},
      {location: ["modeling", "modelingStructures", "componentDiagrams"]},
      {location: ["modeling", "modelingStructures", "packageDiagrams"]},
      {location: ["modeling", "modelingStructures", "compositeStructureDiagrams"]},
      {location: ["modeling", "modelingBehaviors", "timingDiagrams"]},
      {location: ["modeling", "modelingBehaviors", "interactionOverviewDiagrams"]},
      {location: ["modeling", "modelingBehaviors", "communicationDiagrams"]},
      {location: ["modeling", "modelingBehaviors", "stateMachineDiagrams"]},
  {name: "Quality Assurance"},
    {heading: "Combining Multiple Test Inputs"},
      {location: ["testCaseDesign", "combiningTestInputs", "why"]},
      {location: ["testCaseDesign", "combiningTestInputs", "combinationStrategies"]},
      {location: ["testCaseDesign", "combiningTestInputs", "heuristicValid"]},
      {location: ["testCaseDesign", "combiningTestInputs", "heuristicInvalid"]},
      {location: ["testCaseDesign", "combiningTestInputs", "mix"]},
  {name: "Project Management"},
    {heading: "SDLC Process Models"},
      {location: ["processModels", "introduction", "what"]},
      {location: ["processModels", "introduction", "sequentialModels"]},
      {location: ["processModels", "introduction", "iterativeModels"]},
      {location: ["processModels", "introduction", "agileModels"]},
      {location: ["processModels", "exampleProcessModels", "scrum"]},
      {location: ["processModels", "exampleProcessModels", "xp"]},
      {location: ["processModels", "exampleProcessModels", "unifiedProcess"]},
      {location: ["processModels", "more", "cmmi"]},
      {location: ["processModels", "summary", "recap"]},
{week: "12"},
  {name: "Implementation"},
    {heading: "Reuse: Frameworks, Libraries, Platforms"},
      {subheading: "Reuse"},
        {location: ["reuse", "introduction", "what"]},
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
      {location: ["reuse", "cloudComputing", "what"]},
      {location: ["reuse", "cloudComputing", "services"]},
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

<div class="website-content" id="main">

{{ show_nav_buttons(week.num) }}

{{ show_week_schedule_body(week, path) }}

</div>

{% endmacro %}


{% macro show_nav_buttons(week_num) %}
{% set week_num = week_num | int %}
{% if week_num != 1 %}<span style="float:left"><md>[:glyphicon-chevron-left: Previous Week]({{ baseUrl }}/schedule/week{{ (week_num - 1) }}/)</md></span>{% endif %}{% if week_num != 13 %}<span style="float:right"><md>[Next Week :glyphicon-chevron-right:]({{ baseUrl }}/schedule/week{{ (week_num + 1) }}/)</md></span>{% endif %}<br>

{% endmacro %}


{% macro show_week_schedule_body(week, path="") %}

# Week {{ week.num }} <small><small>%%[{{ week.day }}]%%</small></small>

<tabs>
  <tab header="{{ icon_announcement }} Notices">
    <include src="{{ path }}notices-{{ module | lower }}.md" optional />
  </tab>
  <tab header="{{ icon_outcome }} Topics">
    <include src="{{ path }}topics.md" />
  </tab>
  <tab header="{{ icon_project }} Project">
    <include src="{{ path }}project.md" optional />
  </tab>
  <tab header="{{ icon_tutorial }} Tutorial">
    <include src="{{ path }}tutorial-{{ module | lower }}.md" optional />
  </tab>
  <tab header="{{ icon_info }} Admin Info">
    <include src="{{ path }}admin.md" />
  </tab>
</tabs>

{% endmacro %}




<!-- ============================= page content ============================================ -->

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