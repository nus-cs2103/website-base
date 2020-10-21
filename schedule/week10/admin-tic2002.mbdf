{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Add individual feature 1
1. Implement increments `Level-9`, `A-CodingStandard`, `A-CodeQuality`
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }} Add individual feature 1

* Note that ==a very minimal implementation of the feature is good enough==.
* Steps to find the feature you should implement:
  * First take the last digit of your student number. For example, if your student number is `A0123456H`, the last digit is `6`.
  * Then, find the matching row in the table below. That row gives you three options.
  * You may implement any one of the three options. Click on the link to find details of the feature.

<div class="indented-level2" id="feature-allocation">

{% macro ilink(increment) %}[`{{ increment }}`](../../se-book-adapted/projectDuke/index.html#{{ increment | lower }}){% endmacro %}

digit | option 1                             | option 2                            | option 3
------|--------------------------------------|-------------------------------------|-------------------------
0     | {{ ilink('B-TentativeScheduling') }} | {{ ilink('C-DetectDuplicates') }}   | {{ ilink('C-Statistics') }}
1     | {{ ilink('B-Snooze') }}              | {{ ilink('C-FlexibleDataSource') }} | {{ ilink('C-Undo') }}
2     | {{ ilink('B-RecurringTasks') }}      | {{ ilink('C-Sort') }}               | {{ ilink('C-Help') }}
3     | {{ ilink('B-DoAfterTasks') }}        | {{ ilink('C-NaturalDates') }}       | {{ ilink('C-FriendlierSyntax') }}
4     | {{ ilink('B-DoWithinPeriodTasks') }} | {{ ilink('C-BetterSearch') }}       | {{ ilink('B-Snooze') }}
5     | {{ ilink('B-FixedDurationTasks') }}  | {{ ilink('C-Update') }}             | {{ ilink('B-RecurringTasks') }}
6     | {{ ilink('B-Reminders') }}           | {{ ilink('C-Tagging') }}            | {{ ilink('B-DoAfterTasks') }}
7     | {{ ilink('B-FindFreeTimes') }}       | {{ ilink('C-Priority') }}           | {{ ilink('B-DoWithinPeriodTasks') }}
8     | {{ ilink('B-ViewSchedules') }}       | {{ ilink('C-Archive') }}            | {{ ilink('B-FixedDurationTasks') }}
9     | {{ ilink('B-DetectAnomalies') }}     | {{ ilink('C-MassOps') }}            | {{ ilink('B-ViewSchedules') }}
</div>

#### {{ thumb(2) }} Implement increments `Level-9`, `A-CodingStandard`, `A-CodeQuality`

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-9`: Find**" var-fragment="text.md#Level-9" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-CodingStandard`: Coding Standard**" var-fragment="extensions.mbdf#A-CodingStandard" />
<div class="indented-level4">

↳ The coding standard to follow is given [here]({{ url_java_coding_standard }}) -- also given under the `Links` menu at the top of the module website.
</div>
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-CodeQuality`: Increase Code Quality**" var-fragment="extensions.mbdf#A-CodeQuality" />
<div class="indented-level4">

↳ The code quality guidelines to follow are given [here](../../se-book-adapted/chapters/codeQuality.html).
</div>
</div>
</div>
