{% from "common/macros.njk" import  show_stars, show_faq with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("appendixC-faq") %}
<div id="main">

{% macro show_expanded_faq(faq_id) %}
{{ show_faq(faq_id, "y") }}
{% endmacro %}

## FAQs on: General

{{ show_expanded_faq("whereIsEverything") }}
{{ show_expanded_faq("tVsNonT") if cs2103 }}
{{ show_expanded_faq("aPlus") }}
{{ show_expanded_faq("beanCounting") }}
{{ show_expanded_faq("separateWebsite") }}
{{ show_expanded_faq("slideFormat")  if cs2103 }}
{{ show_expanded_faq("narrowProjectScope") }}
{{ show_expanded_faq("favoriteTool") }}
{{ show_expanded_faq("manySubmissions") }}
{{ show_expanded_faq("cs2101Difference") if cs2103  }}
{{ show_expanded_faq("java21")  }}

## FAQs on: Participation

{{ show_expanded_faq("whenCanWeSeeQuizAnswers") }}
{{ show_expanded_faq("participationTaskMissedDueToValidReason") }}

## FAQs on: iP

{{ show_expanded_faq("ipHowTagsUsed") }}
{{ show_expanded_faq("ipBugAfterIncrementDone") }}
{{ show_expanded_faq("ipMultipleIncrementsInSameCommit") }}
{{ show_expanded_faq("ipIncrementAlreadyDone") }}
{{ show_expanded_faq("ipForgotToPushTag") }}
{{ show_expanded_faq("ipIncreaseDashboardFrequency") }}
{{ show_expanded_faq("ipMarksForOptionalIncrements") }}
{{ show_expanded_faq("ipForkedTheWrongRepo") }}
{{ show_expanded_faq("ipIncorrectTagOrBranch") }}
{{ show_expanded_faq("ipNotDoneInBranch") }}
{{ show_expanded_faq("ipOtherDataFormats") }}
{{ show_expanded_faq("ipAspectsNotCoveredByTheStandard") }}
{{ show_expanded_faq("ipCheckstyleMismatchWithCodingStandard") }}
{{ show_expanded_faq("ipMinimumRequirementNotGiven") }}
{{ show_expanded_faq("ipIfSubmissionBelowBar") }}
{{ show_expanded_faq("ipDeadlineExtensions") }}

## FAQs on: Tutorials

{{ show_expanded_faq("tutorialWhatTutorsCanAnswer") }}
{{ show_expanded_faq("tutorialWhyTutorsCannotAnswerAdminQuestions") }}
{{ show_expanded_faq("tutorialWhyTutorsCannotGiveProjectFeedback") }}
{{ show_expanded_faq("tutorialHowToImproveProjectWithoutTutorFeedback") }}
{{ show_expanded_faq("tutorialWhyTutorCannotGiveTechHelp") }}
{{ show_expanded_faq("tutorialWhatIfMissedDueToValidReason") }}
{{ show_expanded_faq("tutorialWhatIfMissedDueToOtherReason") }}
{{ show_expanded_faq("tutorialLength") }}
{{ show_expanded_faq("tutorialWhyF2f") }}
{{ show_expanded_faq("tutorialCannotReachInTime") }}
{{ show_expanded_faq("warmUpTaskRushed") }}

## FAQs on: UML

{{ show_expanded_faq("umlIsItUsedInIndustry") }}
{{ show_expanded_faq("umlAreWeOverdoing") }}
{{ show_expanded_faq("umlWhenNotationNotEnough") }}
{{ show_expanded_faq("umlWhyNoCorrespondenceBetweenUmlAndCode") }}
{{ show_expanded_faq("umlHowToFindIntendedDesignFromCode") }}

## FAQs on: tP

