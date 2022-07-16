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
              {name: "prosAndCons", heading: "Pros and Cons", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:1"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "abstraction", heading: "Objects as Abstractions", priority: "0:2"},
              {name: "encapsulation", heading: "Encapsulation Of Objects", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:1"},
              {name: "classLevelMembers", heading: "Class Level Members", priority: "0:2"},
              {name: "enumerations", heading: "Enumerations", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:1"},
              {name: "navigability", heading: "Navigability", priority: "0:2"},
              {name: "multiplicity", heading: "Multiplicity", priority: "0:2"},
              {name: "dependencies", heading: "Dependencies", priority: "0:3"},
              {name: "composition", heading: "Composition", priority: "0:3"},
              {name: "aggregation", heading: "Aggregation", priority: "0:3"},
              {name: "associationClasses", heading: "Association Classes", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:1"},
              {name: "overriding", heading: "Overriding", priority: "0:2"},
              {name: "overloading", heading: "Overloading", priority: "0:2"},
              {name: "interfaces", heading: "Interfaces", priority: "0:3"},
              {name: "abstractClasses", heading: "Abstract Classes", priority: "0:3"},
              {name: "substitutability", heading: "Substitutability", priority: "0:3"},
              {name: "dynamicAndStaticBinding", heading: "Dynamic and Static Binding", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "polymorphism",
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
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "miscellaneous", heading: "Miscellaneous", priority: "0:3"},
              {name: "review", heading: "Review", priority: "0:3"}
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
              {name: "introduction", heading: "Introduction", priority: "0:2"},
              {name: "nonFunctionalRequirements", heading: "Non-Functional Requirements", priority: "0:2"},
              {name: "prioritizing", heading: "Prioritizing Requirements", priority: "0:3"},
              {name: "quality", heading: "Quality of Requirements", priority: "0:3"}
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
              {name: "brainstorming", heading: "Brainstorming", priority: "0:3"},
              {name: "userSurveys", heading: "User Surveys", priority: "0:3"},
              {name: "observation", heading: "Observation", priority: "0:3"},
              {name: "interviews", heading: "Interviews", priority: "0:3"},
              {name: "focusGroups", heading: "Focus Groups", priority: "0:3"},
              {name: "prototyping", heading: "Prototyping", priority: "0:3"},
              {name: "productSurveys", heading: "Product Surveys", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"}
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
              {name: "introduction", heading: "Introduction", priority: "0:1"},
              {name: "details", heading: "Details", priority: "0:2"},
              {name: "usage", heading: "Usage", priority: "0:2"}
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
              {name: "introduction", heading: "Introduction", priority: "0:2"},
              {name: "identifying", heading: "Identifying", priority: "0:4"},
              {name: "details", heading: "Details", priority: "0:4"},
              {name: "usage", heading: "Usage", priority: "0:4"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"}
            ]
          }
        ]
      },
      {
        name: "coupling",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"},
              {name: "types", heading: "Types of Coupling", priority: "0:4"}
            ]
          }
        ]
      },
      {
        name: "cohesion",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"},
              {name: "umlModels", heading: "UML Models", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "modelingStructures",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "ooStructures", heading: "OO Structures", priority: "0:1"},
              {name: "classDiagramsBasic", heading: "Class Diagrams (Basics)", priority: "0:1"},
              {name: "addingMoreInfo", heading: "Adding More Info to UML Models", priority: "0:3"},
              {name: "classDiagramsIntermediate", heading: "Class Diagrams - Intermediate", priority: "0:2"},
              {name: "classDiagramsAdvanced", heading: "Class Diagrams - Advanced", priority: "3"},
              {name: "objectDiagrams", heading: "Object Diagrams", priority: "0:1"},
              {name: "objectOrientedDomainModels", heading: "Object Oriented Domain Models", priority: "0:4"},
              {name: "deploymentDiagrams", heading: "Deployment Diagrams", priority: "0:4"},
              {name: "componentDiagrams", heading: "Component Diagrams", priority: "0:4"},
              {name: "packageDiagrams", heading: "Package Diagrams", priority: "0:4"},
              {name: "compositeStructureDiagrams", heading: "Composite Structure Diagrams", priority: "0:4"}
            ]
          }
        ]
      },
      {
        name: "modelingBehaviors",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "activityDiagrams", heading: "Activity Diagrams - Basic", priority: "3"},
              {name: "activityDiagramsIntermediate", heading: "Activity Diagrams - Intermediate", priority: "3"},
              {name: "sequenceDiagramsBasic", heading: "Sequence Diagrams - Basic", priority: "0:2"},
              {name: "sequenceDiagramsIntermediate", heading: "Sequence Diagrams - Intermediate", priority: "0:3"},
              {name: "sequenceDiagramsAdvanced", heading: "Sequence Diagrams - Advanced", priority: "-1"},
              {name: "useCaseDiagrams", heading: "Use Case Diagrams", priority: "0:4"},
              {name: "timingDiagrams", heading: "Timing Diagrams", priority: "0:4"},
              {name: "interactionOverviewDiagrams", heading: "Interaction Overview Diagrams", priority: "0:4"},
              {name: "communicationDiagrams", heading: "Communication Diagrams", priority: "0:4"},
              {name: "stateMachineDiagrams", heading: "State Machine Diagrams", priority: "0:4"}
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
              {name: "introduction", heading: "Introduction", priority: "0:2"},
              {name: "basic", heading: "Basic", priority: "0:3"},
              {name: "intermediate", heading: "Intermediate", priority: "0:4"}
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
              {name: "drawing", heading: "Drawing", priority: "3"}
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
              {name: "what", heading: "What", priority: "2"}
            ]
          },
          {
            name: "nTier",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
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
            priority: "4",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "serviceOriented",
            priority: "4",
            level_three_topics: [
              {name: "what", heading: "What", priority: "4"}
            ]
          },
          {
            name: "eventDriven",
            priority: "4",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "more",
            priority: "4",
            level_three_topics: [
              {name: "moreStyles", heading: "More Styles", priority: "4"},
              {name: "usingStyles", heading: "Using Styles", priority: "4"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "format", heading: "Format", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "implementation", heading: "Implementation", priority: "0:2"},
              {name: "evaluation", heading: "Evaluation", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "abstractionOccurrence",
        priority: "-1",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:4"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "3"}
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
              {name: "what", heading: "What", priority: "0:1"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "basic", heading: "Basic", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "maximiseReadability",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "0:1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "avoidLongMethods", heading: "Avoid Long Methods", priority: "0:2"},
              {name: "avoidDeepNesting", heading: "Avoid Deep Nesting", priority: "0:2"},
              {name: "avoidComplicatedExpressions", heading: "Avoid Complicated Expressions", priority: "0:2"},
              {name: "avoidMagicNumbers", heading: "Avoid Magic Numbers", priority: "0:2"},
              {name: "makeCodeObvious", heading: "Make the Code Obvious", priority: "0:2"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "structureCodeLogically", heading: "Structure Code Logically", priority: "0:3"},
              {name: "dontTripReader", heading: "Do Not 'Trip Up' Reader", priority: "0:3"},
              {name: "practiceKISSing", heading: "Practice KISSing", priority: "0:3"},
              {name: "avoidPrematureOptimizations", heading: "Avoid Premature Optimizations", priority: "0:3"},
              {name: "slapHard", heading: "SLAP Hard", priority: "0:3"}
            ]
          },
          {
            name: "advanced",
            level_three_topics: [
              {name: "makeHappyPathProminent", heading: "Make the Happy Path Prominent", priority: "0:3"}
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
              {name: "introduction", heading: "Introduction", priority: "0:2"},
              {name: "basic", heading: "Basic", priority: "0:1"},
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
              {name: "introduction", heading: "Introduction", priority: "0:2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "nounsAndVerbsAsNames", heading: "Use Nouns for Things and Verbs for Actions", priority: "0:2"},
              {name: "useStandardWords", heading: "Use Standard Words", priority: "0:3"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "useNameExplain", heading: "Use Name to Explain", priority: "0:3"},
              {name: "notTooLongNorShort", heading: "Not Too Long, Not Too Short", priority: "0:3"},
              {name: "avoidMisleadingNames", heading: "Avoid Misleading Names", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "avoidShortcuts",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "0:2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "useDefaultBranch", heading: "Use the Default Branch", priority: "0:2"},
              {name: "dontRecycleVarsOrParams", heading: "Don't Recycle Variables or Parameters", priority: "0:2"},
              {name: "avoidEmptyCatchBlocks", heading: "Avoid Empty Catch Blocks", priority: "0:2"},
              {name: "deleteDeadCode", heading: "Delete Dead Code", priority: "0:2"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "minimiseVariableScope", heading: "Minimise Scope of Variables", priority: "0:3"},
              {name: "minimiseCodeDuplication", heading: "Minimise Code Duplication", priority: "0:3"}
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
              {name: "introduction", heading: "Introduction", priority: "0:2"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "dontRepeatObvious", heading: "Do Not Repeat the Obvious", priority: "0:2"},
              {name: "writeToReader", heading: "Write to the Reader", priority: "0:2"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "explainWhatWhyNotHow", heading: "Explain WHAT and WHY, not HOW", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"},
              {name: "when", heading: "When", priority: "0:4"}
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
              {name: "what", heading: "What", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          },
          {
            name: "documentMinimally",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "tools",
        level_two_topics: [
          {
            name: "javaDoc",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:1"},
              {name: "how", heading: "How", priority: "0:1"},
              {name: "when", heading: "When", priority: "0:2"}
            ]
          }
        ]
      },
      {
        name: "assertions",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"},
              {name: "when", heading: "When", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "logging",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "defensiveProgramming",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"},
              {name: "compulsoryAssociations", heading: "Enforcing Compulsory Associations", priority: "3"},
              {name: "1to1Associations", heading: "Enforcing 1-to3 Associations", priority: "3"},
              {name: "referentialIntegrity", heading: "Enforcing Referential Integrity", priority: "3"},
              {name: "when", heading: "When", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "designByContract",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "Design by Contract", priority: "3"}
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
              {name: "what", heading: "What", priority: "0:1"}
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
              {name: "lateVsEarly", heading: "'Late and One Time' vs 'Early and Frequent'", priority: "2"},
              {name: "bigBangVsIncremental", heading: "Big-Bang vs Incremental Integration", priority: "3"},
              {name: "topDownVsBottomUp", heading: "Top-Down vs Bottom-Up Integration", priority: "4"}
            ]
          }
        ]
      },
      {
        name: "buildAutomation",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:1"},
              {name: "continuousIntegrationDeployment", heading: "Continuous Integration and Continuous Deployment", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "when", heading: "When", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
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
              {name: "what", heading: "What", priority: "0:1"},
              {name: "how", heading: "How", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "frameworksVsLibraries", heading: "Frameworks vs Libraries", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "cloudComputing",
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "validationVsVerification", heading: "Validation vs Verification", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "testability", heading: "Testability", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "testingTypes",
        level_two_topics: [
          {
            name: "unitTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:1"},
              {name: "stubs", heading: "Stubs", priority: "0:3"}
            ]
          },
          {
            name: "integrationTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          },
          {
            name: "systemTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"}
            ]
          },
          {
            name: "alphaBetaTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "dogfooding",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "developerTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "why", heading: "Why", priority: "0:3"}
            ]
          },
          {
            name: "exploratoryVsScriptedTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"},
              {name: "when", heading: "When", priority: "0:3"}
            ]
          },
          {
            name: "acceptanceTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "acceptanceVsSystemTesting", heading: "Acceptance vs System Testing", priority: "0:3"}
            ]
          },
          {
            name: "regressionTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "testingTextUis", heading: "Automated Testing of CLI Apps", priority: "0:2"},
              {name: "usingTestDrivers", heading: "Test Automation Using Test Drivers", priority: "0:3"},
              {name: "tools", heading: "Test Automation Tools", priority: "0:3"},
              {name: "testingGuis", heading: "Automated Testing of GUIs", priority: "0:4"}
            ]
          }
        ]
      },
      {
        name: "testCoverage",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "dependencyInjection",
        priority: "0:4",
        level_two_topics: [
          {
            name: "",
            priority: "0:4",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:4"},
              {name: "how", heading: "How", priority: "0:4"}
            ]
          }
        ]
      },
      {
        name: "tdd",
        priority: "0:4",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:4"},
              {name: "how", heading: "How", priority: "0:4"}
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
              {name: "what", heading: "What", priority: "0:3"},
              {name: "positiveVsNegative", heading: "Positive vs Negative Test Cases", priority: "0:2"},
              {name: "blackVsGlass", heading: "Black Box vs Glass Box", priority: "0:2"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "basic", heading: "Basic", priority: "0:2"},
              {name: "intermediate", heading: "Intermediate", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "how", heading: "How", priority: "0:3"}
            ]
          }
        ]
      },
      {
        name: "combiningTestInputs",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "why", heading: "Why", priority: "3"},
              {name: "combinationStrategies", heading: "Test Input Combination Strategies", priority: "3"},
              {name: "heuristicValid", heading: "Heuristic: Each Valid Input at Least Once in a Positive Test Case", priority: "3"},
              {name: "heuristicInvalid", heading: "Heuristic: No More Than One Invalid Input In A Test Case", priority: "3"},
              {name: "mix", heading: "Mix", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "more",
        level_two_topics: [
          {
            name: "",
            priority: "-1",
            level_three_topics: [
              {name: "testingUseCases", heading: "Testing Based on Use Cases", priority: "-1"}
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
              {name: "recap", heading: "Recap", priority: "-1"},
              {name: "exercises", heading: "Exercises", priority: "0:3"}
            ]
          }
        ]
      }
    ]
  },
  revisionControl : {
    name: "revisionControl",
    heading: "Revision Control",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"},
              {name: "repositories", heading: "Repositories", priority: "0:1"},
              {name: "savingHistory", heading: "Saving History", priority: "0:1"},
              {name: "usingHistory", heading: "Using History", priority: "0:2"},
              {name: "remoteRepositories", heading: "Remote Repositories", priority: "0:2"},
              {name: "branching", heading: "Branching", priority: "0:2"},
              {name: "drcsVsCrcs", heading: "DRCS vs CRCS", priority: "0:3"},
              {name: "forkingWorkflow", heading: "Forking Flow", priority: "0:2"},
              {name: "featureBranchFlow", heading: "Feature Branch Flow", priority: "0:4"},
              {name: "centralizedFlow", heading: "Centralized Flow", priority: "0:4"}
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
              {name: "workBreakdownStructure", heading: "Work Breakdown Structure", priority: "0:3"},
              {name: "milestones", heading: "Milestones", priority: "0:2"},
              {name: "buffers", heading: "Buffers", priority: "0:3"},
              {name: "issueTrackers", heading: "Issue Trackers", priority: "0:2"},
              {name: "ganttCharts", heading: "GANTT Charts", priority: "0:4"},
              {name: "pertCharts", heading: "PERT Charts", priority: "0:4"}
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
              {name: "teamStructures", heading: "Team Structures", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:2"},
              {name: "sequentialModels", heading: "Sequential Models", priority: "0:2"},
              {name: "iterativeModels", heading: "Iterative Models", priority: "0:2"},
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
              {name: "unifiedProcess", heading: "Unified Process", priority: "3"}
            ]
          }
        ]
      },
      {
        name: "more",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "cmmi", heading: "CMMI", priority: "3"}
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
              {name: "recap", heading: "Recap", priority: "0:3"}
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
              {name: "what", heading: "What", priority: "0:1"}
            ]
          },
          {
            name: "classes",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:1"}
            ]
          },
          {
            name: "associations",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:1"},
              {name: "navigability", heading: "Navigability", priority: "0:2"},
              {name: "roles", heading: "Roles", priority: "0:3"},
              {name: "labels", heading: "Labels", priority: "0:2"},
              {name: "multiplicity", heading: "Multiplicity", priority: "0:3"}
            ]
          },
          {
            name: "dependencies",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "associationsAsAttributes",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "enumerations",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "classLevelMembers",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "associationClasses",
            level_three_topics: [
              {name: "what", heading: "What", priority: "3"}
            ]
          },
          {
            name: "composition",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"}
            ]
          },
          {
            name: "aggregation",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "classInheritance",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"}
            ]
          },
          {
            name: "interfaces",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:2"}
            ]
          },
          {
            name: "abstractClasses",
            level_three_topics: [
              {name: "what", heading: "What", priority: "0:3"}
            ]
          },
          {
            name: "combine",
            priority: "0:4",
            level_three_topics: [
              {name: "basic", heading: "Basic", priority: "0:2"}
            ]
          }
        ]
      },
      {
        name: "sequenceDiagrams",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "0:1"},
              {name: "basic", heading: "Basic", priority: "0:1"},
              {name: "objectCreation", heading: "Object Creation", priority: "0:2"},
              {name: "objectDeletion", heading: "Object Deletion", priority: "0:3"},
              {name: "loops", heading: "Loops", priority: "0:2"},
              {name: "selfInvocation", heading: "Self Invocation", priority: "0:3"},
              {name: "alternativePaths", heading: "Alternative Paths", priority: "0:3"},
              {name: "optionalPaths", heading: "Optional Paths", priority: "0:3"},
              {name: "parallelPaths", heading: "Parallel Paths", priority: "0:3"},
              {name: "referenceFrames", heading: "Reference Frames", priority: "0:3"},
              {name: "staticMethods", heading: "Calls to Static Methods", priority: "0:3"},
              {name: "minimalNotation", heading: "Minimal Notation", priority: "0:3"}
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
              {name: "introduction", heading: "Introduction", priority: "0:1"},
              {name: "objects", heading: "Objects", priority: "0:1"},
              {name: "associations", heading: "Associations", priority: "0:1"}
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
              {name: "linearPaths", heading: "Linear Paths", priority: "2"},
              {name: "alternatePaths", heading: "Alternate Paths", priority: "2"},
              {name: "parallelPaths", heading: "Parallel Paths", priority: "2"},
              {name: "rakes", heading: "Rakes", priority: "3"},
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
              {name: "notes", heading: "Notes", priority: "0:3"},
              {name: "constraints", heading: "Constraints", priority: "-1"}
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
              {name: "objectVsClassDiagrams", heading: "Object vs Class Diagrams", priority: "0:2"}
            ]
          }
        ]
      }
    ]
  },
  intellij : {
    name: "intellij",
    heading: "Intellij IDEA",
    priority: "0:4",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            priority: "0:4",
            level_three_topics: [
              {name: "projectSetup", heading: "Project Setup", priority: "0:3"},
              {name: "codeNavigation", heading: "Code Navigation", priority: "0:3"},
              {name: "productivityShortcuts", heading: "Productivity Shortcuts", priority: "0:4"},
              {name: "debuggingBasic", heading: "Debugging: Basic", priority: "0:3"},
              {name: "refactoring", heading: "Refactoring", priority: "0:3"}
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
              {name: "init", heading: "`init`: Getting started", priority: "0:1"},
              {name: "commit", heading: "`commit`: Saving changes to history", priority: "0:1"},
              {name: "ignore", heading: "Omitting files from revision control", priority: "0:2"},
              {name: "tag", heading: "`tag`: Naming commits", priority: "0:3"},
              {name: "diff", heading: "`diff`: Comparing revisions", priority: "0:2"},
              {name: "checkout", heading: "`checkout`: Retrieving a specific revision", priority: "0:2"},
              {name: "stash", heading: "`stash`: Shelving changes temporarily", priority: "3"},
              {name: "clone", heading: "`clone`: Copying a repo", priority: "0:1"},
              {name: "pull", heading: "`pull`, `fetch`: Downloading data from other repos", priority: "0:1"},
              {name: "fork", heading: "Fork: Creating a remote copy", priority: "0:1"},
              {name: "push", heading: "`push`: Uploading data to other repos", priority: "0:1"},
              {name: "branch", heading: "`branch`: Doing multiple parallel changes", priority: "0:2"},
              {name: "mergeConflicts", heading: "Dealing with merge conflicts", priority: "0:2"},
              {name: "createPRs", heading: "Creating PRs", priority: "0:1"},
              {name: "reviewPRs", heading: "Reviewing PRs", priority: "0:2"},
              {name: "managePRs", heading: "Merging PRs", priority: "0:2"},
              {name: "forkingWorkflow", heading: "Forking Workflow", priority: "0:3"}
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
              {name: "singleResponsibilityPrinciple", heading: "Single Responsibility Principle", priority: "0:2"},
              {name: "openClosedPrinciple", heading: "Open-Closed Principle", priority: "3"},
              {name: "liskovSubstitutionPrinciple", heading: "Liskov Substitution Principle", priority: "3"},
              {name: "interfaceSegregationPrinciple", heading: "Interface Segregation Principle", priority: "4"},
              {name: "dependencyInversionPrinciple", heading: "Dependency Inversion Principle", priority: "4"},
              {name: "solidPrinciples", heading: "SOLID Principles", priority: "3"},
              {name: "separationOfConcernsPrinciple", heading: "Separation of Concerns Principle", priority: "0:2"},
              {name: "lawOfDemeter", heading: "Law of Demeter", priority: "3"},
              {name: "yagniPrinciple", heading: "YAGNI Principle", priority: "3"},
              {name: "dryPrinciple", heading: "DRY Principle", priority: "3"},
              {name: "brooksLaw", heading: "Brooks' Law", priority: "3"},
              {name: "review", heading: "Review", priority: "3"}
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
              {name: "how", heading: "How Java Works", priority: "0:3"},
              {name: "editions", heading: "Java Editions", priority: "0:3"}
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
              {name: "basic", heading: "JUnit: Basic", priority: "0:2"},
              {name: "intermediate", heading: "JUnit: Intermediate", priority: "0:3"}
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
              {name: "varargs", heading: "Varargs ", priority: "0:4"},
              {name: "streams", heading: "Streams ", priority: "0:4"},
              {name: "javaFX", heading: "JavaFX ", priority: "0:4"}
            ]
          }
        ]
      }
    ]
  }
} %}
