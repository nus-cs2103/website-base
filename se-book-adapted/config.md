{% set chapters = { 
  architecture : {
    name: "architecture", 
    heading: "Architecture",
    level_one_topics: [
      {
        name: "introduction",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "what"}]}
        ]
      },
      {
        name: "architectureDiagrams",
        level_two_topics: [
          {name: "", level_three_topics: [{name: "reading"}, {name: "drawing"}]}
        ]
      },
      {
        name: "architecturalStyles",
        level_two_topics: [
          {name: "introduction", level_three_topics: [{name: "what"}]},
          {name: "nTier", level_three_topics: [{name: "what"}]},
          {name: "clientServer", level_three_topics: [{name: "what"}]},
          {name: "transactionProcessing", level_three_topics: [{name: "what"}]},
          {name: "serviceOriented", level_three_topics: [{name: "what"}]},
          {name: "eventDriven", level_three_topics: [{name: "what"}]},
          {name: "more", level_three_topics: [{name: "moreStyles"}, {name: "usingStyles"}]}
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
          {name: "", level_three_topics: [{name: "basic"}]}
        ]
      },
      {
        name: "maximiseReadability",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "avoidLongMethods"}, 
              {name: "avoidDeepNesting"}, 
              {name: "avoidComplicatedExpressions"}, 
              {name: "avoidMagicNumbers"}, 
              {name: "makeCodeObvious"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"structureCodeLogically"},
              {name:"dontTripReader"},
              {name:"practiceKISSing"},
              {name:"avoidPrematureOptimizations"},
              {name:"slapHard"}
            ]
          },
          {
            name: "advanced", 
            level_three_topics: [{name: "makeHappyPathProminent"}]
          }
        ]
      },
      {
        name: "followStandard",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[
              {name: "introduction"},
              {name: "basic"},
              {name: "intermediate"}
            ]
          }
        ]
      },
      {
        name: "nameWell",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "nounsAndVerbsAsNames"}, 
              {name: "useStandardWords"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"useNameExplain"},
              {name:"notTooLongNorShort"},
              {name:"avoidMisleadingNames"}
            ]
          }
        ]
      },
      {
        name: "avoidShortcuts",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "useDefaultBranch"}, 
              {name: "dontRecycleVarsOrParams"}, 
              {name: "avoidEmptyCatchBlocks"}, 
              {name: "deleteDeadCode"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [
              {name:"minimiseVariableScope"},
              {name:"minimiseCodeDuplication"}
            ]
          }
        ]
      },
      {
        name: "commentMinimally",
        level_two_topics: [
          {
            name: "", 
            level_three_topics:[{name: "introduction"}]
          },
          {
            name: "basic", 
            level_three_topics:[
              {name: "dontRepeatObvious"}, 
              {name: "writeToReader"}
            ]
          },
          {
            name: "intermediate", 
            level_three_topics: [{name:"explainWhatWhyNotHow"}]
          }
        ]
      }
    ]
  }
} %}

{% set topics = [
  {heading: "Design", chapters: [chapters.architecture]},
  {heading: "Implementation", chapters: [chapters.codeQuality]}
  ] 
%}