{{ show_expanded_faq("tpUncontactableMembers") }}
{{ show_expanded_faq("tpWhyNarrowTarget") }}
{{ show_expanded_faq("tpHowNarrowTargetCanBe") }}
{{ show_expanded_faq("tpChangeDirectionLater") }}
{{ show_expanded_faq("tpNotEnoughWorkToDivide") }}
{{ show_expanded_faq("tpOmitStoriesInAb3") if cs2103 }}
{{ show_expanded_faq("tpHowManyFeaturesInMvp") }}
{{ show_expanded_faq("tpEncryptDataFile") }}
{{ show_expanded_faq("tpAb3FeatureInMvpSpec") if cs2103 }}
{{ show_expanded_faq("tpNeedForNewFeatureInMvp") if cs2103 }}
{{ show_expanded_faq("tpIterationDeadline") }}
{{ show_expanded_faq("tpMissingIterationDeadlines") }}
{{ show_expanded_faq("githubWhoCreatesIssues") }}
{{ show_expanded_faq("githubIssuesForNonCodingTasks") }}
{{ show_expanded_faq("githubIssuesSubTasks") }}
{{ show_expanded_faq("githubMultipleIssueAssignees") }}
{{ show_expanded_faq("githubIssuesMultipleDocAuthors") }}
{{ show_expanded_faq("githubIssueForEachPr") }}
{{ show_expanded_faq("githubWhoMergesPrs") }}
{{ show_expanded_faq("tpPrReviewRigor") }}
{{ show_expanded_faq("tpRationaleForCurrentDesign") if cs2103 }}
{{ show_expanded_faq("tpMultiStepCmd") }}
{{ show_expanded_faq("tpRenameAbReferences") if cs2103 }}
{{ show_expanded_faq("tpLowMidtermPeerEvaluations") }}
{{ show_expanded_faq("dgDetailsLevel") }}
{{ show_expanded_faq("dgAddNewUml") if cs2103 }}
{{ show_expanded_faq("noEffectOnUml") if cs2103 }}
{{ show_expanded_faq("tpOtherDiagrammingTool") if cs2103 }}
{{ show_expanded_faq("tpIdeGeneratedDiagrams") }}
{{ show_expanded_faq("tpDgKeepingProposedFeatures") if cs2103}}
{{ show_expanded_faq("tpHowMuchToGetFullMarks") }}
{{ show_expanded_faq("tpChangeFeatureSpec") if cs2103 }}
{{ show_expanded_faq("tpEnoughFeatures") if cs2103 }}
{{ show_expanded_faq("tpMustWrite300Loc") if cs2103 }}
{{ show_expanded_faq("tpIsBlankLinesCounted") if cs2103 }}
{{ show_expanded_faq("tpFullMarksFor300Loc") if cs2103 }}
{{ show_expanded_faq("tpIsLocGraded") }}
{{ show_expanded_faq("tpDivideByComponent") }}
{{ show_expanded_faq("tpNoPrInIteration") if cs2103 }}
{{ show_expanded_faq("tpUpdateTestsWithCode") if cs2103 }}
{{ show_expanded_faq("tpCodecovFails") if cs2103 }}
{{ show_expanded_faq("tpIsCiPassingCompulsory") if cs2103 }}
{{ show_expanded_faq("tpUpdateDocsWithCode") if cs2103 }}
{{ show_expanded_faq("tpMustWeFixAllBugs") }}
{{ show_expanded_faq("tpGuiTestAutomation") if cs2103 }}
{{ show_expanded_faq("tpWhyUpdateDiagramsEarly") }}
{{ show_expanded_faq("tpFeatureTakeovers") }}
{{ show_expanded_faq("tpFeatureDesignChoice") }}

### FAQs on: tP Troubleshooting

{{ show_expanded_faq("tpPrPassCiButFailedAfterMerging") }}
{{ show_expanded_faq("tpWorksLocallyFailsCi") }}

### FAQs on: tP PE

{{ show_expanded_faq("peTooLong") }}
{{ show_expanded_faq("peOtherCommitments") }}
{{ show_expanded_faq("peMorePowerfulTools") }}
{{ show_expanded_faq("tpTesterAddingMoreInfoLater") }}
{{ show_expanded_faq("tpBugRejectedWithReason") }}
{{ show_expanded_faq("tpPeAccuracyForNotInScope") }}
{{ show_expanded_faq("tpPeNotInScopeSeverity") }}
{{ show_expanded_faq("tpTestingLessBuggyProducts") }}
{{ show_expanded_faq("tpNoBugsInTestedProduct") }}
{{ show_expanded_faq("tpNeedToFindAllBugs") }}
{{ show_expanded_faq("tpJustifyBugsAcceptedAsIs") }}
{{ show_expanded_faq("tpMoreCodeMeansHigherPenalty") }}
{{ show_expanded_faq("tpRealBugWrongLabel") }}
{{ show_expanded_faq("tpCorrectBugIncorrectSuggestion") }}
{{ show_expanded_faq("tpTesterAddingMoreInfoLater") }}
{{ show_expanded_faq("tpBugRejectedWithReason") }}


## FAQs on: Exam

{{ show_expanded_faq("examMorePastPapersAndAnswers") }}
{{ show_expanded_faq("examSitNearChargingPoint") }}
{{ show_expanded_faq("examWhyNoBackwardNavigation") }}
{{ show_expanded_faq("examGradingFollowUpQuestion") if cs2103 }}
{{ show_expanded_faq("examMissedFollowUpQuestion") if cs2103 }}
{{ show_expanded_faq("examPartialMarksForMsq") if cs2103 }}

</div>

{% endcall %}
