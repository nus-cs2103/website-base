{% set chapters = { 
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
              {name: "prosAndCons", heading: "Pros and Cons", priority: "1"}
            ]
          }
        ]
      }
    ]
  },
  oopDesign : {
    name: "oopDesign",
    heading: "OOP - Concepts",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "Introduction", priority: "1"}
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
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "abstraction", heading: "Objects as Abstractions", priority: "1"},
              {name: "encapsulation", heading: "Encapsulation Of Objects", priority: "1"}
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
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "classLevelMembers", heading: "Class Level Members", priority: "1"},
              {name: "enumerations", heading: "Enumerations", priority: "1"}
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
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "navigability", heading: "Navigability", priority: "1"},
              {name: "multiplicity", heading: "Multiplicity", priority: "1"},
              {name: "dependencies", heading: "Dependencies", priority: "1"},
              {name: "composition", heading: "Composition", priority: "1"},
              {name: "aggregation", heading: "Aggregation", priority: "1"},
              {name: "associationClasses", heading: "Association Classes", priority: "1"}
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
              {name: "overriding", heading: "Overriding", priority: "1"},
              {name: "overloading", heading: "Overloading", priority: "1"},
              {name: "interfaces", heading: "Interfaces", priority: "1"},
              {name: "abstractClasses", heading: "Abstract Classes", priority: "1"},
              {name: "dynamicAndStaticBinding", heading: "Dynamic and Static Binding", priority: "1"},
              {name: "substitutability", heading: "Substitutability", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "mechanism", heading: "Mechanism", priority: "1"}
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
              {name: "miscellaneous", heading: "Miscellaneous", priority: "1"},
              {name: "review", heading: "Review", priority: "1"}
            ]
          }
        ]
      }
    ]
  },
  oopImplementation : {
    name: "oopImplementation",
    heading: "OOP - Implementation",
    level_one_topics: [
      {
        name: "",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "classes", heading: "Implementing Classes", priority: "1"},
              {name: "classLevelMembers", heading: "Implementing Class-Level Members", priority: "1"},
              {name: "associations", heading: "Implementing Associations", priority: "1"},
              {name: "dependencies", heading: "Implementing Dependencies", priority: "1"},
              {name: "composition", heading: "Implementing Composition", priority: "1"},
              {name: "aggregation", heading: "Implementing Aggregation", priority: "1"},
              {name: "associationClasses", heading: "Implementing Association Classes", priority: "1"},
              {name: "inheritance", heading: "Implementing Inheritance", priority: "1"},
              {name: "overriding", heading: "Implementing Overriding", priority: "1"},
              {name: "overloading", heading: "Implementing Overloading", priority: "1"},
              {name: "interfaces", heading: "Implementing Interfaces", priority: "1"},
              {name: "abstractClasses", heading: "Implementing Abstract Classes", priority: "1"},
              {name: "polymorphism", heading: "Implementing Polymorphism", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "nonFunctionalRequirements", heading: "Non-Functional Requirements", priority: "1"},
              {name: "prioritizing", heading: "Prioritizing Requirements", priority: "1"},
              {name: "quality", heading: "Quality of Requirements", priority: "1"}
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
              {name: "brainstorming", heading: "Brainstorming", priority: "1"},
              {name: "userSurveys", heading: "User Surveys", priority: "1"},
              {name: "observation", heading: "Observation", priority: "1"},
              {name: "interviews", heading: "Interviews", priority: "1"},
              {name: "focusGroups", heading: "Focus Groups", priority: "1"},
              {name: "prototyping", heading: "Prototyping", priority: "1"},
              {name: "productSurveys", heading: "Product Surveys", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "details", heading: "Details", priority: "1"},
              {name: "usage", heading: "Usage", priority: "1"}
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
              {name: "identifying", heading: "Identifying", priority: "1"},
              {name: "details", heading: "Details", priority: "1"},
              {name: "usage", heading: "Usage", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"},
              {name: "types", heading: "Types of Coupling", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"},
              {name: "umlModels", heading: "UML Models", priority: "1"}
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
              {name: "ooStructures", heading: "OO Structures", priority: "1"},
              {name: "classDiagramsBasic", heading: "Class Diagrams (Basics)", priority: "1"},
              {name: "classDiagramsIntermediate", heading: "Class Diagrams - Intermediate", priority: "1"},
              {name: "classDiagramsAdvanced", heading: "Class Diagrams - Advanced", priority: "1"},
              {name: "objectDiagrams", heading: "Object Diagrams", priority: "1"},
              {name: "objectOrientedDomainModels", heading: "Object Oriented Domain Models", priority: "1"},
              {name: "deploymentDiagrams", heading: "Deployment Diagrams", priority: "1"},
              {name: "componentDiagrams", heading: "Component Diagrams", priority: "1"},
              {name: "packageDiagrams", heading: "Package Diagrams", priority: "1"},
              {name: "compositeStructureDiagrams", heading: "Composite Structure Diagrams", priority: "1"}
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
              {name: "activityDiagrams", heading: "Activity Diagrams", priority: "1"},
              {name: "sequenceDiagramsBasic", heading: "Sequence Diagrams - Basic", priority: "1"},
              {name: "sequenceDiagramsIntermediate", heading: "Sequence Diagrams - Intermediate", priority: "1"},
              {name: "sequenceDiagramsAdvanced", heading: "Sequence Diagrams - Advanced", priority: "1"},
              {name: "useCaseDiagrams", heading: "Use Case Diagrams", priority: "1"},
              {name: "timingDiagrams", heading: "Timing Diagrams", priority: "1"},
              {name: "interactionOverviewDiagrams", heading: "Interaction Overview Diagrams", priority: "1"},
              {name: "communicationDiagrams", heading: "Communication Diagrams", priority: "1"},
              {name: "stateMachineDiagrams", heading: "State Machine Diagrams", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "modelingASolution",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "intermediate", heading: "Intermediate", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "nTier",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "clientServer",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "transactionProcessing",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "serviceOriented",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "eventDriven",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "more",
            level_three_topics: [
              {name: "moreStyles", heading: "More Styles", priority: "1"},
              {name: "usingStyles", heading: "Using Styles", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "format", heading: "Format", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "implementation", heading: "Implementation", priority: "1"},
              {name: "evaluation", heading: "Evaluation", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "abstractionOccurrence",
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
        name: "facade",
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
        name: "command",
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
        name: "modelViewController",
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
        name: "observer",
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
        name: "more",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "combiningDesignPatterns", heading: "Combining Design Patterns", priority: "1"},
              {name: "otherDesignPatterns", heading: "Other Design Patterns", priority: "1"},
              {name: "usingDesignPatterns", heading: "Using Design Patterns", priority: "1"},
              {name: "otherTypesOfPatterns", heading: "Other Types of Patterns", priority: "1"},
              {name: "vsPrinciples", heading: "Design Patterns vs Design Principles", priority: "1"}
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
              {name: "what", heading: "Multi-Level Design", priority: "1"}
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
              {name: "what", heading: "Top-Down and Bottom-Up Design", priority: "1"}
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
              {name: "what", heading: "Agile Design", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "basic", heading: "Basic", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "avoidLongMethods", heading: "Avoid Long Methods", priority: "1"},
              {name: "avoidDeepNesting", heading: "Avoid Deep Nesting", priority: "1"},
              {name: "avoidComplicatedExpressions", heading: "Avoid Complicated Expressions", priority: "1"},
              {name: "avoidMagicNumbers", heading: "Avoid Magic Numbers", priority: "1"},
              {name: "makeCodeObvious", heading: "Make the Code Obvious", priority: "1"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "structureCodeLogically", heading: "Structure Code Logically", priority: "1"},
              {name: "dontTripReader", heading: "Do Not 'Trip Up' Reader", priority: "1"},
              {name: "practiceKISSing", heading: "Practice KISSing", priority: "1"},
              {name: "avoidPrematureOptimizations", heading: "Avoid Premature Optimizations", priority: "1"},
              {name: "slapHard", heading: "SLAP Hard", priority: "1"}
            ]
          },
          {
            name: "advanced",
            level_three_topics: [
              {name: "makeHappyPathProminent", heading: "Make the Happy Path Prominent", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"},
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "intermediate", heading: "Intermediate", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "nounsAndVerbsAsNames", heading: "Use Nouns for Things and Verbs for Actions", priority: "1"},
              {name: "useStandardWords", heading: "Use Standard Words", priority: "1"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "useNameExplain", heading: "Use Name to Explain", priority: "1"},
              {name: "notTooLongNorShort", heading: "Not Too Long, Not Too Short", priority: "1"},
              {name: "avoidMisleadingNames", heading: "Avoid Misleading Names", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "useDefaultBranch", heading: "Use the Default Branch", priority: "1"},
              {name: "dontRecycleVarsOrParams", heading: "Don't Recycle Variables or Parameters", priority: "1"},
              {name: "avoidEmptyCatchBlocks", heading: "Avoid Empty Catch Blocks", priority: "1"},
              {name: "deleteDeadCode", heading: "Delete Dead Code", priority: "1"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "minimiseVariableScope", heading: "Minimise Scope of Variables", priority: "1"},
              {name: "minimiseCodeDuplication", heading: "Minimise Code Duplication", priority: "1"}
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
              {name: "introduction", heading: "Introduction", priority: "1"}
            ]
          },
          {
            name: "basic",
            level_three_topics: [
              {name: "dontRepeatObvious", heading: "Do Not Repeat the Obvious", priority: "1"},
              {name: "writeToReader", heading: "Write to the Reader", priority: "1"}
            ]
          },
          {
            name: "intermediate",
            level_three_topics: [
              {name: "explainWhatWhyNotHow", heading: "Explain WHAT and WHY, not HOW", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "why", heading: "Why", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          },
          {
            name: "aimForComprehensibility",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          },
          {
            name: "documentMinimally",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          },
          {
            name: "markdown",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          },
          {
            name: "asciiDoc",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "how", heading: "How", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "compulsoryAssociations", heading: "Enforcing Compulsory Associations", priority: "1"},
              {name: "1to1Associations", heading: "Enforcing 1-to-1 Associations", priority: "1"},
              {name: "referentialIntegrity", heading: "Enforcing Referential Integrity", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
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
              {name: "what", heading: "Design by Contract", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "lateVsEarly", heading: "'Late and One Time' vs 'Early and Frequent'", priority: "1"},
              {name: "bigBangVsIncremental", heading: "Big-Bang vs Incremental Integration", priority: "1"},
              {name: "topDownVsBottomUp", heading: "Top-Down vs Bottom-Up Integration", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "continuousIntegrationDeployment", heading: "Continuous Integration and Continuous Deployment", priority: "1"}
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
              {name: "review", heading: "Review", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "designingAPIs", heading: "Designing APIs", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "frameworksVsLibraries", heading: "Frameworks vs Libraries", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "services", heading: "Iaas, PaaS, and SaaS", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "validationVsVerification", heading: "Validation vs Verification", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "testability", heading: "Testability", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "stubs", heading: "Stubs", priority: "1"}
            ]
          },
          {
            name: "integrationTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          },
          {
            name: "systemTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "alphaBetaTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "dogfooding",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
            ]
          },
          {
            name: "developerTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "why", heading: "Why", priority: "1"}
            ]
          },
          {
            name: "exploratoryVsScriptedTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "when", heading: "When", priority: "1"}
            ]
          },
          {
            name: "acceptanceTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "acceptanceVsSystemTesting", heading: "Acceptance vs System Testing", priority: "1"}
            ]
          },
          {
            name: "regressionTesting",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "testingTextUis", heading: "Automated Testing of CLI Apps", priority: "1"},
              {name: "usingTestDrivers", heading: "Test Automation Using Test Drivers", priority: "1"},
              {name: "tools", heading: "Test Automation Tools", priority: "1"},
              {name: "testingGuis", heading: "Automated Testing of GUIs", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "dependencyInjection",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "tdd",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "positiveVsNegative", heading: "Positive vs Negative Test Cases", priority: "1"},
              {name: "blackVsGlass", heading: "Black Box vs Glass Box", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "basic", heading: "Basic", priority: "1"},
              {name: "intermediate", heading: "Intermediate", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "how", heading: "How", priority: "1"}
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
              {name: "why", heading: "Why", priority: "1"},
              {name: "combinationStrategies", heading: "Test Input Combination Strategies", priority: "1"},
              {name: "heuristicValid", heading: "Heuristic: Each Valid Input at Least Once in a Positive Test Case", priority: "1"},
              {name: "heuristicInvalid", heading: "Heuristic: No More Than One Invalid Input In A Test Case", priority: "1"},
              {name: "mix", heading: "Mix", priority: "1"}
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
              {name: "testingUseCases", heading: "Testing Based on Use Cases", priority: "1"}
            ]
          }
        ]
      },
      {
        name: "summary",
        level_two_topics: [
          {
            name: "",
            level_three_topics: [
              {name: "recap", heading: "Recap", priority: "1"},
              {name: "exercises", heading: "Exercises", priority: "1"}
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
              {name: "what", heading: "What", priority: "1"},
              {name: "repositories", heading: "Repositories", priority: "1"},
              {name: "savingHistory", heading: "Saving History", priority: "1"},
              {name: "usingHistory", heading: "Using History", priority: "1"},
              {name: "remoteRepositories", heading: "Remote Repositories", priority: "1"},
              {name: "branching", heading: "Branching", priority: "1"},
              {name: "drcsVsCrcs", heading: "DRCS vs CRCS", priority: "1"},
              {name: "forkingWorkflow", heading: "Forking Flow", priority: "1"},
              {name: "featureBranchFlow", heading: "Feature Branch Flow", priority: "1"},
              {name: "centralizedFlow", heading: "Centralized Flow", priority: "1"}
            ]
          }
        ]
      }
    ]
  }
} %}

{% set topics = [
  {heading: "Software Engineering", chapters: [chapters.softwareEngineering]},
  {heading: "Object-Oriented Programming (with UML)", chapters: [chapters.oopDesign, chapters.oopImplementation]},
  {heading: "Requirements", chapters: [chapters.requirements, chapters.gatheringRequirements, chapters.specifyingRequirements]},
  {heading: "Design", chapters: [chapters.design, chapters.designFundamentals, chapters.modeling, chapters.architecture, chapters.designPatterns, chapters.designApproaches]},
  {heading: "Implementation", chapters: [chapters.ides, chapters.codeQuality, chapters.refactoring, chapters.documentation, chapters.errorHandling, chapters.integration, chapters.reuse]},
  {heading: "Quality Assurance", chapters: [chapters.qualityAssurance, chapters.testing, chapters.testCaseDesign]},
  {heading: "Project Management", chapters: [chapters.revisionControl]}
  ] 
%}
