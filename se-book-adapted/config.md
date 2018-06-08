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
    }
} %}

{% set topics = [
{heading: "Design", name: "design", chapters: [chapters.architecture]}
] %}


