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
{{ show_expanded_faq("whenCanWeSeeQuizAnswers") }}

## FAQs on: tP

{{ show_expanded_faq("dgDetailsLevel") }}
{{ show_expanded_faq("dgAddNewUml") if cs2103 }}
{{ show_expanded_faq("githubWhoCreatesIssues") }}
{{ show_expanded_faq("githubIssuesForNonCodingTasks") }}
{{ show_expanded_faq("githubIssuesSubTasks") }}
{{ show_expanded_faq("githubMultipleIssueAssignees") }}
{{ show_expanded_faq("githubIssuesMultipleDocAuthors") }}
{{ show_expanded_faq("githubIssueForEachPr") }}
{{ show_expanded_faq("githubWhoMergesPrs") }}
{{ show_expanded_faq("tpHowMuchToGetFullMarks") }}
{{ show_expanded_faq("tpEnoughFeatures") if cs2103 }}
{{ show_expanded_faq("tpMustWrite300Loc") if cs2103 }}
{{ show_expanded_faq("tpFullMarksFor300Loc") if cs2103 }}
{{ show_expanded_faq("tpIterationDeadline") }}
{{ show_expanded_faq("tpNotEnoughWorkToDivide") }}
{{ show_expanded_faq("tpOmitStoriesInAb3") if cs2103 }}
{{ show_expanded_faq("tpHowManyFeaturesInMvp") }}
{{ show_expanded_faq("tpNoPrInIteration") if cs2103}}
{{ show_expanded_faq("tpUpdateTestsWithCode") if cs2103}}
{{ show_expanded_faq("tpUpdateDocsWithCode") if cs2103}}
{{ show_expanded_faq("tpWhyUpdateDiagramsEarly")}}
{{ show_expanded_faq("tpFeatureTakeovers")}}
</div>

{% endcall %}
