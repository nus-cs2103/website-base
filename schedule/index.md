<frontmatter>
title: "Schedule"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<include src="../common/header.md" />

<div class="website-content">
<panel header="{{glyphicon_calendar}} Tutorial Schedule" no-close>
  <include src="overview/tutorialSchedule.md"/>
</panel>
<include src="overview/index.md" name=":exclamation: For all weeks" dynamic />
<include src="week1/index.md" name=":exclamation: Week 1 [Jan 15]" dynamic />
<panel header=":exclamation: Week 2 [Jan 22]" expanded no-close>
  <include src="week2/index.md"/>
</panel>
<include src="week3/index.md" name="Week 3 [Jan 29]" dynamic />
<include src="week4/index.md" name="Week 4 [Feb 5]" dynamic />
<include src="week5/index.md" name="Week 5 [Feb 12]" dynamic />
<include src="week6/index.md" name="Week 6 [Feb 19]" dynamic />
<include src="week7/index.md" name="Week 7 [Mar 5]" dynamic />
<include src="week8/index.md" name="Week 8 [Mar 12]" dynamic />
<include src="week9/index.md" name="Week 9 [Mar 19]" dynamic />
<include src="week10/index.md" name="Week 10 [Mar 26]" dynamic />
<include src="week11/index.md" name="Week 11 [Apr 2]" dynamic />
<include src="week12/index.md" name="Week 12 [Apr 9]" dynamic />
<include src="week13/index.md" name="Week 13 [Apr 16]" dynamic />
</div>