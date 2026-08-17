{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}

<include src="../../admin/common-notices-fragment.md#about-summary-tab" />
<include src="../../admin/common-notices-fragment.md#semester-start" />


<panel type="info" header="##### ==[MUST-WATCH]== Briefing Videos for Week 1" peek >

****Before you do anything else,**** **please watch the following briefing videos in the order given.** NUSNET login is required to access videos.

<include src="../../admin/courseBriefings.md#course-briefing-w1" />

</panel>
<p/>

<box type="info">

****Week 1 Lecture**** ({{ get_date(date_w1_start, 4, format=format_normal, time="4-6pm") }}): There is no formal lecture. Lectures (aka _weekly briefings_) start next week.

==**[Optional] Coding Session**==: **We'll use this week's lecture slot as an optional 'coding session' instead.** During that time, you are welcome to come to the lecture venue ({{ lecture_venue }}), sit with your classmates, and get started on Git-Mastery exercises or the project.

* A few of us from the teaching team will be there too, so you can easily ask for our help/input if you encounter issues during that time.
* If you are in CS2103 (not CS2103T), this is also a good chance to meet classmates you can team up with.
</box>

