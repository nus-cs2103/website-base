{% set textbook_topics = {
  softwareEngineering : {
    name: "softwareEngineering",
    heading: "Software Engineering",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "prosAndCons", heading: "Pros and Cons", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  oop : {
    name: "oop",
    heading: "Object-Oriented Programming",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "objects",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "abstraction", heading: "Objects as Abstractions", priority: "3"},
              {name: "encapsulation", heading: "Encapsulation Of Objects", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "classes",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "classLevelMembers", heading: "Class Level Members", priority: "2"},
              {name: "enumerations", heading: "Enumerations", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "associations",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "navigability", heading: "Navigability", priority: "2"},
              {name: "multiplicity", heading: "Multiplicity", priority: "2"},
              {name: "dependencies", heading: "Dependencies", priority: "3"},
              {name: "composition", heading: "Composition", priority: "3"},
              {name: "aggregation", heading: "Aggregation", priority: "3"},
              {name: "associationClasses", heading: "Association Classes", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "inheritance",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "overriding", heading: "Overriding", priority: "2"},
              {name: "overloading", heading: "Overloading", priority: "2"},
              {name: "interfaces", heading: "Interfaces", priority: "-1"},
              {name: "abstractClasses", heading: "Abstract Classes", priority: "-1"},
              {name: "substitutability", heading: "Substitutability", priority: "-1"},
              {name: "dynamicAndStaticBinding", heading: "Dynamic and Static Binding", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "polymorphism",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "more",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "miscellaneous", heading: "Miscellaneous", priority: "3"},
              {name: "review", heading: "Review", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  requirements : {
    name: "requirements",
    heading: "Requirements",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"},
              {name: "nonFunctionalRequirements", heading: "Non-Functional Requirements", priority: "2"},
              {name: "quality", heading: "Quality of Requirements", priority: "3"},
              {name: "prioritizing", heading: "Prioritizing Requirements", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  gatheringRequirements : {
    name: "gatheringRequirements",
    heading: "Gathering Requirements",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "brainstorming", heading: "Brainstorming", priority: "3"},
              {name: "userSurveys", heading: "User Surveys", priority: "3"},
              {name: "observation", heading: "Observation", priority: "3"},
              {name: "interviews", heading: "Interviews", priority: "3"},
              {name: "focusGroups", heading: "Focus Groups", priority: "3"},
              {name: "prototyping", heading: "Prototyping", priority: "3"},
              {name: "productSurveys", heading: "Product Surveys", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  specifyingRequirements : {
    name: "specifyingRequirements",
    heading: "Specifying Requirements",
    level_one_topics: [
      {
        name: "prose",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "featureList",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "userStories",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "details", heading: "Details", priority: "2"},
              {name: "usage", heading: "Usage", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "useCases",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "identifying", heading: "Identifying", priority: "2"},
              {name: "details", heading: "Details", priority: "2"},
              {name: "usage", heading: "Usage", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "glossary",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "supplementaryRequirements",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  design : {
    name: "design",
    heading: "Software Design",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  designFundamentals : {
    name: "designFundamentals",
    heading: "Design Fundamentals",
    level_one_topics: [
      {
        name: "abstraction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "coupling",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"},
              {name: "types", heading: "Types of Coupling", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "cohesion",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  modeling : {
    name: "modeling",
    heading: "Modeling",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"},
              {name: "umlModels", heading: "UML Models", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "modelingStructures",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "ooStructures", heading: "OO Structures", priority: "1"},
              {name: "classDiagramsBasic", heading: "Class Diagrams (Basics)", priority: "-1"},
              {name: "addingMoreInfo", heading: "Adding More Info to UML Models", priority: "-1"},
              {name: "classDiagramsIntermediate", heading: "Class Diagrams - Intermediate", priority: "-1"},
              {name: "classDiagramsAdvanced", heading: "Class Diagrams - Advanced", priority: "-1"},
              {name: "objectDiagrams", heading: "Object Diagrams", priority: "-1"},
              {name: "objectOrientedDomainModels", heading: "Object Oriented Domain Models", priority: "4"},
              {name: "deploymentDiagrams", heading: "Deployment Diagrams", priority: "4"},
              {name: "componentDiagrams", heading: "Component Diagrams", priority: "4"},
              {name: "packageDiagrams", heading: "Package Diagrams", priority: "4"},
              {name: "compositeStructureDiagrams", heading: "Composite Structure Diagrams", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "modelingBehaviors",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "activityDiagrams", heading: "Activity Diagrams - Basic", priority: "1"},
              {name: "activityDiagramsIntermediate", heading: "Activity Diagrams - Intermediate", priority: "4"},
              {name: "sequenceDiagramsBasic", heading: "Sequence Diagrams - Basic", priority: "4"},
              {name: "sequenceDiagramsIntermediate", heading: "Sequence Diagrams - Intermediate", priority: "-1"},
              {name: "sequenceDiagramsAdvanced", heading: "Sequence Diagrams - Advanced", priority: "-1"},
              {name: "useCaseDiagrams", heading: "Use Case Diagrams", priority: "2"},
              {name: "timingDiagrams", heading: "Timing Diagrams", priority: "4"},
              {name: "interactionOverviewDiagrams", heading: "Interaction Overview Diagrams", priority: "4"},
              {name: "communicationDiagrams", heading: "Communication Diagrams", priority: "4"},
              {name: "stateMachineDiagrams", heading: "State Machine Diagrams", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "modelingASolution",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"},
              {name: "basic", heading: "Basic", priority: "3"},
              {name: "intermediate", heading: "Intermediate", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  architecture : {
    name: "architecture",
    heading: "Software Architecture",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "architectureDiagrams",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "reading", heading: "Reading", priority: "1"},
              {name: "drawing", heading: "Drawing", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "architecturalStyles",
        level_two_topics: [
          {
            name: "introduction",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "nTier",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "clientServer",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "transactionProcessing",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "serviceOriented",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "eventDriven",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "more",
            level_three_topics: [
              {name: "moreStyles", heading: "More Styles", priority: "4"},
              {name: "usingStyles", heading: "Using Styles", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  designPatterns : {
    name: "designPatterns",
    heading: "Software Design Patterns",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "format", heading: "Format", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "singleton",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "implementation", heading: "Implementation", priority: "2"},
              {name: "evaluation", heading: "Evaluation", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "abstractionOccurrence",
        priority: "4",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "facade",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "command",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "modelViewController",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "observer",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "more",
        priority: "4",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "combiningDesignPatterns", heading: "Combining Design Patterns", priority: "4"},
              {name: "otherDesignPatterns", heading: "Other Design Patterns", priority: "4"},
              {name: "usingDesignPatterns", heading: "Using Design Patterns", priority: "4"},
              {name: "otherTypesOfPatterns", heading: "Other Types of Patterns", priority: "4"},
              {name: "vsPrinciples", heading: "Design Patterns vs Design Principles", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  designApproaches : {
    name: "designApproaches",
    heading: "Design Approaches",
    level_one_topics: [
      {
        name: "multilevelDesign",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "topDownBottomUp",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "agileDesign",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  ides : {
    name: "ides",
    heading: "IDEs",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "debugging",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  codeQuality : {
    name: "codeQuality",
    heading: "Code Quality",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "basic", heading: "Basic", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "maximizeReadability",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "avoidLongMethods", heading: "Avoid Long Methods", priority: "3"},
              {name: "avoidDeepNesting", heading: "Avoid Deep Nesting", priority: "3"},
              {name: "avoidComplicatedExpressions", heading: "Avoid Complicated Expressions", priority: "3"},
              {name: "avoidMagicNumbers", heading: "Avoid Magic Numbers", priority: "3"},
              {name: "makeCodeObvious", heading: "Make the Code Obvious", priority: "4"}
            ]
          },
          {
            name: "intermediate",
            priority: "-1",
            level_three_topics: [
              {name: "structureCodeLogically", heading: "Structure Code Logically", priority: "3"},
              {name: "dontTripReader", heading: "Do Not 'Trip Up' Reader", priority: "3"},
              {name: "practiceKISSing", heading: "Practice KISSing", priority: "3"},
              {name: "avoidPrematureOptimizations", heading: "Avoid Premature Optimizations", priority: "3"},
              {name: "slapHard", heading: "SLAP Hard", priority: "3"}
            ]
          },
          {
            name: "advanced",
            priority: "-1",
            level_three_topics: [
              {name: "makeHappyPathProminent", heading: "Make the Happy Path Prominent", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "followStandard",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "3"},
              {name: "basic", heading: "Basic", priority: "4"},
              {name: "intermediate", heading: "Intermediate", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "nameWell",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "nounsAndVerbsAsNames", heading: "Use Nouns for Things and Verbs for Actions", priority: "2"},
              {name: "useStandardWords", heading: "Use Standard Words", priority: "3"}
            ]
          },
          {
            name: "intermediate",
            priority: "-1",
            level_three_topics: [
              {name: "useNameExplain", heading: "Use Name to Explain", priority: "3"},
              {name: "notTooLongNorShort", heading: "Not Too Long, Not Too Short", priority: "3"},
              {name: "avoidMisleadingNames", heading: "Avoid Misleading Names", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "avoidShortcuts",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "useDefaultBranch", heading: "Use the Default Branch", priority: "-1"},
              {name: "dontRecycleVarsOrParams", heading: "Don't Recycle Variables or Parameters", priority: "2"},
              {name: "avoidEmptyCatchBlocks", heading: "Avoid Empty Catch Blocks", priority: "-1"},
              {name: "deleteDeadCode", heading: "Delete Dead Code", priority: "-1"}
            ]
          },
          {
            name: "intermediate",
            priority: "-1",
            level_three_topics: [
              {name: "minimiseVariableScope", heading: "Minimize Scope of Variables", priority: "3"},
              {name: "minimiseCodeDuplication", heading: "Minimize Code Duplication", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "commentMinimally",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "dontRepeatObvious", heading: "Do Not Repeat the Obvious", priority: "2"},
              {name: "writeToReader", heading: "Write to the Reader", priority: "3"}
            ]
          },
          {
            name: "intermediate",
            priority: "-1",
            level_three_topics: [
              {name: "explainWhatWhyNotHow", heading: "Explain WHAT and WHY, not HOW", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  refactoring : {
    name: "refactoring",
    heading: "Refactoring",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "-1"},
              {name: "when", heading: "When", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  documentation : {
    name: "documentation",
    heading: "Documentation",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "guidelines",
        level_two_topics: [
          {
            name: "goTopDown",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "why", heading: "Why", priority: "3"},
              {name: "how", heading: "How", priority: "2"}
            ]
          },
          {
            name: "aimForComprehensibility",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          },
          {
            name: "documentMinimally",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "tools",
        priority: "-1",
        level_two_topics: [
          {
            name: "javaDoc",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  errorHandling : {
    name: "errorHandling",
    heading: "Error Handling",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "exceptions",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "2"},
              {name: "when", heading: "When", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "assertions",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"},
              {name: "when", heading: "When", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "logging",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "defensiveProgramming",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "compulsoryAssociations", heading: "Enforcing Compulsory Associations", priority: "3"},
              {name: "1to1Associations", heading: "Enforcing 1-to-1 Associations", priority: "4"},
              {name: "referentialIntegrity", heading: "Enforcing Referential Integrity", priority: "4"},
              {name: "when", heading: "When", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "designByContract",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "Design by Contract", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  integration : {
    name: "integration",
    heading: "Integration",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "approaches",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "lateVsEarly", heading: "Late-and-One-Time vs Early-and-Frequent", priority: "3"},
              {name: "bigBangVsIncremental", heading: "Big-Bang vs Incremental Integration", priority: "3"},
              {name: "topDownVsBottomUp", heading: "Top-Down vs Bottom-Up Integration", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "buildAutomation",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "continuousIntegrationDeployment", heading: "Continuous Integration and Continuous Deployment", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "more",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "review", heading: "Review", priority: "-1"}
            ]
          }
        ]
      }
    ]
  },
  reuse : {
    name: "reuse",
    heading: "Reuse",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "when", heading: "When", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "apis",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "designingAPIs", heading: "Designing APIs", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "libraries",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "frameworks",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "frameworksVsLibraries", heading: "Frameworks vs Libraries", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "platforms",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "cloudComputing",
        priority: "3",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "services", heading: "Iaas, PaaS, and SaaS", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  qualityAssurance : {
    name: "qualityAssurance",
    heading: "Quality Assurance",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "validationVsVerification", heading: "Validation vs Verification", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "codeReviews",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "staticAnalysis",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "formalVerification",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  testing : {
    name: "testing",
    heading: "Testing",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "testability", heading: "Testability", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "testingTypes",
        level_two_topics: [
          {
            name: "regressionTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "developerTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "why", heading: "Why", priority: "4"}
            ]
          },
          {
            name: "unitTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "stubs", heading: "Stubs", priority: "-1"}
            ]
          },
          {
            name: "integrationTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "-1"}
            ]
          },
          {
            name: "systemTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "alphaBetaTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "dogfooding",
            priority: "4",
            level_three_topics: [
              {name: "what", heading: "What", priority: "4"}
            ]
          },
          {
            name: "exploratoryVsScriptedTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "when", heading: "When", priority: "4"}
            ]
          },
          {
            name: "acceptanceTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "acceptanceVsSystemTesting", heading: "Acceptance vs System Testing", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "testAutomation",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "testingTextUis", heading: "Automated Testing of CLI Apps", priority: "3"},
              {name: "usingTestDrivers", heading: "Test Automation Using Test Drivers", priority: "-1"},
              {name: "tools", heading: "Test Automation Tools", priority: "-1"},
              {name: "testingGuis", heading: "Automated Testing of GUIs", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "testCoverage",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "dependencyInjection",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "how", heading: "How", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "tdd",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "4"},
              {name: "how", heading: "How", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  testCaseDesign : {
    name: "testCaseDesign",
    heading: "Test Case Design",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "positiveVsNegative", heading: "Positive vs Negative Test Cases", priority: "-1"},
              {name: "blackVsGlass", heading: "Black Box vs Glass Box", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "equivalencePartitions",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "basic", heading: "Basic", priority: "2"},
              {name: "intermediate", heading: "Intermediate", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "boundaryValueAnalysis",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "how", heading: "How", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "combiningTestInputs",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "why", heading: "Why", priority: "2"},
              {name: "combinationStrategies", heading: "Test Input Combination Strategies", priority: "2"},
              {name: "heuristicValid", heading: "Heuristic: Each Valid Input at Least Once in a Positive Test Case", priority: "3"},
              {name: "heuristicInvalid", heading: "Heuristic: Test Invalid Inputs Individually Before Combining Them", priority: "3"},
              {name: "mix", heading: "Mix", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "more",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "testingUseCases", heading: "Testing Based on Use Cases", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "summary",
        priority: "4",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "recap", heading: "Recap", priority: "-1"},
              {name: "exercises", heading: "Exercises", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  projectPlanning : {
    name: "projectPlanning",
    heading: "Project Planning",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "workBreakdownStructure", heading: "Work Breakdown Structure", priority: "3"},
              {name: "milestones", heading: "Milestones", priority: "2"},
              {name: "buffers", heading: "Buffers", priority: "3"},
              {name: "issueTrackers", heading: "Issue Trackers", priority: "2"},
              {name: "ganttCharts", heading: "GANTT Charts", priority: "4"},
              {name: "pertCharts", heading: "PERT Charts", priority: "4"}
            ]
          }
        ]
      }
    ]
  },
  teamwork : {
    name: "teamwork",
    heading: "Teamwork",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "teamStructures", heading: "Team Structures", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  processModels : {
    name: "processModels",
    heading: "SDLC Process Models",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"},
              {name: "sequentialModels", heading: "Sequential Models", priority: "2"},
              {name: "iterativeModels", heading: "Iterative Models", priority: "2"},
              {name: "agileModels", heading: "Agile Models", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "exampleProcessModels",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "xp", heading: "XP", priority: "3"},
              {name: "scrum", heading: "Scrum", priority: "3"},
              {name: "unifiedProcess", heading: "Unified Process", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "more",
        priority: "4",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "cmmi", heading: "CMMI", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "summary",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "recap", heading: "Recap", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  uml : {
    name: "uml",
    heading: "UML",
    level_one_topics: [
      {
        name: "classDiagrams",
        level_two_topics: [
          {
            name: "introduction",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "classes",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "associations",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "navigability", heading: "Navigability", priority: "2"},
              {name: "roles", heading: "Roles", priority: "3"},
              {name: "labels", heading: "Labels", priority: "3"},
              {name: "multiplicity", heading: "Multiplicity", priority: "2"}
            ]
          },
          {
            name: "dependencies",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "associationsAsAttributes",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "enumerations",
            priority: "-1",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "classLevelMembers",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "associationClasses",
            priority: "-1",
            level_three_topics: [
              {name: "what", heading: "What", priority: "-1"}
            ]
          },
          {
            name: "composition",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "aggregation",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "classInheritance",
            level_three_topics: [
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "interfaces",
            priority: "-1",
            level_three_topics: [
              {name: "what", heading: "What", priority: "-1"}
            ]
          },
          {
            name: "abstractClasses",
            priority: "-1",
            level_three_topics: [
              {name: "what", heading: "What", priority: "-1"}
            ]
          },
          {
            name: "combine",
            priority: "-1",
            level_three_topics: [
              {name: "basic", heading: "Basic", priority: "-1"}
            ]
          }
        ]
      },
      {
        name: "sequenceDiagrams",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "objectCreation", heading: "Object Creation", priority: "2"},
              {name: "objectDeletion", heading: "Object Deletion", priority: "3"},
              {name: "loops", heading: "Loops", priority: "2"},
              {name: "selfInvocation", heading: "Self Invocation", priority: "3"},
              {name: "alternativePaths", heading: "Alternative Paths", priority: "3"},
              {name: "optionalPaths", heading: "Optional Paths", priority: "3"},
              {name: "parallelPaths", heading: "Parallel Paths", priority: "4"},
              {name: "referenceFrames", heading: "Reference Frames", priority: "4"},
              {name: "minimalNotation", heading: "Minimal Notation", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "objectDiagrams",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "2"},
              {name: "objects", heading: "Objects", priority: "2"},
              {name: "associations", heading: "Associations", priority: "2"}
            ]
          }
        ]
      },
      {
        name: "activityDiagrams",
        level_two_topics: [
          {
            name: "introduction",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "basicNotations",
            level_three_topics: [
              {name: "linearPaths", heading: "Linear Paths", priority: "1"},
              {name: "alternatePaths", heading: "Alternate Paths", priority: "2"},
              {name: "parallelPaths", heading: "Parallel Paths", priority: "2"},
              {name: "rakes", heading: "Rakes", priority: "4"},
              {name: "swimlanes", heading: "Swimlanes", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "notes",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "notes", heading: "Notes", priority: "3"},
              {name: "constraints", heading: "Constraints", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "miscellaneous",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "objectVsClassDiagrams", heading: "Object vs Class Diagrams", priority: "2"}
            ]
          }
        ]
      }
    ]
  },
  intellij : {
    name: "intellij",
    heading: "IntelliJ IDEA",
    priority: "4",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            priority: "4",
            level_three_topics: [
              {name: "projectSetup", heading: "Project Setup", priority: "1"},
              {name: "codeNavigation", heading: "Code Navigation", priority: "2"},
              {name: "productivityShortcuts", heading: "Productivity Shortcuts", priority: "4"},
              {name: "debuggingBasic", heading: "Debugging: Basic", priority: "3"},
              {name: "refactoring", heading: "Refactoring", priority: "2"}
            ]
          }
        ]
      }
    ]
  },
  gitAndGithub : {
    name: "gitAndGithub",
    heading: "Git and Github",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "init", heading: "Init", priority: "1"},
              {name: "commit", heading: "Commit", priority: "1"},
              {name: "ignore", heading: "Ignore", priority: "2"},
              {name: "tag", heading: "Tag", priority: "3"},
              {name: "checkout", heading: "Checkout", priority: "2"},
              {name: "clone", heading: "Clone", priority: "1"},
              {name: "pull", heading: "Pull", priority: "1"},
              {name: "push", heading: "Push", priority: "1"},
              {name: "branch", heading: "Branch", priority: "2"},
              {name: "mergeConflicts", heading: "Merge Conflicts", priority: "2"},
              {name: "createPRs", heading: "Create PRs", priority: "1"},
              {name: "managePRs", heading: "Manage PRs", priority: "2"},
              {name: "forkingWorkflow", heading: "Forking Workflow", priority: "3"}
            ]
          }
        ]
      }
    ]
  },
  principles : {
    name: "principles",
    heading: "Principles",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "singleResponsibilityPrinciple", heading: "Single Responsibility Principle", priority: "3"},
              {name: "openClosedPrinciple", heading: "Open-Closed Principle", priority: "3"},
              {name: "liskovSubstitutionPrinciple", heading: "Liskov Substitution Principle", priority: "0:3"},
              {name: "interfaceSegregationPrinciple", heading: "Interface Segregation Principle", priority: "4"},
              {name: "dependencyInversionPrinciple", heading: "Dependency Inversion Principle", priority: "4"},
              {name: "solidPrinciples", heading: "SOLID Principles", priority: "4"},
              {name: "separationOfConcernsPrinciple", heading: "Separation of Concerns Principle", priority: "2"},
              {name: "lawOfDemeter", heading: "Law of Demeter", priority: "3"},
              {name: "yagniPrinciple", heading: "YAGNI Principle", priority: "4"},
              {name: "dryPrinciple", heading: "DRY Principle", priority: "4"},
              {name: "brooksLaw", heading: "Brooks' Law", priority: "4"},
              {name: "review", heading: "Review", priority: "-1"}
            ]
          }
        ]
      }
    ]
  },
  cppToJava : {
    name: "cppToJava",
    heading: "C++ to Java",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "about", heading: "About this Book Chapter", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "javaWorld",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What is Java?", priority: "0:3"},
              {name: "how", heading: "How Java Works", priority: "0:4"},
              {name: "editions", heading: "Java Editions", priority: "0:4"}
            ]
          }
        ]
      },
      {
        name: "gettingStarted",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "installation", heading: "Installation", priority: "0:1"},
              {name: "helloWorld", heading: "HelloWorld", priority: "0:1"},
              {name: "compiling", heading: "Compiling Programs", priority: "0:1"},
              {name: "running", heading: "Running Programs", priority: "0:1"}
            ]
          }
        ]
      },
      {
        name: "dataTypes",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "primitiveTypes", heading: "Primitive Data Types", priority: "0:1"},
              {name: "variables", heading: "Variables", priority: "0:1"},
              {name: "operators", heading: "Operators", priority: "0:1"},
              {name: "arrays", heading: "Arrays", priority: "0:1"}
            ]
          }
        ]
      },
      {
        name: "controlFlow",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "branching", heading: "Branching", priority: "0:1"},
              {name: "methods", heading: "Methods", priority: "0:1"},
              {name: "loops", heading: "Loops", priority: "0:1"}
            ]
          }
        ]
      },
      {
        name: "objects",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "usingObjects", heading: "Using Java Objects", priority: "0:1"},
              {name: "instanceMembers", heading: "Instance Members", priority: "0:1"},
              {name: "passingObjects", heading: "Passing Objects", priority: "0:1"},
              {name: "garbageCollection", heading: "Garbage Collection", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "classes",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "definingClasses", heading: "Defining Classes", priority: "0:1"},
              {name: "gettersAndSetters", heading: "Getters and Setters", priority: "0:1"},
              {name: "classLevelMembers", heading: "Class-Level Members", priority: "0:2"}
            ]
          }
        ]
      },
      {
        name: "usefulClasses",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "api", heading: "Java API", priority: "0:2"},
              {name: "stringClass", heading: "The String Class", priority: "0:1"},
              {name: "wrapperClasses", heading: "Wrapper Classes for Primitive Types", priority: "0:3"},
              {name: "arraysClass", heading: "The Arrays Class", priority: "0:2"},
              {name: "scannerClass", heading: "The Scanner Class", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "inheritance",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "basic", heading: "Inheritance (Basic)", priority: "0:2"},
              {name: "objectClass", heading: "The Object Class", priority: "0:2"},
              {name: "interfaces", heading: "Interfaces", priority: "0:3"},
              {name: "polymorphism", heading: "Polymorhism", priority: "0:3"},
              {name: "abstractClassesAndMethods", heading: "Abstract Classes and Methods", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "exceptions",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What are Exceptions?", priority: "0:2"},
              {name: "how", heading: "How to use Exceptions", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "generics",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What are Generics?", priority: "0:2"},
              {name: "how", heading: "How to use Generics", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "collections",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "The Collections Framework", priority: "0:3"},
              {name: "arrayListClass", heading: "The ArrayList Class", priority: "0:2"},
              {name: "hashMapClass", heading: "The HashMap Class", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "junit",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "basic", heading: "JUnit: Basic", priority: "2"},
              {name: "intermediate", heading: "JUnit: Intermediate", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "misc",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "enums", heading: "Enums", priority: "0:2"},
              {name: "packages", heading: "Packages", priority: "0:2"},
              {name: "fileAccess", heading: "File Access", priority: "0:3"},
              {name: "accessModifiers", heading: "Access Modifiers", priority: "0:1"},
              {name: "constants", heading: "Constants", priority: "0:1"},
              {name: "casting", heading: "Casting", priority: "0:1"},
              {name: "jar", heading: "JAR Files", priority: "0:3"},
              {name: "varargs", heading: "Varargs", priority: "0:3"},
              {name: "streams", heading: "Streams", priority: "0:3"},
              {name: "javaFX", heading: "JavaFX", priority: "3"}
            ]
          }
        ]
      }
    ]
  }
} %}
